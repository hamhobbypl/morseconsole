## MorseCONSOLE 0.250 — changes since 0.236

### New SWR scanner

- Open **SWR Scan** from the top menu to plot SWR against frequency and find the lowest measured SWR.
- Measurements use short **5 W carrier pulses**, with frequency changes made only in receive.
- The default range covers the CW section of the current TX band, with a **5 kHz step**. The range and step can be adjusted within the same supported amateur band.
- The scanner follows the radio's TX VFO: the selected VFO without SPLIT, or the opposite VFO with SPLIT enabled.
- During scanning, the app temporarily selects the measurement VFO and disables SPLIT. Previous VFO selection, SPLIT, frequency, mode, power and other modified settings are restored after completion, STOP or an error, once RX is confirmed.
- The application's **AF GAIN** is muted during the scan and restored afterwards.
- **STOP**, the radio's HI-SWR alarm, an SWR reading above **3:1**, missing RF output or a CAT error stop the measurement.
- Results can be exported to **CSV**. Diagnostic details are saved in swr-scan.log.
- The scanner window uses the application's dark styling, rounded corners and custom title bar.

The antenna tuner must be OFF. Scanning transmits RF; select a clear range permitted by your licence. SWR and power values are approximate readings from the radio's meters, not a calibrated antenna analyser measurement.

### SPLIT and CLAR with CW via CAT

- **CW via CAT** now allows SPLIT and CLAR operation in AUTO, MANUAL and macro modes.
- Native CAT CW playback uses the radio's existing TX VFO and clarifier settings without applying an additional frequency correction.
- Audio-based CW transmission retains its existing restrictions.

### Clearer VFO controls and indicators

- **SPLIT** replaces the former LOCK button in both compact and full-screen layouts.
- The button enables or disables SPLIT on the FT-710 through CAT and shows the confirmed radio state.
- With SPLIT enabled, the large frequency readout temporarily shows the TX VFO during transmission, then returns to the RX VFO.
- Small rounded **RX** and **TX** badges identify each VFO's role. RX is green with white text; TX is red with white text.

### Updating

Install over the existing version. The installer preserves user configuration, registration and QSO data.


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
