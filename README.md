# Jaspp

### Your Mac, beautifully in control.

Jaspp brings the everyday controls of your Mac into one elegant menu bar companion. Shape its cooling, tune your displays, guide your music, and reach your desktop from another device on the same network.

## A quieter rhythm. A clearer workspace.

- **Cooling with intention.** Monitor fan speeds and temperatures, choose a preset, or create a temperature-based fan curve.
- **Your desktop, within reach.** Control your Mac from a browser on a trusted local network, with a pairing token to protect access.
- **Light, balanced.** Adjust built-in and compatible external displays, with brightness and display power controls in one place.
- **Sound, uninterrupted.** Manage system volume and Apple Music playback without breaking your flow.
- **Everyday essentials.** Lock your Mac, turn off its screen, or request a normal shutdown from the remote interface.
- **A place to compose.** Write emails with attachments through a local workspace connected to your own Resend account.

## Get Jaspp

Download **[Jaspp for Apple Silicon](https://github.com/SASAMITTRRR/Jaspp/releases/latest)**, open the disk image, and drag **Jaspp.app** into **Applications**.

**Requirements:** Apple Silicon, macOS 14 or later, and `/usr/bin/python3`, available with Xcode Command Line Tools. External display controls require a compatible DDC-enabled display.

The app uses ad-hoc code signing and is not notarized by Apple. macOS may require you to allow it in **System Settings → Privacy & Security** when opening it for the first time.

## Designed around your setup

Jaspp keeps its configuration on your Mac. This distribution ships without personal mail records, API keys, saved pairing tokens, or a preset sender domain. A separate data directory gives it a fresh start.

Fan control requests administrator permission to install its helper. Local network and automation permissions depend on the features you use. Email requires your own Resend API key and a verified sender domain. Use the remote interface on a trusted network.

## Build your own

Download and extract **`Jaspp-1.2.1-source.zip`**, then run the following commands inside `Jaspp-source`:

```sh
bash build.sh
```

The app is created at `build/Jaspp.app`. The build runs 56 fan-control logic checks. To run the mail configuration tests:

```sh
PYTHONDONTWRITEBYTECODE=1 python3 tests/test_mail.py
```

The source package includes the Swift app, Python service, browser interfaces, build scripts, tests, and third-party notices. The bundled m1ddc license is preserved alongside the component.

---

**Jaspp 1.2.1** · Apple Silicon · Made for the way you use your Mac.
