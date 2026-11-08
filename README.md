
## MorseCONSOLE 0.280 - Changes since version **0.279**.

### Installer BUG FIX

If you have problem with reinstall app just install new version without uninstalling old.

### Display and macros

- Improved text alignment and reduced clipping at **100%** and **125%** Windows display scaling.
- The macro panel switches to a compact layout when the window is maximized and vertical space is limited, keeping the RF spectrum and waterfall visible.
- Missing required macro values are highlighted in red in both preview and edit modes. Sending is disabled until all required values are entered.

### CW decoder

- Improved CW decoding and word spacing.

### QSO Logger

- Widened the Logger window and added **EXCH RECEIVED** and **EXCH SENT** columns to the saved QSO list.
- Added a **QRZ.COM** button that opens the selected QSO's callsign page in the default browser.

### LOG4OM 2

- Added manual forwarding for the selected saved QSO, including contest exchanges and the sent serial number when available.
- Manual forwarding also works when automatic forwarding is disabled.


## MorseCONSOLE 0.275 — Changes since 0.262

### USB transmit audio and ALC

- **Settings → TX AUDIO LEVEL** adjusts the USB audio sent to the FT-710 for audio CW.
- **TUNE** transmits a continuous 700 Hz tone for up to 10 seconds. The FT-710 ALC reading is displayed live while you adjust the audio level.
- **AUTO ALC** starts at 10% audio level and raises it in 10-point steps. It stops transmitting when the ALC reading levels off and saves the previous step. If no plateau is found, it restores the starting level. The automatic test is limited to 15 seconds.
- **TUNE** and **AUTO ALC** ask for confirmation before keying the transmitter. **NO** is selected by default.
- Tone tests temporarily select audio CW and enable BK-IN, then restore the previous settings when the test ends. Use VFO A in CW mode with SPLIT off and select the radio's USB TX audio output.

### Contest macros and logging

- Added **CONTEST** to the full-screen macro profiles, with six starter macros.
- Set the fixed exchange **{EXCH}** and next serial **{COUNT}** directly in the contest row. Use the minus and plus buttons or type the serial.
- Successful contest macros fill **EXCH SENT**. The serial advances after saving a new QSO containing the transmitted serial for that callsign.
- Added **EXCH RCVD** and **EXCH SENT** to the QSO Logger and to the quick logger in CONTEST mode.
- ADIF export and Log4OM2 forwarding include the exchange as **SRX_STRING** and **STX_STRING**, plus **STX** for a transmitted serial.

### Updating

Close MorseCONSOLE and run the Windows x64 installer over the existing version. Settings, registration, macros and QSO data are preserved. You can skip driver installation if the radio already connects correctly.

## MorseCONSOLE 0.262 — Changes since 0.257

### AUTO replies

- Manual edits to an **AUTO** reply are preserved while the decoder continues receiving text.
- **SEND** transmits the reply currently on screen. Click **AUTO** again to replace it with the latest suggestion.

### Signal meter and callsign lookup

- The header displays an **S-meter** during reception and switches to **POWER** and **SWR** during transmission.
- Signal strength is displayed as **S0–S9**. Readings above S9 are shown in dB, with markers at **S9**, **+20**, **+40**, and **+60**.
- The [**QRZ.COM**](https://www.qrz.com/) button opens the profile for the callsign entered in **DX CALL** in your browser.

### Multi-monitor display settings

- Under **Settings → DISPLAY**, choose **Automatic** (default) or **Fit to monitor**.
- **Fit to monitor** lets you adjust each of the four screen margins independently from **0 to 128 px**. Margin settings are saved separately for each monitor.
- **APPLY** updates an already maximized window immediately. **RESET** returns all four margin sliders to **0 px**.
## MorseCONSOLE 0.257 — Changes since 0.250

### Macro improvements

- Added an editable **RST** field after **DX CALL** in the full-screen QSO layout. Select a preset or enter a report manually.
- Added `{RST}` to macro templates and editor suggestions.
- The outgoing RST is remembered between sessions. Clicking a decoded report does not change it or the macro templates.
- Updated the default QSO report macro to use `{RST}`, while preserving custom templates.
- Improved **EXCH** positioning in the CWT layout.

### Logger improvements

- **RCVD** and **SENT** now support both preset selection and manual entry in the quick logger and the Logger window.
- Removed **ADVANCED RST** and the expanded report list.

### Spectrum controls

- Added CAT-controlled **CENTER** and **CURSOR** buttons below the VFO controls in full-screen mode.

### Updating

Install over the existing version. Configuration, registration, custom macros and QSO data are preserved.

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
