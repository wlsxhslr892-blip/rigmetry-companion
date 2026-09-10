# Rigmetry Companion for Windows

Rigmetry Companion sends supported Windows PC hardware telemetry to the Rigmetry Android app over your local network.

## Quick start

1. Download **Rigmetry-Companion-Windows.zip** from this repository's **Releases** page.
2. Extract the entire ZIP to a folder on your Windows PC.
3. Run **Rigmetry Companion.exe**.
4. If Windows Firewall asks, allow **Private networks** on your trusted local network. Keep the firewall enabled.
5. Connect your Android phone and PC to the same router/Wi-Fi. A wired PC on the same router is supported.
6. Open Rigmetry on Android and select your PC.
7. Compare the PC identity codes on both screens, then complete pairing with the six-digit PIN shown on the PC.

No Rigmetry account or developer-operated cloud telemetry server is required.

## Requirements

- Windows 10/11 x64
- Rigmetry Android app
- PC and Android device on the same local network

The portable package includes its .NET runtime. A separate .NET installation is not required. Sensor availability depends on the PC and its drivers; unsupported readings remain unavailable.

## Open and exit

- **X** hides the window to the system tray while monitoring continues.
- Run the EXE again to reopen the existing window.
- Use **Exit** in the window or tray menu to stop the companion completely.
- After a full restart, the phone may need to pair again using the current PIN.

## Security

Pairing uses PIN verification and TLS. Compare the PC identity codes before pairing. Never ignore a certificate mismatch, expose the companion port to the internet, or share private keys.

Only download the Companion from this official repository. The release includes a SHA-256 checksum file for the ZIP.

This initial Windows EXE is **not code-signed**; Windows may display a reputation warning. Do not disable Windows security or ignore a malware detection to run it.

If startup fails, the app displays an error rather than resetting your PC identity. A bounded local startup diagnostic may be written to `%LOCALAPPDATA%\ProjectC\logs\last-startup-error.txt`. It contains no PIN, pairing token or private key, and is not uploaded automatically.
