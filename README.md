# Rigmetry Companion for Windows

Rigmetry Companion is required to connect the Rigmetry Android app to a Windows PC and provide supported hardware telemetry over your local network.

## Download

On your **Windows PC**, open the [latest release](https://github.com/wlsxhslr892-blip/rigmetry-companion/releases/latest) and download **Rigmetry-Companion-Windows.zip**. The Windows ZIP is not an Android app.

## Quick start

1. Download **Rigmetry-Companion-Windows.zip**.
2. Extract the entire ZIP to a folder on your Windows PC.
3. Double-click **Rigmetry Companion.exe**.
4. If Windows Firewall asks, allow **Private networks** on your trusted local network. Keep the firewall enabled.
5. Keep Rigmetry Companion running.
6. Connect your Windows PC and Android phone to the same router / Wi-Fi. A wired PC on the same router is supported.
7. Open Rigmetry on Android.
8. Select your PC.
9. Compare all four PC identity code groups on both screens.
10. Only if they match, complete pairing with the six-digit PIN shown on your PC.

No Rigmetry account or developer-operated telemetry cloud is required.

## Requirements

- Windows 10/11 x64
- Rigmetry for Android
- PC and phone on the same local network

The portable package includes its .NET runtime; no separate .NET installation is required. Supported readings depend on the PC and its drivers. Unsupported readings remain unavailable, not zero.

## Troubleshooting

If no PC appears:

- Confirm that Rigmetry Companion is running.
- Confirm that your PC and phone use the same local network, not an isolated guest Wi-Fi.
- Check Windows Firewall Private-network permission on your trusted network.
- Try **Manual Address** in the Android app with the PC's IPv4 address.

## Open and exit

- **X** hides the window to the system tray; monitoring continues.
- Run the EXE again to reopen the existing window.
- Use **Exit** in the window or tray menu to stop completely.
- After a full restart, the phone may need to pair again using the current PIN.

## Security

Pairing uses PC identity verification, PIN pairing and TLS. Do not ignore an identity mismatch, expose the Companion port to the internet, or share private keys.

Only download the Companion from this official repository. A SHA-256 checksum is included with each Windows ZIP.

The Windows EXE is **not code-signed**; Windows may display an unknown-publisher or reputation warning. Do not disable Windows security or ignore a malware detection to run it.

If startup fails, the app displays an error instead of resetting the PC identity. A bounded local diagnostic may be written to `%LOCALAPPDATA%\ProjectC\logs\last-startup-error.txt`. It contains no PIN, token or private key and is not uploaded automatically.
