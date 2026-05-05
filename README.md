# Nocturne Alchemy Firmware Loader

**Web-based firmware flasher for all Nocturne Alchemy Platform modules**  
*FlatSix Modular*  
*Hosted via GitHub Pages*

---

## What Is This?

This repository hosts the web firmware loader for the [Nocturne Alchemy Platform](https://flatsixmodular.com/) by FlatSix Modular. It allows users to flash firmware directly from their browser (Chrome on Mac or PC) without needing the Arduino IDE.

The loader supports all current Nocturne Alchemy Platform firmwares:

- **Slight Of Hand** — CV keyboard, 4 octaves, portamento
- **Arp Of Darkness** — Buffer arpeggiator with Golden Ratio playback
- **Seventh Summoner** — 6-channel multi-sequencer with meta-sequencer layer
- **Shroud Of Turing** — Generative shift register sequencer with musical quantization

---

## Live Pages

| Page | URL | Purpose |
|---|---|---|
| Stable | https://seanrieger.github.io/nocturne-alchemy-firmware-loader/ | Current stable firmware for all modules |
| Beta | https://seanrieger.github.io/nocturne-alchemy-firmware-loader/beta.html | Beta firmware for testing |

---

## How It Works

The loader uses [arduino-web-uploader](https://github.com/dbuezas/arduino-web-uploader) by dbuezas. Compiled `.hex` files for each firmware version are stored in the `uploader/` folder and referenced directly by the HTML pages.

### Requirements for Users
- Google Chrome on Mac or PC
- USB-A to USB Mini cable
- Nocturne Alchemy Platform module unplugged from Eurorack power

---

## Repository Structure

```
nocturne-alchemy-firmware-loader/
├── index.html          ← Stable firmware flasher (GitHub Pages root)
├── beta.html           ← Beta firmware flasher
├── uploader/
│   ├── *.hex           ← Compiled firmware hex files for all modules
│   └── *.svg           ← Module panel images
└── README.md
```

---

## Adding a New Firmware Version

1. Compile the firmware in Arduino IDE — the `.hex` file is in the `build/arduino.avr.nano/` folder
2. Copy the `.hex` file into `uploader/` with a clear version name
3. Update `index.html` or `beta.html` to reference the new file
4. Commit and push — GitHub Pages updates automatically

---

## Credits

Web flashing powered by [arduino-web-uploader](https://github.com/dbuezas/arduino-web-uploader) — © dbuezas.

---

*Nocturne Alchemy Firmware Loader — FlatSix Modular — 2026*
