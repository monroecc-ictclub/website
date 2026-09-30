# PC Building Guide: Memory (RAM)

## What RAM does

RAM (Random Access Memory) is the computer's short-term working space. When you open a program, game or browser tab, its data is loaded from slow storage (the SSD) into fast RAM so the CPU can reach it almost instantly. RAM is **volatile**, which means it's wiped when the PC turns off.

- **Too little RAM** is the most noticeable problem. When memory fills up, Windows starts using the much slower SSD as overflow, which causes stutters, freezes and sluggish app switching.
- **Enough RAM that's also fast** gives a smaller but real boost, mainly to minimum FPS (smoothness) in CPU-heavy games.

**The order that matters:** first **enough capacity**, then **the right configuration (dual-channel)**, then **speed and latency**.

---

## What differs between kits

| Spec | What it means | Why it matters |
|---|---|---|
| **Generation (DDR4 / DDR5)** | The memory standard. They are **not** interchangeable. The notch is in a different place. | Must match the motherboard. Current AMD (AM5) and Intel (LGA 1851) platforms are **DDR5 only**. |
| **Capacity (GB)** | How much data it can hold. | The biggest factor for multitasking and modern games. |
| **Speed (MT/s)** | Transfers per second, such as DDR5-6000. Often mislabeled as "MHz." | Higher speed means more bandwidth. |
| **CAS latency (CL)** | How many clock cycles the RAM takes to respond, such as CL30. Lower is better. | Together with speed, this decides the real-world response time. |
| **Timings** | The full set, such as 30-38-38-96. CL is the first number. | Tighter (lower) timings are faster. Most people only need to compare CL. |
| **Kit configuration** | How many sticks, such as 2×16GB. | **Two sticks gives dual-channel mode**, which roughly doubles bandwidth versus one stick. |
| **XMP / EXPO profile** | A preset overclock stored on the RAM (XMP for Intel, EXPO for AMD). | RAM runs at a slow default speed until you **turn on the profile in the BIOS**. |
| **Ranks / die type** | Single or dual rank, and the memory chip maker (SK Hynix, Samsung, Micron). | Enthusiast detail. SK Hynix chips generally overclock best on DDR5. |
| **CUDIMM** | New DDR5 with a clock driver on the stick. | Enables very high speeds (8000+ MT/s) on Intel Core Ultra. It isn't needed on AMD. |
| **Form factor** | **DIMM** (desktop) or **SO-DIMM** (laptop, smaller). | Must match the device. Many laptops have soldered RAM (LPDDR5X) that **can't be upgraded**. |
| **ECC** | Error-correcting memory. | For servers and workstations. Consumer desktops don't need it. |
| **Heat spreader / RGB height** | Tall sticks with RGB lighting or large heatsinks. | Can hit large air coolers. Check clearance. |

### Working out real latency
Speed and CL together decide how quickly the RAM actually responds:

> **True latency (ns) = CL × 2000 ÷ speed (MT/s)**

| Kit | True latency |
|---|---|
| DDR4-3200 CL16 | 10.0 ns |
| DDR5-6000 CL36 | 12.0 ns |
| **DDR5-6000 CL30** | **10.0 ns** (the sweet spot) |
| DDR5-6400 CL32 | 10.0 ns |
| DDR5-8000 CL38 | 9.5 ns |

DDR5 isn't slower than DDR4. It responds about as fast and has far more bandwidth.

---

## How much RAM do you need?

| Capacity | Good for |
|---|---|
| **8GB** | Basic browsing and office work only. Too little for gaming in 2026. |
| **16GB** | Budget gaming and everyday use. Workable, but modern games plus a browser and Discord can fill it. |
| **32GB (2×16GB)** | **The recommended standard** for gaming, streaming and general use. |
| **64GB (2×32GB)** | Video editing, 3D, virtual machines, large codebases and heavy multitasking. |
| **96–128GB+** | Professional workstations, big datasets and local AI models. |

---

## DDR4 vs. DDR5

| | **DDR4** | **DDR5** |
|---|---|---|
| **Platforms** | Older: AM4 (Ryzen 5000 and earlier), Intel 12th–14th gen DDR4 boards | Current: **AM5**, **LGA 1851**, and 12th–14th gen DDR5 boards |
| **Typical speed** | 3200–3600 MT/s | 5600–8000+ MT/s |
| **Pros** | Cheaper, and you may be able to reuse it in an older-platform build | Much more bandwidth, higher capacities, the only option on new platforms |
| **Cons** | End of life, no upgrade path | More expensive, especially during the 2026 shortage |

> **2026 market note:** AI data center demand has caused a severe memory shortage. A 32GB DDR5-6000 CL30 kit now costs about **$400**, roughly **3–4 times** what it cost a year ago, and Intel has warned the shortage could last until **2028**. Tips: track prices with a tool like RamRadar, consider starting with 2×16GB and upgrading later, and compare the cost of a prebuilt (see `build-vs-buy.md`), because prebuilt makers often locked in cheaper memory.

---

## RAM for AMD (AM5)

**Target: DDR5-6000 CL30, 2×16GB (or 2×32GB), with EXPO enabled.**

