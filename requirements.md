# Laptop requirements (from the 2026-11-02 voice note)

Source: `voice-notes/2026-11-02_laptop.cleaned.md` (recorded 2026-11-02). Extracted by Claude Code
(claude-opus-5-5). Tiers follow the note: tier 1 = core, tier 2 = nice to have, tier 3 = stretch.

## Context

- Replacing a Lenovo ThinkPad E15 (AMD, 16 GB RAM, 0.5–1 TB SSD). Arrow keys and trackpad are faulty.
- Mostly a desktop user, but has worked mainly on the laptop for six months.
- OS: Ubuntu with KDE Plasma; installs his own OS, so a preinstalled Linux is worth nothing extra.
- Typical load: 4–8 Claude Code sessions side by side in Konsole, Python runs, browser, occasional
  VS Code, Audacity, GIMP, light Kdenlive, a rarely used Windows VM.
- Near-constant dictation with a local ASR model (his own Paraformer fine-tune, run on CPU).
- Wants it to last 3–5 years.
- Budget: none fixed. He wants a basic spec and a stretch spec with prices, then a number for the
  family budget. If two options are equal on spec, choose the more repairable brand.

## Tier 1: core requirements

| # | Requirement | Note |
|---|---|---|
| 1 | RAM 32 GB minimum, 64 GB preferred | RAM prices are high in 2026, so whether upgradable or soldered matters |
| 2 | Storage 2 TB | current drive keeps running out |
| 3 | CPU (and iGPU/NPU) that runs local ASR quickly | Paraformer on CPU now; a local agent model would be a bonus |
| 4 | 15.6–16 in screen | current size is fine |
| 5 | Integrated eSIM / cellular | has to be designed in at the motherboard level, so choose it at purchase |
| 6 | Extra programmable keys (about 6) | tap-to-talk/PTT, retake, delete, send, a Claude Code key |
| 7 | Wi-Fi 7 and Bluetooth | |
| 8 | USB-C charging | |
| 9 | Works well with a docking station | Ethernet and extra ports via the dock rather than built-in |
| 10 | Durable keyboard and trackpad | the ThinkPad E15 failed here |

## Tier 2: nice to have

- A decent webcam for video calls (not necessarily 4K).
- A good built-in microphone (beamforming array) for ASR.
- A keyboard backlight (no RGB), for typing at night.
- Decent battery life.
- Repairability, spare-parts availability and upgradability.
- Two external displays (HDMI or DisplayPort/USB-C alt mode).
- Enough ports; built-in Ethernet is not required.

## Tier 3: stretch

- Two internal SSD slots (for RAID or backup).
- A discrete or strong integrated GPU (upscaling, light video rendering, local models).
- Built-in NFC (for writing inventory tags).

## Not wanted or not relevant

- RGB lighting. Gaming. Preinstalled Linux.

## Where to buy

1. **Israel:** local warranty, but usually higher prices and a narrower selection.
2. **Abroad (US, on a visit):** wider selection and how the E15 was bought; the warranty may not
   apply in Israel.

## Research outcome (2026-11-02)

Full report: [`research/2026-11-02-laptop-shortlist/Laptop-Search-1126-research-report.pdf`](research/2026-11-02-laptop-shortlist/Laptop-Search-1126-research-report.pdf).

- **Pick:** Lenovo ThinkPad T16 Gen 5. It meets every tier-1 item on Lenovo's PSREF: up to 64 GB
  (Intel, one LPCAMM2) or 96 GB (AMD, two SODIMM), 2 TB, an X61 5G modem with eSIM, Wi-Fi 7 and a
  numeric keypad to remap as macro keys. iFixit scores it 10/10. Runner-up: HP EliteBook 8 G1i 16.
- **Budget line:** ₪12,500 basic (32 GB / 2 TB), ₪16,000 stretch (64 GB / 2 TB), bought in Israel.
- **Before ordering:** confirm the Israeli SKU has the 5G/eSIM module, ask whether the AMD T16 Gen 5 is
  sold in Israel, and test the eSIM on Ubuntu inside the return window.
