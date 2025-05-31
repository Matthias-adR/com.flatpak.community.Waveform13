## Waveform 13 Free (Flatpak)
**NOTE: This wrapper is not verified by, affiliated with, or supported by the Tracktion Software Corporation.**
**The program is the free version and isn't activated!**

Please note that due to lack of actual programming or coding knowledge outside of just messing around with files like these I cannot fix any bugs

I have no near future plans to update it - anyone is free to PR and try to!

### Prerequisites:

* Flatpak installed, duh

### Installation Methods:

#### 📦 1. Download and Install the Flatpak Bundle (Recommended)

1.  **Download the `Waveform13-13.3.13.flatpak` file** from the "Assets" section below this release.
2.  **Open your terminal** in the directory where you downloaded the file (e.g., `~/Downloads/`).
3.  **Run the installation command:**
    ```bash
    flatpak install --user ./Waveform13-13.3.13.flatpak
    ```
    *To install system-wide (requires root privileges), you can omit `--user` and run `sudo flatpak install ./Waveform13-13.3.13.flatpak`.*

#### 🤓 2. Build from Source (advanced stuff, spooky)

1.  **Clone this repository:**
    ```bash
    git clone [https://github.com/andrimattheu/com.flatpak.community.Waveform13.git](https://github.com/andrimattheu/com.flatpak.community.Waveform13.git)
    cd com.flatpak.community.Waveform13
    ```
2.  **Build the Flatpak application:**
    ```bash
    flatpak-builder --force-clean --repo=flatpak-build/repo flatpak-build com.flatpak.community.Waveform13.yaml
    ```
3.  **Install the Flatpak application from your local repository:**
    ```bash
    flatpak install --user flatpak-build/repo com.flatpak.community.Waveform13
    ```
4.  **Run the application:**
    ```bash
    flatpak run com.flatpak.community.Waveform13
    ```

### Updating to a New Version (if I ever update this lol):

This Flatpak bundle does **not** support automatic updates. When a new version is released:

1.  Download the new `.flatpak` file from the latest release on this GitHub page.
2.  Run the `flatpak install --user <new-version-file.flatpak>` command again. Flatpak will automatically handle the upgrade, replacing the old version with the new one.

### Important Notes:

* **PipeWire Compatibility:** You have to have PipeWire installed and running. This Flatpak does not bundle a separate JACK2 daemon.
* **Third-Party Plugins (VST/VST3/LV2):**
    Waveform 13 expects plugins to be in certain standard locations. You might need to point Waveform to the correct plugin directories within the Flatpak's sandbox. Common paths for plugins inside a Flatpak are often in `/app/extensions/Plugins/` (if you use the `org.freedesktop.LinuxAudio.Plugins` extension) or within your `~/.vst`, `~/.vst3` directories if they are exposed by your `--filesystem=home` permission.
    You might need to enable the `org.freedesktop.LinuxAudio.Plugins` Flatpak extension if you want to use Flatpak'd audio plugins (it's automatically enabled but it has to be installed).
* **Flatpak permission issues:** You may have to configure certain parameters in e.g. Flatseal