### Why this configuration
- **6000 MT/s is the sweet spot for Ryzen.** It lets the CPU's internal memory controller run in sync (1:1) with the RAM. Going much faster usually breaks that sync and can make performance *worse* unless you tune it by hand.
- **EXPO** is AMD's one-click profile. Most XMP kits also work on AM5.

### Things to know
- **X3D chips** (like the 9800X3D) care less about RAM speed because of their huge cache, so DDR5-6000 CL36 is fine and you don't need premium CL30.
- **Long first boot.** Memory training can take a minute or more the first time, or after changing RAM settings. This is normal. Turn on "Memory Context Restore" in the BIOS to make later boots faster.
- **Stick to 2 sticks.** Four DDR5 sticks on AM5 usually force much lower speeds.

---

## RAM for Intel (LGA 1851, Core Ultra)

**Target: DDR5-6400 to 8000+, 2×16GB (or 2×32GB), with XMP enabled.**

### Why this configuration
- **Arrow Lake's memory controller handles high speeds well.** It runs DDR5-6400 officially and works well at 7200–8000+.
- **CUDIMM kits** add an onboard clock driver for stable 8000+ MT/s speeds. They're most useful with Z890 boards and K-series CPUs.
- **XMP** is Intel's one-click profile.

### Things to know
- **Higher speeds need a capable board.** Check the motherboard's memory support list (QVL). B860 allows memory overclocking, and Z890 boards generally reach the highest speeds.
- **The payoff shrinks at the top end.** 8000+ kits cost much more for single-digit gains. DDR5-6400–7200 is the value zone.
- **Stick to 2 sticks**, as on AMD.

---

## RAM kit options

| Kit | Type | Best for |
|---|---|---|
| **Patriot Viper Venom 32GB DDR5-6000 CL30** | Standard DIMM | About $400, one of the lowest-priced proven 6000 CL30 kits (AMD) |
| **XPG Lancer 32GB DDR5-6000 CL30** | Standard DIMM | About $405, good value 6000 CL30 |
| **V-Color Manta XSky 32GB DDR5-6000 CL30** | Standard DIMM, SK Hynix, EXPO | About $410, a strong AM5 pick |
| **Corsair Vengeance 32GB DDR5-6000 CL36** | Standard DIMM | About $410, a mainstream brand; looser timings are fine for X3D chips |
| **G.Skill Trident Z5 / Flare X5 (AMD) series** | Standard DIMM | Popular enthusiast line with EXPO (Flare X5) and XMP (Trident Z5) versions |
| **CUDIMM DDR5-8000+ (G.Skill, Kingston, Corsair)** | CUDIMM | Intel Core Ultra enthusiasts on Z890 |

---

## Buying & install tips
- **Buy a matched kit** such as 2×16GB. **Don't mix** different kits or brands, even if the specs look the same. Mixed kits often fail to run at their rated speed.
- **Use the right slots.** With 2 sticks, use slots **A2 and B2** (usually the 2nd and 4th from the CPU). The motherboard manual will confirm this.
- **Turn on XMP/EXPO in the BIOS.** Otherwise the RAM runs at a slower default speed, typically 4800–5600 MT/s.
- **Check that it's working:** Task Manager → Performance → Memory shows the speed and how many slots are used.
- **Check clearance** under large air coolers if you're buying tall RGB sticks.
- **Laptops:** check whether the RAM is soldered before planning an upgrade. Many thin laptops can't be upgraded.

---

**Quick verdict:** For almost everyone, buy **32GB (2×16GB) of DDR5**. On **AMD**, get **6000 CL30 with EXPO** (CL36 is fine with X3D chips). On **Intel Core Ultra**, get **6400–7200 with XMP**, or CUDIMM 8000+ for enthusiasts. Capacity and dual-channel matter far more than chasing the highest speed, especially at 2026 prices.

## Sources
- [Newegg – DDR5 price crisis 2026: how to buy RAM smart](https://www.newegg.com/insider/ddr5-price-crisis-buying-guide-2026/)
- [Newegg – Best DDR5 RAM for gaming 2026](https://www.newegg.com/insider/best-ddr5-ram-for-gaming-2026-speed-capacity-and-value-explained/)
- [DropReference – DDR5 shortage April 2026](https://dropreference.com/en/blog/news/ddr5-shortage-april-2026-price-stock-whereismyram)
- [DropReference – Top 3 DDR5 RAM to buy](https://dropreference.com/en/blog/component/top-3-ddr5-ram-buy-april-2026-shortage)
- [RamRadar – DDR4 & DDR5 price tracker](https://ramradar.app/)
- [RamRadar – Best DDR5 RAM for Intel Core Ultra](https://ramradar.app/guides/best-ddr5-ram-for-intel-core-ultra)
- [RAM Prices USA – Best RAM for gaming 2026](https://rampricesusa.com/guides/best-ram-for-gaming)
- [Gaming PC Guru – Best 32GB DDR5 kits 2026](https://gamingpcguru.com/best-32gb-ddr5-ram-2026/)
- [Tech Searchers – Fastest DDR5 kits of 2026](https://techsearchers.com/fastest-ddr5-ram-kits-launched-2026/)
