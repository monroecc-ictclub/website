# PC Building Guide: Processors (CPUs)

## What a CPU does

The CPU (Central Processing Unit) is the part of the computer that carries out instructions from the operating system, games and applications. It handles game logic, physics and AI, compiling code, file compression, and a large share of video encoding. The GPU draws the frames, but the CPU has to feed it data. If the CPU is too slow, the GPU sits idle waiting, which is called a "CPU bottleneck."

## What differs between models

| Spec | What it means | Why it matters |
|---|---|---|
| **Cores / threads** | Independent processing units. With SMT/Hyper-Threading, each core can run 2 threads. | More cores help with multitasking, rendering, streaming and compiling. Most games gain little past 8 cores. |
| **Clock speed (GHz)** | How many cycles each core runs per second. "Boost" is the short-term maximum. | Higher clocks mean snappier single-threaded work and more game FPS. |
| **IPC / architecture** | Instructions per clock, which is how much work each cycle gets done. Newer architectures do more per GHz. | A newer chip can beat an older one even at a lower clock speed. |
| **Cache (L2/L3)** | Very fast memory on the CPU itself. | Games are very sensitive to cache size. This is why AMD's X3D chips lead in gaming. |
| **Hybrid cores (P/E)** | Intel mixes Performance cores with smaller Efficiency cores. | Adds a lot of multi-threaded throughput for less power and die space. |
| **TDP / power draw** | How much heat the cooler has to remove. | Decides what cooler, power supply and case airflow you need. |
| **Integrated graphics** | A basic GPU built into the CPU. | Lets you run without a graphics card or troubleshoot one. Intel "F" and some AMD models don't have it. |
| **Socket / platform** | The physical connector and chipset on the motherboard. | Decides which motherboards fit and whether you can upgrade the CPU later. |
| **Unlocked (K / X)** | The chip can be overclocked. | Mostly matters to enthusiasts. Unlocked chips also tend to be the higher-clocked parts. |

**Tiers:** Both brands use a "3 / 5 / 7 / 9" naming ladder (Ryzen 5/7/9, Core Ultra 5/7/9). A 5 is the budget/mainstream sweet spot, a 7 is upper-mid gaming, and a 9 is for workstation-level multitasking.

---

## AMD (Ryzen)

AMD's current desktop line is the **Ryzen 9000 series** (Zen 5 architecture) on the **AM5** socket, which uses DDR5 memory.

### Pros
- **Best gaming performance available.** X3D chips have 3D V-Cache (extra cache stacked on the chip), and the Ryzen 7 9800X3D is widely rated the fastest gaming CPU. It also has the best 1% lows, meaning fewer stutters.
- **Efficient.** Strong performance per watt, so it runs cooler and quieter and needs a less expensive cooler.
- **Long platform support.** AMD has committed to keeping AM5 around for several generations, so you can drop in a newer CPU later without replacing the motherboard.
- **Consistent core design.** Every core is the same kind, so there are no P-core/E-core scheduling quirks.

### Cons
- **X3D models cost more** than the standard chips.
- **Integrated graphics are very basic** on desktop chips. They're fine for display output, not for gaming.
- **Fewer cores per dollar** in multi-threaded work than Intel's hybrid designs at some price points.
- **Memory matters.** For best results, use DDR5-6000 with EXPO enabled. First boot can take a while because of memory training.

### Options

| CPU | Cores / Threads | Best for |
|---|---|---|
| **Ryzen 5 7600X / 9600X** | 6 / 12 | Budget-to-mid gaming builds |
| **Ryzen 7 9700X** | 8 / 16 | Mainstream sweet spot for gaming and general use |
| **Ryzen 7 7800X3D** | 8 / 16 | Best-value X3D gaming chip |
| **Ryzen 7 9800X3D** | 8 / 16 | Fastest pure-gaming CPU |
| **Ryzen 9 9950X3D** | 16 / 32 | Top-tier gaming plus heavy productivity |

---

## Intel (Core Ultra)

Intel's current desktop line is the **Core Ultra 200S** (Arrow Lake) and the **200S Plus refresh**, which launched March 2026. Both use the **LGA 1851** socket.

### Pros
- **Lots of cores for the money.** The mix of P-cores and E-cores gives excellent multi-threaded performance. For example, the Core Ultra 7 270K Plus has 24 cores for a $299 MSRP.
- **Aggressive refresh pricing.** The Plus chips got more cores, faster memory support and price cuts, and Intel claims about 15% higher gaming performance than the originals.
- **Usable integrated graphics and Quick Sync.** Quick Sync is excellent for video editing, streaming and media servers such as Plex or Jellyfin.
- **Strong productivity performance** in rendering, compiling and content creation.

### Cons
- **Behind in top-end gaming.** AMD's X3D chips still win in most games.
- **Short socket life.** LGA 1851 is expected to be replaced by **LGA 1954** when Nova Lake arrives in late 2026, so it has little upgrade path left.
- **Uses more power** under heavy all-core load, so it needs stronger cooling.
- **Hybrid scheduling quirks.** Occasionally a program or game handles P-cores and E-cores poorly.
- **Worth waiting for Nova Lake?** It's coming soon (up to 52 cores, new socket), so buying now has a timing risk.

### Options

| CPU | Cores (P+E) | Best for |
|---|---|---|
| **Core Ultra 5 250KF Plus** | Hybrid, no iGPU | Budget gaming build with a dedicated GPU |
| **Core Ultra 5 250K Plus** | Hybrid | About $199 mainstream gaming and productivity |
| **Core Ultra 7 270K Plus** | 24 (8P + 16E) | About $299, best Intel value for gaming plus multitasking |
| **Core Ultra 9 285K** | 24 (8P + 16E) | High-end productivity and workstation-style builds |

---

**Quick verdict:** For a gaming-focused build, go **AMD X3D** (9800X3D, or the 7800X3D for value). For multi-threaded or media work on a budget, go **Intel 270K Plus**. If the long-term upgrade path matters, AM5 is the safer platform right now.

## Sources
- [Tom's Hardware – Best CPUs for Gaming 2026](https://www.tomshardware.com/reviews/best-cpus,3986.html)
- [Newegg – Best CPUs for Gaming & Productivity 2026](https://www.newegg.com/insider/best-cpus-for-gaming-productivity-in-2026/)
- [Wikipedia – AMD Ryzen 9950X3D](https://en.wikipedia.org/wiki/AMD_Ryzen_9950X3D)
- [Tom's Hardware – Arrow Lake Refresh announcement](https://www.tomshardware.com/pc-components/cpus/intel-claims-arrow-lake-refresh-cpus-deliver-15-percent-higher-gaming-performance-and-multi-threaded-boost-core-ultra-7-270k-and-core-ultra-5-250k-come-with-more-cores-faster-memory-and-a-price-cut)
- [Newegg – Core Ultra 200S Plus overview](https://www.newegg.com/insider/intels-fastest-gaming-desktop-cpus-are-almost-here-a-complete-look-at-the-core-ultra-200s-plus-arrow-lake-refresh/)
- [TechSpot – Nova Lake confirmed for 2026](https://www.techspot.com/news/109998-intel-confirms-nova-lake-cpu-launch-2026-up.html)
- [TechPowerUp – Nova Lake late-2026 launch](https://www.techpowerup.com/345539/intel-core-ultra-series-4-nova-lake-processors-launch-in-late-2026)
