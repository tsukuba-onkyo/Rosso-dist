*[日本語版はこちら / Japanese version](README.md)*

# Rosso — a circuit simulator for guitar effects and audio

A schematic simulator with **1,920 parts** of the kind effects-pedal and tube-amp
builders actually reach for. Draw a circuit and you hear it, right there.

**→ [Overview page](https://tsukuba-onkyo.github.io/Rosso-dist/?lang=en)** ・ **[Download](../../releases/latest)**

## What makes it different

It does not imitate EQ curves. It solves the circuit sample by sample with
**modified nodal analysis (MNA) + Newton's method**. That means the *bad* physical
behaviour of real parts comes through in the sound.

- **180 germanium transistors** — leakage current doubles every 10 °C. A fuzz that
  dies in midsummer heat behaves like one
- **188 vacuum tubes** — asymmetric compression from grid current, charge building up
  in coupling capacitors (blocking distortion)
- **33 BBD devices** — the actual bucket-brigade transfer. Charge is lost at every
  stage, so more stages means a duller sound
- **CdS cells** — pick an LED or an incandescent lamp as the light source. The lamp is
  slowed by its heat capacity, and it cools more slowly than it heats
- **Transformers** — magnetic saturation and residual flux

It can also read a photograph of a schematic and turn it into a circuit, and let you
develop a circuit by talking to an AI (both need a free Google AI Studio API key).

## Language

The interface is available in **English and Japanese**. It follows your system language
on first launch, and the **🌐** button in the toolbar switches it at any time.
Part names, categories, pin names and preset names are all translated — but part
numbers such as `2SK117` or `MN3007` stay as they are, because they are also search keys.

## Download

Grab the one for your platform from [Releases](../../releases/latest).

| File | For |
|---|---|
| `Rosso_x.y.z_x64-setup.exe` | Windows 64-bit (installer, recommended) |
| `Rosso_x.y.z_x64_en-US.msi` | Windows 64-bit (MSI) |
| `Rosso_x.y.z_aarch64.dmg` | macOS (Apple Silicon) |

When a new version is out, the app tells you at startup.

### About the warning on first launch

The installers are not code-signed, so macOS shows a Gatekeeper warning and Windows
shows a SmartScreen warning. On macOS, right-click → **Open**. On Windows, click
**More info** → **Run anyway**.

### If macOS says *"Rosso" is damaged and can't be opened*

**This is a bug in macOS builds up to v1.3.4. The app is not damaged** — the signature
was inconsistent, and v1.3.5 fixed it.

Right-click → Open does **not** get past this particular message. Run the following in
Terminal first, then open the app:

```
xattr -cr /Applications/Rosso.app
```

Reinstalling v1.3.5 or later avoids it entirely. Sorry for the trouble.

## Known limitations

- **The amplifier simulator is currently disabled.** A model with two stacked tube
  stages produces intermittent noise. The cause is identified, and it will be enabled
  again once fixed
- The simulation approximates real behaviour. Building or modifying real hardware is at
  your own risk — the high voltages in tube circuits are genuinely dangerous

## Bugs and requests

Please open an [issue](../../issues). Steps to reproduce help a lot, and a circuit file
(JSON) helps even more.

## Licence

Rosso itself is proprietary (all rights reserved). It is free for personal use.
Bundled third-party components are covered by their own licences — the full texts are
available from "License information" inside the app.

© 2026 Tsukuba Onkyo (筑波音響)
