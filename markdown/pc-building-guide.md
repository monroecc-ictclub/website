# PC Building Guide

A quick reference for choosing parts and putting a PC together. Each section covers what the part does, what to look for, and a recommended pick for most builds.

> **2026 market note:** An AI-driven memory shortage has pushed RAM, SSD and GPU prices well above normal. A 32GB DDR5 kit costs about **$400**, roughly 3–4× what it did in late 2025. Large prebuilt makers locked in parts before the spike, so **a prebuilt can now match or beat a DIY build on price**, especially between $1,000 and $1,900. Price out both before you buy.

---

## Build, Buy, Laptop or Chromebook?

| | **Custom Build** | **Prebuilt** | **Laptop** | **Chromebook** |
|---|---|---|---|---|
| **Upfront cost** | Medium–High | Medium–High (often the best 2026 value) | Medium–Very High | Low |
| **Performance per dollar** | Best (normal market) | Very good | Fair | Fine for light tasks |
| **Portable** | No | No | Yes | Yes |
| **Upgradable** | Fully | Usually, Depends on brand | Barely (SSD, sometimes RAM) | No |
| **Setup effort** | High | Low | Very low | Very low |
| **Gaming** | Excellent | Excellent | Good (gaming models) | Cloud only |
| **Warranty** | Per part | Single vendor | Single vendor | Single vendor |
| **Typical lifespan** | 5–8+ years | 4–7 years | 3–5 years | Until its update expiration date |

- **Build** if you want the most control, easy upgrades and the hands-on learning. Budget for a Windows license, monitor and peripherals too.
- **Buy prebuilt** if you want desktop power without the effort. Check the spec sheet for a quality power supply, **two** RAM sticks and a known-brand SSD, since these are where builders cut corners.
- **Get a laptop** if you need to work in more than one place.
- **Get a Chromebook** for browsing, schoolwork and streaming. It can't run most Windows desktop apps or PC games.

---

## Processor (CPU)

The CPU runs the instructions from the OS, games and apps: game logic, physics, compiling, compression. If it's too slow, the GPU sits idle waiting on it (a "CPU bottleneck").

| Spec | Why it matters |
|---|---|
| **Cores / threads** | More cores help with multitasking, streaming and rendering. Most games gain little past 8. |
| **Clock speed & architecture** | Newer architectures do more per GHz, so a newer chip can beat an older, higher-clocked one. |
| **Cache (L3)** | Games love cache. This is why AMD's **X3D** chips lead in gaming. |
| **Integrated graphics** | Lets you run or troubleshoot without a GPU, saves on power for builds that don't need much in the way of graphics. |
| **Socket** | Decides which motherboards fit and whether you can upgrade later. |

**Tiers:** both brands use a 3 / 5 / 7 / 9 pattern where bigger numbers often mean more powerful chips.

| | **AMD Ryzen 9000 (AM5)** | **Intel Core Ultra 200S / 200S Plus (LGA 1851)** |
|---|---|---|
| **Strengths** | Best gaming (X3D), efficient, socket supported for future CPUs | More cores per dollar, Quick Sync for video/media servers |
| **Weaknesses** | X3D costs more, basic integrated graphics | Behind in top-end gaming |
| **Picks 2026** | Ryzen 5 9600X (budget), Ryzen 7 9700X (mainstream), **Ryzen 7 7800X3D / 9800X3D (gaming)**, Ryzen 9 9950X3D (gaming + work) | Core Ultra 5 250K Plus (~$199), **Core Ultra 7 270K Plus (~$299, 24 cores)**, Core Ultra 9 285K (workstation) |

---

## Motherboard

Everything plugs into the motherboard. It doesn't make games faster. It decides **which parts fit, how many, how fast they connect and how easy upgrades are**.

| Spec | Why it matters |
|---|---|
| **Socket** | Must match your CPU exactly. |
| **Chipset** | Sets the feature tier: overclocking, PCIe generation, USB ports. |
| **Form factor** | **ATX** (standard), **Micro-ATX** (smaller), **Mini-ITX** (tiny). Must fit your case. |
| **M.2 slots** | Fast SSD slots. Some share bandwidth with SATA ports, so read the manual. |
| **Connectivity** | Built-in Wi-Fi, Ethernet speed, USB count. Check the rear ports for what you'll plug in. |
| **BIOS Flashback** | Updates the BIOS without a CPU installed, handy when a new CPU needs a newer BIOS. |

