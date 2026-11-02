---
title: "Replacing the ThinkPad E15"
subtitle: "Which 16-inch laptop meets the voice-note requirements, what a basic and a stretch spec cost, and where to buy"
kicker: "EXECUTIVE RESEARCH REPORT"
date: 2026-11-02
author: "Claude for Daniel Rosehill"
researched_by: "Claude Code · Opus 5.5 (claude-opus-5-5), agents Sonnet 5.5 (claude-sonnet-5-5)"
started: "2026-11-02 13:34:52 +02:00"
completed: "2026-11-02 13:48:06 +02:00"
sources_count: "33 sources cited (71 logged), accessed 2026-11-02"
method: "4 research agents (claude-sonnet-5-5) in parallel; load-bearing claims checked against the cited pages by the orchestrator"
requested_by: "Daniel Rosehill, for Laptop-Search-1126 (a public demo of voice note → agent research → PDF)"
abstract: |
  The Lenovo ThinkPad T16 Gen 5 is the best fit. It is the only model whose manufacturer spec sheet confirms every core requirement: 64 GB, 2 TB, a 5G modem with eSIM, Wi-Fi 7, USB-C charging, a numeric keypad to remap as macro keys, and a 10/10 iFixit repairability score. A basic spec (32 GB, 2 TB) costs about ₪11,200–12,400 in Israel today: a 32 GB / 1 TB unit from Zap's listings plus a 2 TB SSD fitted locally. A stretch spec (64 GB, 2 TB) costs about ₪15,000–20,500, depending on whether the two-slot AMD version is sold in Israel. Buy in Israel. Once Israeli VAT is added, US list prices come to about the same, and Lenovo's international warranty only covers machine types that are also sold in Israel. Budget ₪12,500 for the basic spec and ₪16,000 for the stretch spec. Confirm before ordering that the chosen Israeli SKU actually has the 5G/eSIM module.
---

# Bottom line

**Buy a ThinkPad T16 Gen 5 in Israel, and budget ₪12,500 for the basic spec or ₪16,000 for the stretch spec.** Confidence is medium. The specs come from Lenovo's own spec sheets, which I checked directly [1][2]. The prices are reseller asking prices on Zap from one day [3][4]. Four things would change the answer:

- **5G/eSIM availability.** If no Israeli T16 Gen 5 SKU comes with the 5G/eSIM module, the choice moves to the HP EliteBook 8 G1i 16. HP's spec sheet confirms the module, but it must be chosen at purchase [5].
- **The AMD version.** If the T16 Gen 5 AMD (two SODIMM slots) is sold in Israel, it is the better buy. RAM can then be added later, without replacing the single LPCAMM2 module the Intel version has [2][1].
- **Local LLMs.** If running local models of 30B parameters or more becomes a real goal, neither machine is enough. That needs an AMD Strix Halo laptop with up to 128 GB of unified memory, which this research did not price [6].
- **Framework.** If Framework starts shipping to Israel with a cellular option, the Framework Laptop 16 becomes the best match on macro keys and repairability. Neither is the case now [7].

# Key findings

| Finding | Confidence | Sources |
|---|---|---|
| The ThinkPad T16 Gen 5 meets every tier-1 item on Lenovo's spec sheet: up to 64 GB (Intel) or 96 GB (AMD), a 2 TB SSD, an X61 5G modem with eSIM, Wi-Fi 7 and a numeric keypad | High | [1][2] |
| T16 Gen 5 repairability is 10/10 on iFixit, the same as Framework. Keyboard replacement is "best-in-class", and Lenovo sells parts | High | [8][9] |
| Israel, 32 GB / 1 TB T16 Gen 5: from ₪9,687 (11 shops). No 16-inch business laptop is sold with 2 TB, so the 2 TB SSD (from ₪1,536) is an upgrade | Medium | [3][10][4] |
| The nearest 64 GB model in Israel is the ThinkPad P16s Gen 5 (64 GB / 1 TB) at ₪18,012–18,960. The Dell Pro 5 Series 16 (64 GB / 1 TB) is ₪13,894, but has no confirmed WWAN | Medium | [4][11] |
| US list price for a 32 GB / 1 TB T16 Gen 5 is \$2,609, about ₪9,630 with 18% Israeli VAT, which is close to the Israeli price | Medium | [12][13][14] |
| Local ASR (Paraformer) needs no NPU: it runs at real-time factor 0.08–0.2 on 1–2 CPU threads. For local LLMs, memory bandwidth and RAM size matter, not NPU TOPS | Medium | [15][6] |
| eSIM on Linux is not guaranteed. Lenovo supports WWAN on Linux per module and per system, and eSIM support through ModemManager is reported as rough | Medium | [16] |
| Framework Laptop 16 has QMK macro-pad modules but no cellular option, and no confirmed shipping to Israel | Low | [17][7] |

