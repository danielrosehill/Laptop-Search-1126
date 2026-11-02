# Brief

## Request (verbatim, 2026-11-02)

> Okay, could you save the transcript into the repo? Raw cleaned up one and requirements, and then do some research, save research, ultimately we want to get a PDF and we just wanted this is just like a demo. It's the reason it's public because it's a demo example of voice notes through to AI agent conducted research through to produced research in PDF format, which is a pipeline I've used frequently but it's just another demo of it.

## Central question

Which laptops on the market in November 2026 best meet the requirements in `requirements.md`,
what would a basic spec and a stretch spec cost, and should he buy in Israel or abroad?

## Sub-questions

1. **Shortlist:** which current 15–16 in laptops meet tier 1 (32–64 GB RAM, 2 TB, eSIM/WWAN,
   Wi-Fi 7, USB-C charging, a durable keyboard), and what are their configurations?
2. **Compute for local AI on Linux:** which CPUs, iGPUs and NPUs (AMD Ryzen AI, Intel Core Ultra,
   others) run CPU/iGPU ASR (Paraformer via sherpa-onnx/ONNX Runtime) and small local agent models
   best on Ubuntu, and is NPU support on Linux usable yet? Also how well each shortlisted platform
   runs Ubuntu with KDE.
3. **Keyboard, repairability and docking:** which laptops give extra programmable keys (macro
   pads or input modules), user-replaceable RAM/SSD (SODIMM, LPCAMM2, two M.2 slots), good
   repair and parts scores, and dependable Thunderbolt/USB4 docking with two external displays?
4. **Prices and channel:** what the shortlisted configurations cost in Israel (KSP, Ivory, Bug,
   official importers) against manufacturer list prices, and how warranties work for a laptop
   bought in the US and used in Israel.

## Scope

- In: laptops on sale or announced for sale by 2026-11-02, 15–16 in.
- Out: gaming laptops, Macs (Ubuntu is a requirement), Chromebooks.
- Geography: buyer in Israel; may buy in the US while visiting.
- Prices: in ILS where possible, USD list prices with their source date.

## Assumptions

- Price research egresses from Israel. Live US street prices can't be fetched reliably, so
  manufacturer US list prices are given as list prices with dates, not as what he would pay.
- "eSIM" means a WWAN/5G module with eSIM support. A configuration without WWAN fails tier 1.