| Platform | Budget | **Sweet spot** | Enthusiast |
|---|---|---|---|
| **AMD AM5** | A620 (avoid B840, it's PCIe 3.0 only) | **B650 / B850** | X870 / X870E |
| **Intel LGA 1851** | H810 | **B860** | Z890 (needed to overclock K-series) |

**The golden rule:** choose the CPU first, then a board with the matching socket, then the cheapest chipset with the features you need. Money saved here does more in other budget areas.

---

## Memory (RAM)

RAM is short-term working space. Programs load from the SSD into RAM so the CPU can reach them instantly. It's wiped when the PC turns off.

**What matters, in order:** enough capacity → two sticks (dual-channel) → speed and latency.

| Capacity | Good for |
|---|---|
| **16GB** | Budget gaming and everyday use. A game plus a browser and Discord can fill it. |
| **32GB (2×16GB)** | **The standard** for gaming, streaming and general use. |
| **64GB (2×32GB)** | Video editing, virtual machines, heavy multitasking. |

- **DDR4 and DDR5 are not interchangeable.** Current AMD and Intel platforms are **DDR5 only**.
- **Speed (MT/s) and CAS latency (CL)** decide real-world speed. Lower CL is better. True latency = CL × 2000 ÷ speed.
- **AMD target:** DDR5-6000 CL30 (CL36 is fine with X3D chips).
- **Intel target:** DDR5-6400 to 7200.
- **Turn on XMP (Intel) or EXPO (AMD) in the BIOS**, or the RAM runs at a slow default speed.
- **Use 2 sticks in slots A2 and B2** (usually the 2nd and 4th from the CPU). Four DDR5 sticks often force lower speeds.
- **Buy one matched kit.** Mixing kits often fails to run at rated speed.

---

## Graphics Card (GPU)

The GPU draws the frames you see. In a gaming PC it matters most for frame rate and is usually the most expensive part. **Choose it to match your monitor:** 1080p is budget, **1440p is the sweet spot**, and 4K needs a high-end card.

| Spec | Why it matters |
|---|---|
| **VRAM** | Running out causes stutter. 8GB is entry-level, 12GB is the minimum for 1440p, 16GB+ is safe for 4K. |
| **Ray tracing** | Realistic lighting at a big performance cost. NVIDIA leads. |
| **Upscaling / frame gen** | DLSS (NVIDIA), FSR (AMD), XeSS (Intel) give big free FPS boosts. |
| **Power draw** | Sets your PSU wattage and power connectors. |
| **Size** | High-end cards can be 300mm+ long and 3+ slots thick. Check the case. |

| Brand | Strengths | Weaknesses | Picks |
|---|---|---|---|
| **NVIDIA RTX 50** | Best ray tracing, DLSS 4, best for AI/creative work (CUDA) | Most expensive, low VRAM on cheaper cards | RTX 5060 Ti 16GB, RTX 5070, **RTX 5070 Ti**, RTX 5080, RTX 5090 |
| **AMD RX 9000** | Best raw FPS per dollar, 16GB VRAM, great Linux drivers | Behind in heavy ray tracing, no flagship | RX 9060 XT 16GB, RX 9070, **RX 9070 XT** |
| **Intel Arc B-series** | Great budget value, 12GB VRAM, strong video encoding | Budget only, needs Resizable BAR on, older games inconsistent | Arc B570, **Arc B580** |

**Recommendation:** RTX 5070 Ti for the best all-rounder, RX 9070 XT for the most FPS per dollar at 1440p, Arc B580 on a tight budget. Avoid 8GB cards if you can.

---

## Storage

Storage keeps the OS, programs and files when the power is off. Faster storage means faster boot and load times, but it barely affects FPS once a game is running.

**The golden rule:** always put the operating system on an **SSD**.

| Type | Speed (read) | Notes |
|---|---|---|
| **HDD** | ~150–280 MB/s | Cheapest per TB. Bulk media and backups only, never the OS drive. |
| **SATA SSD (2.5")** | ~550 MB/s | Good upgrade for older PCs without M.2. |
| **NVMe PCIe 4.0** | ~5,000–7,450 MB/s | **The sweet spot.** Fast and well-priced. |
| **NVMe PCIe 5.0** | ~10,000–14,700 MB/s | 2–3× the price, runs hot, little gaming benefit today. |

- **Capacity:** 1TB for budget builds, **2TB as the starting point** for gaming (games take 100–200GB each). Keep 10–20% free.
- **Budget DRAM-less drives** (Kingston NV3, Crucial P310) are fine for gaming. **DRAM drives** (WD Black SN850X, Samsung 990 Pro) hold up better under heavy use.
- **Peel the plastic film off the M.2 heatsink's thermal pad.** It's a very common mistake.
- **New drive not showing up?** Initialize and format it in Disk Management.
- **Back up with 3-2-1:** 3 copies, on 2 types of storage, 1 offsite or in the cloud.

---

## Operating System

A new build has **no OS**. You install one from a USB stick, and the OS decides what software and games you can run.

| | **Windows 11** | **Linux** |
|---|---|---|
| **Cost** | ~$140 Home / ~$200 Pro | Free |
| **Software** | Runs almost everything | No native Office desktop or Adobe Creative Cloud |
| **Gaming** | Everything works | Most games work through Steam's Proton. Many with kernel anti-cheat (Valorant, Fortnite, CoD) don't. |
| **Updates** | Microsoft decides | You decide |
| **Privacy** | Ads, telemetry, Microsoft account push | No ads, minimal telemetry |
| **Learning curve** | Familiar | Easy on beginner distros, sometimes needs the terminal |

- **Windows 11 needs TPM 2.0 and Secure Boot**, which may need to be turned on in the BIOS.
- **Windows 10 security updates end October 13, 2026.** Upgrade or switch.

| Distro | Difficulty | Best for |
|---|---|---|
| **Ubuntu** (or Mint, Pop!_OS) | Easy | Beginners, developers, the most online help |
| **Debian** | Easy–Moderate | Servers, older hardware, rock-solid stability |
| **Arch** (or CachyOS, EndeavourOS) | Advanced | Newest drivers, gaming, learning how Linux works |
| **NixOS** | Advanced+ | Reproducible setups with built-in rollbacks |

**Before switching a gaming PC to Linux,** check your games on **ProtonDB.com** and **AreWeAntiCheatYet.com**. Try any distro first from a live USB.

---

## Monitor

The monitor sets the ceiling on your whole system. A powerful GPU is wasted on a 60Hz 1080p screen, so **pick the monitor and GPU together**.

| Panel | Strengths | Weaknesses |
|---|---|---|
| **IPS** | Accurate color, wide angles, fast. The best default. | Grayish blacks, "IPS glow" |
| **VA** | Deepest LCD blacks, cheap | Smearing in fast dark scenes |
| **Mini-LED** | Brightest HDR, no burn-in | Halos around bright objects |
| **OLED** | Perfect blacks, near-instant response | Burn-in risk from static elements, higher price |

| Resolution | Ideal size | GPU demand |
|---|---|---|
| **1080p** | 24" | Low |
| **1440p** | 27" | Medium (**the sweet spot**) |
| **4K** | 27–32" | High |

- **Refresh rate:** the biggest jump you'll notice is **60Hz → ~144Hz**. 240Hz is premium, 360Hz+ is for competitive esports.
- **Adaptive sync (G-Sync / FreeSync)** removes screen tearing. Make sure it's on.
- **Use DisplayPort 1.4+ or HDMI 2.1** for high resolution at high refresh rates.
- **HDR400 on a regular LCD is basically marketing.** Real HDR needs OLED or Mini-LED.

**Recommendation:** a **27" 1440p monitor at 165–240Hz**. IPS for value, or a QD-OLED like the MSI MAG 272QP (~$400) if you can stretch.

---

## Peripherals

Peripherals don't affect FPS, but you touch them constantly. **Fit and feel matter more than specs.**

- **Keyboard:** a **TKL or 75% mechanical** keyboard suits most people. Switch feels are **linear** (smooth, popular for gaming), **tactile** (a bump, good for typing) and **clicky** (loud). Competitive FPS players should look at **Hall effect** boards with Rapid Trigger (Wooting 80HE, Razer Huntsman V3 HE).
- **Mouse:** pick **shape and weight for your hand and grip** (palm, claw or fingertip) first. Any modern sensor is fine, and huge DPI numbers are marketing; most players use 400–1600. 2.4GHz wireless is as fast as wired.
- **Headset:** **closed-back** for shared spaces, open-back for a wider sound. Use wired or **2.4GHz wireless**, and never game on Bluetooth audio because of the lag. The HyperX Cloud III (~$80) is the value pick.
- **Cheap upgrades worth making:** a large mousepad, a USB microphone, a monitor arm, and a UPS if your power is unreliable.

---

## Compatibility Checklist

Run through this before you buy:

- [ ] CPU **socket** matches the motherboard (AM5 or LGA 1851).
- [ ] Motherboard **BIOS** supports the CPU, or the board has BIOS Flashback.
- [ ] RAM is **DDR5** (for current platforms), a **matched 2-stick kit**, and short enough to clear the CPU cooler.
- [ ] Motherboard **form factor** fits the case.
- [ ] GPU **length and thickness** fit the case.
- [ ] Power supply has enough **wattage** and the right **GPU power connectors** (8-pin or 12V-2x6).
- [ ] CPU cooler is rated for the CPU's power draw and fits the case.
- [ ] M.2 slot supports the SSD (NVMe vs. SATA, PCIe generation).
- [ ] Monitor resolution and refresh rate match what the GPU can drive.
- [ ] You have an OS (Windows license or Linux USB) and a USB stick to install it from.

## Assembly Order

1. **Build on the motherboard box, outside the case.** Install the CPU (match the arrow to the socket mark and don't force it), then the RAM in A2/B2, then the M.2 SSD.
2. **Mount the CPU cooler.** Check for pre-applied thermal paste, and peel any plastic off the cooler's contact plate.
3. **Install the I/O shield** if it isn't built into the board, then mount the motherboard in the case on its standoffs.
4. **Install the power supply** and route cables to the back of the case.
5. **Connect power:** 24-pin to the motherboard, 8-pin CPU power at the top of the board, and the front-panel connectors (check the manual).
6. **Install the GPU** in the top PCIe slot and plug in its power cables until they're fully seated.
7. **First boot:** plug the monitor into the **GPU**, not the motherboard. The first boot can take a minute or more while DDR5 memory trains. That's normal.
8. **In the BIOS:** confirm the CPU, RAM and SSD are detected, turn on **XMP/EXPO**, and turn on TPM and Secure Boot if you're installing Windows 11.
9. **Install the OS**, then the GPU drivers, then check Task Manager → Performance → Memory to confirm the RAM speed.
