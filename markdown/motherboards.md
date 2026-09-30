# PC Building Guide: Motherboards

## What a motherboard does

The motherboard is the main circuit board that everything plugs into. It connects the CPU, RAM, graphics card, storage, power supply and front-panel ports, and routes power and data between them. The motherboard doesn't make games faster by itself. What it decides is **which parts you can use**, **how many of them you can use**, **how fast they connect**, and **how easily you can upgrade later**. A good board is stable, has the ports you need, and powers your CPU reliably. Paying extra past that mostly buys features, not FPS.

## What differs between models

| Spec | What it means | Why it matters |
|---|---|---|
| **Socket** | The physical CPU connector, such as AMD **AM5** or Intel **LGA 1851**. | Must match your CPU exactly. It also decides your future upgrade path. |
| **Chipset** | The platform controller, such as B850, X870E, B860 or Z890. | Sets the board's feature tier: overclocking, PCIe generation, lane count and USB ports. |
| **Form factor** | Board size: **ATX** (standard), **Micro-ATX** (smaller) or **Mini-ITX** (tiny). | Must fit your case. Smaller boards have fewer slots and ports. |
| **VRM (power delivery)** | The circuitry that converts and regulates power for the CPU. | High-core-count CPUs need strong VRMs to hold boost clocks without overheating. |
| **Memory slots & support** | Usually 2 or 4 DDR5 slots, with a rated maximum speed. | Affects capacity and speed. Two sticks usually run faster and more stably than four. |
| **PCIe generation** | Gen 5, Gen 4 or Gen 3 for the GPU slot and M.2 slots. | Gen 5 is future-proofing. Current GPUs barely benefit, but Gen 5 SSDs need it. |
| **M.2 slots** | Slots for NVMe SSDs. | More slots means more fast storage without cables. Some slots share bandwidth with SATA ports or PCIe slots. |
| **Connectivity** | Wi-Fi/Bluetooth, Ethernet speed (1G / 2.5G / 5G), USB count, USB4/Thunderbolt. | Check the rear I/O for what you actually plug in. Built-in Wi-Fi saves buying an adapter. |
| **BIOS features** | BIOS Flashback, a debug LED/code display, a clear-CMOS button. | Flashback lets you update the BIOS without a CPU installed, which is handy when a new CPU needs a newer BIOS. |

**The golden rule:** Choose the CPU first, then a board with the matching socket, then the chipset tier that has the features you need. Don't overspend here, because that money usually does more for performance in the GPU budget.

---

## AMD (AM5 platform)

AM5 supports Ryzen 7000 and 9000 CPUs and uses **DDR5 only**. There are two chipset generations: the 600 series and the newer 800 series. Both work with the same CPUs.

### Pros
- **Long upgrade path.** AMD has committed to AM5 for multiple CPU generations, so today's board can likely take a future Ryzen after a BIOS update.
- **Overclocking on mid-range boards.** B650/B850 allow both CPU and memory overclocking. Intel keeps CPU overclocking to its Z-series boards.
- **PCIe 5.0 at reasonable prices.** B850 guarantees a Gen 5 M.2 slot, and X870/X870E add a Gen 5 GPU slot.
- **Clear tiers**, and the older B650 boards are still good value.

### Cons
- **Confusing names.** B840 sounds like B850 but is a cut-down budget chipset limited to PCIe 3.0.
- **Boards cost more** than older AM4 boards, especially the X870E flagships.
- **Long first boot.** DDR5 memory training can make the first boot take a minute or more, which is normal but alarming if you don't expect it.
- **May need a BIOS update** before older boards support the newest CPUs. Look for BIOS Flashback.

### Chipset tiers

| Chipset | Key features | Best for |
|---|---|---|
| **A620** | No CPU overclocking, PCIe 4.0 | Cheapest builds with Ryzen 5 non-X / 65W chips |
| **B840** | Budget, PCIe 3.0 only | Basic office/home PCs (avoid for gaming builds) |
| **B650 / B850** | CPU and memory overclocking. B850 guarantees a Gen 5 M.2 slot | **The sweet spot for most gaming builds** |
| **X870** | Gen 5 GPU and M.2 slots, USB4 required | Enthusiasts wanting modern I/O |
| **X870E** | Most PCIe lanes, Gen 5 everywhere, USB4 | Flagship builds with multiple GPUs/SSDs |