# Findings

## The shortlist

**The ThinkPad T16 Gen 5 is the only model whose spec sheet confirms every core requirement. The HP EliteBook 8 G1i 16 is the runner-up.** I opened both Lenovo spec sheets myself on 2026-11-02 (PSREF, Lenovo's product specifications reference):

- **Intel version.** It has one LPCAMM2 slot taking up to 64 GB and one M.2 2280 PCIe 5.0 SSD of up to 2 TB [1].
- **AMD version (Ryzen AI PRO 400, "Gorgon Point").** It has two DDR5 SODIMM slots taking up to 96 GB, and up to 2 TB [2].
- **Both versions.** They list a "Snapdragon X61 5G Modem-RF System … with embedded eSIM functionality", a spill-resistant 6-row keyboard with a numeric keypad, Wi-Fi 7, a 5 MP camera, a dual-microphone array and an optional keyboard backlight [1][2].
- **US availability.** The Intel version is the only one sold in North America [18].

| Model | RAM (max, type) | 2 TB | 5G eSIM | Notes | Verdict |
|---|---|---|---|---|---|
| ThinkPad T16 Gen 5 Intel | 64 GB, 1× LPCAMM2 | Yes | Yes (X61) | numpad; iFixit 10/10 | **Basic pick** |
| ThinkPad T16 Gen 5 AMD | 96 GB, 2× SODIMM | Yes | Yes (X61) | numpad; RAM upgradable | **Stretch pick, if sold in Israel** |
| ThinkPad P16s Gen 5 (AMD/Intel) | 96 GB, LPCAMM2 | Yes | Yes (X61) | stronger CPU/GPU; Ubuntu preload option | Stretch alternative, expensive |
| HP EliteBook 8 G1i 16 | 64 GB, 2× SODIMM | Yes | Yes (T700), at purchase only | backlit DuraKey keyboard | Runner-up |
| Dell Pro 16 Plus | 32 GB with 5G (as shown) | not shown | Yes (tray) | 64 GB + 5G not seen on Dell's store | Basic only |
| ThinkPad P16 Gen 3 | 192 GB, 4× SODIMM | 3 M.2 slots | Yes (RW350R) | 2.54 kg workstation | Over-spec |
| Framework Laptop 16 | 96 GB, 2× SODIMM | 2 M.2 slots | **None found** | QMK macro pad modules | Fails eSIM |

Sources: [1][2][19][20][21][5][22][23].

No spec sheet shows 64 GB, 2 TB and 5G as one orderable SKU. Each appears as a separate option, so ordering all three together is inferred, not confirmed [1]. HP states that WWAN-ready hardware "must be selected at purchase" [5].

## Compute for local AI on Linux

**Any current 8–12-core Intel or AMD laptop CPU handles the ASR workload. RAM, not the NPU, decides what local agents can run.** Paraformer int8 in sherpa-onnx runs at a real-time factor of 0.073–0.195 on one or two threads [15]. I found no Paraformer route on any NPU.

NPUs are usable on Linux, but only narrowly:

- **AMD.** AMD's Ryzen AI software supports only an NPU flow, only on Ubuntu 24.04 [24].
- **Intel.** Intel's NPU driver supports OpenVINO on Ubuntu 24.04 and 26.04 [25].
- **Snapdragon X2.** It is not ready for Ubuntu: Wi-Fi, audio and the webcam fail out of the box [26].

For local LLMs, token speed follows memory bandwidth. A community llama.cpp table shows Strix Halo at about twice Strix Point's text-generation speed on a 7B model: about 52–54 tokens/s against 22–24 [6]. That table is undated and doesn't give the test hardware. Strix Point/Gorgon Point and Panther Lake suit 7–14B models.

From those figures I infer that 32 GB is the floor. 64 GB is the practical size for 14–30B models alongside 4–8 Claude Code sessions and a VM.

Both T16 Gen 5 platforms run Ubuntu 26.04 well. Lenovo warns that WWAN may not work on Linux [27]. Its Linux WWAN enablement is per module and per system, and it requires ModemManager 1.22+ [16].

## Macro keys, repairability and docking

**Remap the T16's numeric keypad as macro keys. For dedicated keys, add a small QMK/VIA macro pad.** The keypad is confirmed on both T16 Gen 5 spec sheets [1][2].

- **Remapping.** keyd remaps keys at the evdev level, so it works on both Wayland and X11, and it supports layers, tap/hold actions and macros [28]. Input Remapper is a GUI alternative packaged in Ubuntu [29]. Either covers PTT, retake, delete, send and a Claude Code key.
- **Framework.** It is the only laptop with built-in modular QMK macro keys [17], but it fails the eSIM requirement.

Repairability:

- **ThinkPad T16 Gen 5.** iFixit scored it 10/10 in 2026 [8]. iFixit also rates its keyboard replacement "best-in-class" and notes that Lenovo sells parts and publishes repair guides [9].
- **ThinkPad E series.** The E16, from the same family as the failed E15, has its keyboard bonded into the top case, which makes it harder to replace [9]. That fits the E15's history.
- **RAM prices.** RAM is expensive in late 2026: loose 32 GB DDR5 SODIMMs cost about \$15–16.50 per GB, and prices rose 24% in six weeks [30]. Israeli 32 GB modules cost ₪1,589–2,444 [4]. A second SODIMM slot (AMD T16) keeps a later upgrade cheap. The single LPCAMM2 slot (Intel T16) means replacing the module.

Docking:

- **Recommended docks.** The Dell WD22TB4 and the Lenovo 40B0 Thunderbolt 4 dock are the best documented on Linux, with fwupd firmware updates [31].
- **Display technologies.** MST docks need no driver. DisplayLink docks need the evdi module and don't work with proprietary GPU drivers [32].
- **AMD hosts.** No test covered an AMD laptop with Ethernet and two displays.

## Prices and where to buy

**Buy in Israel. The US saves little once VAT is paid, and it puts the warranty at risk.**

| Spec | Configuration (Israel, Zap, 2026-11-02, incl. VAT) | Cost |
|---|---|---|
| Basic | T16 Gen 5 21WT0061IV, Core Ultra 7 355, 32 GB / 1 TB, from ₪9,687–10,829, + Samsung 990 Pro 2 TB from ₪1,536 | **₪11,200–12,400** |
| Stretch A (if the AMD T16 is sold here) | an AMD T16 Gen 5 32 GB configuration (price not found; assumed similar to Intel) + 32 GB SODIMM ₪1,589–2,444 + 2 TB SSD | **≈ ₪13,000–15,000 (inferred)** |
| Stretch B (available now) | P16s Gen 5 21XE005FIV, 64 GB / 1 TB, RTX PRO, ₪18,012–18,960, + 2 TB SSD | **₪19,500–20,500** |
| Stretch C (cheapest 64 GB) | Dell Pro 5 Series 16, 64 GB / 1 TB, ₪13,894 (WWAN not stated), + 2 TB SSD | **≈ ₪15,400** |

Sources: [3][11][4].

- **Basic option with confirmed WWAN.** The ThinkPad T16 Gen 4 21QE0043IV (32 GB / 1 TB) is listed with 4G LTE, from ₪9,350 [3]. It is the only Israeli listing found that names a cellular modem.
- **US prices.** Lenovo US lists a 32 GB / 1 TB T16 Gen 5 at \$2,609 [12]. That is ₪8,162 at 3.1284 ₪/$ [13], or ₪9,631 with 18% VAT [14]. The US and Israeli configurations differ, so no like-for-like saving was measured.
- **Warranty.** Lenovo's International Warranty Service covers a machine only where its machine type is sold and supported, and for the country-of-origin term, often one year in the US [33]. The Dell and HP evidence is forum-level.
- **Framework.** It had not launched in Israel as of the only source found (2023) [7].

# Implications for this project

- `requirements.md`: I've added the options and price ranges above under a "Research outcome" heading. The tiers stay as recorded.
- **Budget line for the family budget:** ₪12,500 for the basic spec, ₪16,000 for the stretch spec.
- **Before ordering:**
  1. Ask the Lenovo Israel importer or reseller whether the SKU includes the X61 5G module, and whether a T16 Gen 5 AMD SKU is sold in Israel.
  2. Check the machine type on Lenovo's IWS lookup if buying abroad.
  3. Test the eSIM on Ubuntu early, inside the return window.

# Open questions

- Does any Israeli T16 Gen 5 SKU include 5G/eSIM? Zap titles don't say [3].
- Is the T16 Gen 5 AMD sold in Israel, and at what price?
- What do KSP, Ivory and Bug charge? KSP blocked fetches, and Zap aggregates only part of the market.
- Is the US street price (with Lenovo coupons) meaningfully below list? There is no US egress to check it.
- Does an eSIM profile from an Israeli carrier work through ModemManager on this modem?
- Strix Halo laptops, for 30B+ local models, were not priced.

# Sources

1. Lenovo PSREF: ThinkPad T16 Gen 5 (Intel) spec PDF — Lenovo, 2026-09-21. https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_T16_Gen_5_Intel/ThinkPad_T16_Gen_5_Intel_Spec.pdf. Accessed 2026-11-02.
2. Lenovo PSREF: ThinkPad T16 Gen 5 (AMD) spec PDF — Lenovo, 2026-09-23. https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_T16_Gen_5_AMD/ThinkPad_T16_Gen_5_AMD_Spec.pdf. Accessed 2026-11-02.
3. Zap search results "thinkpad t16 gen 4" and "thinkpad t16 gen 5" — Zap, 2026-11-02 (live). https://www.zap.co.il/search.aspx?keyword=thinkpad+t16+gen+5. Accessed 2026-11-02.
4. Zap search results "990 PRO 2TB", "DDR5 SODIMM 32GB", "thinkpad p16s 64GB" — Zap, 2026-11-02 (live). https://www.zap.co.il/search.aspx?keyword=DDR5+SODIMM+32GB. Accessed 2026-11-02.
5. QuickSpecs HP EliteBook 8 G1i 16 inch Notebook AI PC, v21 — HP, 2026-08-18. https://www8.hp.com/h20195/V2/GetPDF.aspx/c09097612. Accessed 2026-11-02.
6. Performance of llama.cpp with Vulkan #10879 — ggml-org/llama.cpp GitHub discussion, rolling. https://github.com/ggml-org/llama.cpp/discussions/10879. Accessed 2026-11-02.
7. Ordering laptops in Israel? — Framework Community, 2023-08-08. https://community.frame.work/t/ordering-laptops-in-israel/35126. Accessed 2026-11-02.
8. 10/10 from iFixit: Lenovo ThinkPad T14 G7 and T16 G5 star with Framework Laptop-matching repairability — Notebookcheck, 2026-03-10. https://www.notebookcheck.net/10-10-from-iFixit-Lenovo-ThinkPad-T14-G7-and-ThinkPad-T16-G5-star-with-Framework-Laptop-matching-repairability.1246676.0.html. Accessed 2026-11-02.
9. Laptop Repairability Scores — iFixit, 2026 (page current at access). https://www.ifixit.com/repairability/laptop-repairability-scores (fetched by curl). Accessed 2026-11-02.
10. Zap search results "thinkpad x1 carbon", "thinkpad 2TB", "laptop 64GB 2TB 16" — Zap, 2026-11-02 (live). https://www.zap.co.il/search.aspx?keyword=thinkpad+2TB. Accessed 2026-11-02.
11. Zap search results "dell pro 16" and "dell pro max 16" — Zap, 2026-11-02 (live). https://www.zap.co.il/search.aspx?keyword=dell+pro+16. Accessed 2026-11-02.
12. ThinkPad T16 Gen 5 Intel (16") models and configurator (21WT0068US, 21WTCTO1WWUS2) — Lenovo US store, 2026-11-02 (live). https://www.lenovo.com/us/en/p/laptops/thinkpad/thinkpadt/lenovo-thinkpad-t16-gen-5-16-inch-intel/len101t0158. Accessed 2026-11-02.
13. ECB reference rates via fx tool (USD base) — European Central Bank, 2026-10-30. https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html. Accessed 2026-11-02.
14. Israel VAT rate increase to 18% from January 1, 2025 — Sovos, 2024. https://sovos.com/regulatory-updates/vat/israel-vat-rate-increase-to-18-from-january-1-2025/. Accessed 2026-11-02 (search snippet only).
15. Paraformer models (offline) — sherpa-onnx documentation, k2-fsa, undated. https://k2-fsa.github.io/sherpa/onnx/pretrained_models/offline-paraformer/paraformer-models.html. Accessed 2026-11-02.
16. lenovo/lenovo-wwan-unlock README — GitHub (Lenovo), undated. https://github.com/lenovo/lenovo-wwan-unlock. Accessed 2026-11-02.
17. FW 16 Keyboard VIAL support (ISO/ANSI/Macro-/Numpad) — Framework Community, undated. https://community.frame.work/t/fw-16-keyboard-vial-support-iso-ansi-macro-numpad/51411.md. Accessed 2026-11-02.
18. Lenovo releases new 16-inch laptop in North America with LPCAMM2 RAM and Intel Panther Lake — Notebookcheck, 2026-05-12. https://www.notebookcheck.net/Lenovo-releases-new-16-inch-laptop-in-North-America-with-LPCAMM2-RAM-and-Intel-Panther-Lake.1294606.0.html. Accessed 2026-11-02.
19. Lenovo PSREF: ThinkPad P16s Gen 5 (AMD) spec PDF — Lenovo, 2026-09-14. https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_P16s_Gen_5_AMD/ThinkPad_P16s_Gen_5_AMD_Spec.pdf. Accessed 2026-11-02.
20. Lenovo PSREF: ThinkPad P16s Gen 5 (Intel) spec PDF — Lenovo, 2026-10-21. https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_P16s_Gen_5_Intel/ThinkPad_P16s_Gen_5_Intel_Spec.pdf. Accessed 2026-11-02.
21. Lenovo PSREF: ThinkPad P16 Gen 3 spec PDF — Lenovo, 2026-10-28. https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_P16_Gen_3/ThinkPad_P16_Gen_3_Spec.pdf. Accessed 2026-11-02.
22. Dell Pro 16 Plus with AI and 5G Connectivity (PB16250), Dell US store page — Dell, live 2026-11-02. https://www.dell.com/en-us/shop/laptop-computers/spd/dellproplus16laptoppb16250. Accessed 2026-11-02.
23. Introducing the new Framework Laptop 16 with NVIDIA GeForce RTX 5070 — Framework Community, 2025-08-26. https://community.frame.work/t/introducing-the-new-framework-laptop-16-with-nvidia-geforce-rtx-5070/74547.md. Accessed 2026-11-02.
24. Ryzen AI Software on Linux — AMD Ryzen AI documentation (v1.9.0), undated. https://ryzenai.docs.amd.com/en/latest/linux.html. Accessed 2026-11-02.
25. intel/linux-npu-driver release v1.38.0 — GitHub (Intel), published 11 Sep 2026 (year inferred from build date 20260910). https://github.com/intel/linux-npu-driver/releases/tag/v1.38.0. Accessed 2026-11-02.
26. Snapdragon X2 Performance On Linux Exceeding Expectations In Initial Benchmarks — Phoronix, 2026-10-21. https://phoronix.com/review/snapdragon-x2-linux. Accessed 2026-11-02.
27. Linux auf dem ThinkPad T16 Gen 5 AMD ausprobiert — Notebookcheck, 2026-06-14 (updated 2026-10-05). https://www.notebookcheck.com/Linux-auf-dem-ThinkPad-T16-Gen-5-AMD-ausprobiert.1320640.0.html. Accessed 2026-11-02.
28. keyd: a key remapping daemon for Linux — GitHub (rvaiya/keyd), undated. https://github.com/rvaiya/keyd. Accessed 2026-11-02.
29. Input Remapper — GitHub (sezanzeb/input-remapper), undated. https://github.com/sezanzeb/input-remapper. Accessed 2026-11-02.
30. 32GB DDR5 Laptop RAM: Live SO-DIMM Prices per GB — datacenterdisk.com, 2026-11-02. https://datacenterdisk.com/ram/laptop/ddr5/32gb. Accessed 2026-11-02.
31. Best Thunderbolt Docks for Linux in 2026 — ThunderboltLaptop, updated 2026-10-28. https://thunderboltlaptop.com/best-thunderbolt-docks-work-with-linux/. Accessed 2026-11-02.
32. Best DisplayLink dock for Linux — ComputingForGeeks, 2026-10-27. https://computingforgeeks.com/best-displaylink-dock-linux/. Accessed 2026-11-02.
33. International Warranty Service (IWS) policy, Notebook/Desktop/Workstation — Lenovo Support Israel, undated (read 2026-11-02). https://support.lenovo.com/il/he/solutions/ht505335. Accessed 2026-11-02.
