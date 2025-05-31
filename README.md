## Waveform 13 Free (Flatpak)
**NOTE: This wrapper is not verified by, affiliated with, or supported by the Tracktion Software Corporation.**
**The program is the free version and isn't activated!**

Please note that due to lack of actual programming or coding knowledge outside of just messing around with files like these I cannot fix any bugs

I have no near future plans to update it - anyone is free to PR and try to!

### Prerequisites:

- Flatpak installed, obviously
- (Git LFS installed: If you plan to clone this repository and build the Flatpak yourself, you will need Git Large File Storage (Git LFS))

### Installation methods

1. Install the .flatpakref file

2. flatpak-install command

To install:

    flatpak remote-add --user --if-not-exists my-waveform-repo https://github.com/andrimattheu/com.flatpak.community.Waveform13/raw/main/repo/

    flatpak install --user my-waveform-repo com.flatpak.community.Waveform13

    flatpak run com.flatpak.community.Waveform13

To remove the Flatpak application:

    flatpak uninstall --user com.flatpak.community.Waveform13

    flatpak remote-delete --user my-waveform-repo
    
3. git clone - technical

If you know what this is, you probably know - just make sure to have `git-lfs` and pull/checkout the missing files (presumably the binary and files that are not supposed to be ASCII)

    
### Important Notes:

  PipeWire Compatibility: You have to have PipeWire. It does not bundle a separate JACK2 daemon.
  
  Third-Party Plugins (VST/VST3/LV2):
        Waveform 13 expects plugins to be in certain standard locations. You might need to point Waveform to the correct plugin directories within the Flatpak's sandbox. Common paths for plugins inside a Flatpak are often in /app/extensions/Plugins/ (if you add the Linux Audio Plugins extension) or within your ~/.vst, ~/.vst3 directories if they're exposed by your --filesystem=home permission.
        You might need to enable the org.freedesktop.LinuxAudio.Plugins Flatpak extension if you want to use Flatpak'd audio plugins.