### Example boards
- **MSI PRO B850-P WiFi**: budget-friendly B850 with Wi-Fi.
- **Gigabyte B850 Aorus Elite WiFi7**: well-rounded mid-range pick.
- **ASUS ROG Strix B850-A Gaming WiFi**: highly rated mid-range board.
- **MSI MAG X870 Tomahawk WiFi**: about 90% of X870E features for around $225.
- **ASUS ROG Strix X870E-E Gaming WiFi**: top-tier connectivity and VRMs.

---

## Intel (LGA 1851 platform)

LGA 1851 supports Core Ultra 200S and 200S Plus (Arrow Lake) CPUs and uses **DDR5 only**. There are three chipsets: H810, B860 and Z890.

### Pros
- **Thunderbolt 4/5 is common**, especially on Z890 and many B860 boards. That's great for fast external drives, docks and displays.
- **Lots of connectivity**, including many M.2 slots on Z890 boards.
- **Good-value B860 boards** with strong rear I/O for mid-range builds.
- **Mature BIOS and memory support** now that the platform has been out for a while.

### Cons
- **Dead-end socket.** LGA 1851 is expected to be replaced by **LGA 1954** with Nova Lake in late 2026. Plan on changing the board when you upgrade the CPU.
- **CPU overclocking only on Z890.** B860 allows memory overclocking only.
- **Z890 boards are expensive**, and high-end ones cost as much as a good CPU.
- **Gen 5 M.2 is less consistent** on B860 than B850 guarantees on AMD. Check each board's spec sheet.

### Chipset tiers

| Chipset | Key features | Best for |
|---|---|---|
| **H810** | Entry-level, no overclocking, fewer lanes and ports | Budget office/home builds |
| **B860** | Memory overclocking, good I/O, often Thunderbolt 4 | **The sweet spot for most Intel builds** (non-K or K chips run at stock) |
| **Z890** | Full CPU and memory overclocking, most lanes and M.2 slots | K-series CPUs, enthusiasts and heavy storage setups |

### Example boards
- **MSI MAG B860 Tomahawk WiFi**: solid mainstream B860.
- **ASRock B860 Steel Legend WiFi**: impressive rear I/O for the price.
- **MSI MAG Z890 Tomahawk WiFi**: value-focused Z890 for K-series overclocking.
- **ASUS ROG Strix Z890-E Gaming WiFi**: 7 M.2 slots and Thunderbolt 4, a flagship-class board.

---

**Quick verdict:** For most AMD builds, a **B850** (or a discounted B650) board is the best value. Only step up to X870/X870E if you need USB4 or extra Gen 5 lanes. For Intel, **B860** covers most people, and **Z890** is only worth it if you'll overclock a K-series chip or need lots of storage. For future upgrades, **AM5** is the safer bet, because LGA 1851 is near the end of its life.

## Sources
- [Tom's Hardware – Best Motherboards 2026](https://www.tomshardware.com/best-picks/best-motherboards)
- [Club386 – Best motherboard 2026](https://www.club386.com/best-motherboard/)
- [Newegg – B850 vs B860: How to pick a motherboard in 2026](https://www.newegg.com/insider/b850-vs-b860-how-to-pick-a-motherboard-in-2026/)
- [Dave's Computers – B850 vs X870](https://www.davescomputers.com/how-to-choose-a-motherboard-gaming-pc-b850-vs-x870-nj/)
- [Wikipedia – Socket AM5](https://en.wikipedia.org/wiki/Socket_AM5)
- [TechSpot – Guide to AMD AM5 motherboard chipsets](https://www.techspot.com/guides/2901-amd-ryzen-x870-b850-b840-x670-b650-a620-motherboards/)
- [Digital Citizen – AM5 chipsets explained](https://www.digitalcitizen.life/x670e-x670-b650e-b650-chipsets/)
- [HWCooling – X870, X870E, B850 and B840 differences](https://www.hwcooling.net/en/x870-x870e-b850-and-b840-boards-for-amd-differences-and-release-dates/)
