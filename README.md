# MorseCONSOLE 0.236

## Changes since 0.232

### Sidebar auto-hide

- Added optional sidebar auto-hide in both full-screen and windowed modes.
- Hover over the edge handle to reveal the panel. It hides automatically when the pointer moves away.
- The panel overlays the spectrum, keeping the spectrum and waterfall dimensions unchanged.
- The panel remains open while editing fields, dragging sliders or using dropdown lists.
- Auto-hide supports both left and right panel positions. The preference is saved.
- The **Hide Panel / Show Panel** option is removed from the top menu while auto-hide is enabled.
- Fixed the position of the auto-hide option in Settings to prevent overlap with the waterfall palette selector.

Enable this feature under **Settings → AUTO-HIDE PANEL**.


MorseCONSOLE - Windows x64 installer

Requirements: Windows 10/11 x64, .NET Framework 4.7.2 or later with WPF, Yaesu FT-710 and compatible USB audio/CAT/FTDI interfaces. Normal Windows 10/11 installations include the required .NET Framework runtime.

Setup installs MorseCONSOLE for the current Windows user, creates a Start menu shortcut and optionally a desktop shortcut. The target directory is %LOCALAPPDATA%\Programs\MorseCONSOLE. User configuration, registration and QSO data are not bundled and are preserved when reinstalling or updating.

The driver page lets you install the bundled, original signed Silicon Labs CP210x and FTDI packages. Their licences must be accepted separately. Administrator approval is requested only for installation of the drivers. Existing suitable drivers can be retained by clearing "Install the required radio drivers". The final page offers an unchecked option to launch MorseCONSOLE. Selecting it starts the application when you click Finish. The application can then automatically connect CAT and enable MONITOR when suitable devices are detected.

When installing drivers, close programs using the radio interfaces. Check the installation result and driver-install.log. A restart may be required. Cancelling administrator approval leaves MorseCONSOLE installed and reports that the drivers were not installed.

After installation, open Settings and choose the correct CAT port and USB audio routes. Check the radio settings before enabling CW TX. Registration requirements of MorseCONSOLE remain unchanged.

Uninstall via Windows Settings > Apps. Application files and shortcuts are removed. Configuration, licence files, recordings and QSO data are retained. Shared hardware drivers are not removed.

See Terms-of-use.txt and Licenses\Driver-license-links.txt. This package is not digitally signed by the application developer; the bundled vendor driver catalogs and runtime DLLs retain their original signatures.
