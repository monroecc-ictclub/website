# PC Building Guide: Storage (SSDs & Hard Drives)

## What storage does

Storage is the computer's long-term memory. It holds the operating system, programs, games and files, and unlike RAM it **keeps everything when the power is off**. When you launch something, it's read from storage into RAM (see `ram.md`).

Storage speed affects **how fast things load**: boot times, app launches, game loading screens, file transfers and texture streaming in open-world games. Once a game is loaded, it has very little effect on FPS. Capacity decides **how much you can keep installed at once**, and modern games often take 100–200GB each.

**The golden rule:** Always put the operating system on an **SSD**. A PC booting from a hard drive feels painfully slow in 2026.

---

## Storage types

| Type | How it works | Typical speed (sequential read) | Pros | Cons |
|---|---|---|---|---|
| **HDD (Hard Disk Drive)** | Spinning magnetic platters and a moving read head | ~150–280 MB/s | **Cheapest per TB**, huge capacities (20TB+) | Slow, noisy, fragile. Moving parts can fail. |
| **SATA SSD (2.5")** | Flash memory over the older SATA interface | ~550 MB/s | Fits older PCs and laptops, a big upgrade over an HDD | Limited by SATA. Needs data and power cables. |
| **NVMe SSD – PCIe 3.0** | Flash memory on an M.2 stick over PCIe | ~3,500 MB/s | Cheap and still quick for everyday use | Older standard |
| **NVMe SSD – PCIe 4.0** | Same as above, with the PCIe generation doubled | ~5,000–7,450 MB/s | **The sweet spot**: fast, mature and well-priced | Slightly warmer than Gen 3 |
| **NVMe SSD – PCIe 5.0** | Newest generation | ~10,000–14,700 MB/s | Fastest available | 2–3× the price, runs hot (needs a heatsink), little real-world gaming benefit yet |
| **External / portable SSD** | SSD in a USB or Thunderbolt enclosure | ~1,000–4,000 MB/s (USB/port dependent) | Portable backups and transfers | Limited by the port speed |

**How much faster feels faster?** Moving from an HDD to any SSD is a huge difference. SATA SSD to NVMe is noticeable. Gen 4 to Gen 5 is hard to notice outside of large file transfers and professional workloads.

---

## What differs between models

| Spec | What it means | Why it matters |
|---|---|---|
| **Form factor** | **M.2 2280** (22mm wide, 80mm long) is the desktop standard. **2.5"** is used by SATA SSDs and laptop HDDs, and **3.5"** by desktop HDDs. | Must fit your motherboard or case. Some small laptops and handhelds use shorter M.2 2230 or 2242 drives. |
| **Interface** | SATA or NVMe (PCIe Gen 3/4/5). | An M.2 slot can be SATA-only, NVMe-only or both, so check the motherboard manual. A Gen 5 drive in a Gen 4 slot works, but only at Gen 4 speed. |
| **Sequential speed** | Speed for large single files (the number on the box). | Matters for huge transfers and video editing. |
| **Random read/write (IOPS)** | Speed for many small files. | **What actually makes a PC feel snappy** when booting, launching apps and loading games. |
| **NAND type** | How many bits each memory cell stores: **TLC** (3) or **QLC** (4). | TLC is faster under sustained writes and lasts longer. QLC is cheaper and denser but slows down a lot during long writes. |
| **DRAM cache** | A small memory chip on the drive that stores its "map" of where data lives. | DRAM drives stay fast under heavy use. **DRAM-less (HMB)** drives borrow system RAM and are fine for gaming and general use. |
| **SLC cache** | Part of the drive acts as a fast buffer. | Writes are very fast until the cache fills, then they drop. Only matters for very large copies. |
| **Endurance (TBW)** | "Terabytes Written," the rated lifetime of writes. | Typical ratings (600TB+ per TB of capacity) far exceed normal home use. |
| **Warranty** | Usually 3–5 years for SSDs. | A 5-year warranty signals a higher-quality drive. |
| **Heatsink** | A metal cooler on top of the drive. | Gen 5 drives need one. Most motherboards include M.2 heatsinks, so buy the version without one if yours does. |

---

## How much storage do you need?

| Capacity | Good for |
|---|---|
| **500GB** | OS plus basic apps only. Too small as the only drive for gaming. |
| **1TB** | Budget builds: OS, apps and a few large games. |
| **2TB** | **The recommended starting point** for a gaming PC. |
| **4TB+** | Big game libraries, video editing and content creation. |
| **HDD 4–20TB+** | Bulk media, photo and video archives, and backups. |

**Tip:** SSDs slow down and wear faster when nearly full. Try to keep **10–20% free**.

### Common setups
- **Budget:** a single 1TB NVMe for everything.
- **Mainstream gaming:** a 2TB NVMe Gen 4, with room for a second M.2 drive later.
- **Enthusiast / creator:** 1–2TB NVMe for the OS and apps, a 2–4TB NVMe for games and projects, and an HDD or NAS for archives and backups.

> **2026 market note:** The same AI-driven memory shortage raising RAM prices has hit SSDs too. NAND prices jumped as much as 65% in a single month in late 2025, and a 1TB NVMe now runs about **$150–$320** depending on the tier. Consider starting with a smaller drive and adding a second later, since most boards have multiple M.2 slots. HDDs remain the cheapest per TB for bulk storage.

---

## NVMe SSDs by tier

### Budget (PCIe 4.0, DRAM-less)

**Pros:** cheapest NVMe, still about 10× faster than an HDD, and fine for gaming.

**Cons:** slows down during long, heavy writes, and usually has shorter warranties and endurance.

### Mainstream / high-end (PCIe 4.0, DRAM, TLC)

**Pros:** the best balance of speed, price, endurance and temperature, and the most-reviewed drives.

**Cons:** costs more than budget drives, for a difference most gamers won't notice.

### Enthusiast (PCIe 5.0)

**Pros:** the fastest sequential and random performance available, ready for future DirectStorage games, and great for huge file workloads.

**Cons:** 2–3× the price per TB, runs hot and needs a heatsink, requires a Gen 5 M.2 slot (B850/X870 on AMD, check B860/Z890 boards on Intel; see `motherboards.md`), and gives little real gaming benefit today.

---

## Storage options

| Drive | Type | Best for |
|---|---|---|
| **Kingston NV3** | NVMe Gen 4, DRAM-less | About $150/TB, lowest-cost NVMe |
| **Crucial P310** | NVMe Gen 4, DRAM-less | About $172/TB, budget pick with good efficiency (also comes in the 2230 size) |
| **WD Black SN850X** | NVMe Gen 4, DRAM | Proven high-end Gen 4 gaming drive |
| **Samsung 990 Pro** | NVMe Gen 4, DRAM | About $319/TB, the fastest Gen 4 drive (maxes out the interface at 7,450 MB/s) |
| **WD Black SN8100** | NVMe Gen 5 | Rated the best Gen 5 SSD, fast and relatively efficient |
| **Samsung 9100 Pro** | NVMe Gen 5 | Up to 14,700 MB/s, with capacities up to 8TB and a 5-year warranty |
| **Samsung 870 EVO / Crucial MX500** | 2.5" SATA SSD | Upgrading older PCs and laptops without M.2 |
| **Seagate IronWolf / WD Red Plus** | 3.5" HDD (NAS-rated) | Reliable bulk storage for media, backups and NAS boxes |

---

## Install & setup tips
- **Check which M.2 slot to use.** The top slot (closest to the CPU) is usually the fastest, often Gen 5 on newer boards. Some slots **turn off SATA ports or share lanes with a PCIe slot**, so read the manual.
- **Use the included standoff or latch** and the motherboard's M.2 heatsink, and **peel the plastic film off the thermal pad**. This is a very common mistake.
- **A new drive doesn't show up?** Initialize and format it in **Disk Management** (Windows) before it will appear in File Explorer.
- **Moving from an old drive:** cloning software can copy your existing OS, or do a clean Windows install on the new SSD. A clean install is usually the better choice.
- **Keep firmware updated** with the manufacturer's tool (Samsung Magician, WD Dashboard and others).
- **Don't defragment SSDs.** Windows handles SSD maintenance (TRIM) automatically. Defragmenting is only for HDDs.

## Backups: the 3-2-1 rule
Storage **will** fail eventually, and SSDs often fail without warning. Protect important files with:
- **3** copies of your data,
- on **2** different types of storage (for example the internal SSD plus an external drive),
- with **1** copy offsite or in the cloud (OneDrive, Google Drive, Backblaze and similar).

---

**Quick verdict:** For most builds, get a **2TB PCIe 4.0 NVMe SSD** from a reputable brand. A budget DRAM-less drive is perfectly fine for gaming, and a DRAM model like the SN850X or 990 Pro is worth it for heavy workloads. **Skip Gen 5** unless you move huge files regularly or have money to spare. Add an **HDD** only for bulk media and backups, never as the OS drive. And whatever you buy, **back up what matters**.

## Sources
- [Tom's Hardware – Best SSDs 2026](https://www.tomshardware.com/reviews/best-ssds,3891.html)
- [GPCB – Fastest M.2 NVMe SSDs in 2026](https://www.gamingpcbuilder.com/best-m-2-nvme-ssd/)
- [GPCB – Best 4TB+ SSDs 2026](https://www.gamingpcbuilder.com/4tb-ssd-roundup-all-4-tb-solid-state-drives/)
- [Tech Insider – WD Black SN8100 vs Samsung 9100 Pro](https://tech-insider.org/wd-black-sn8100-vs-samsung-9100-pro-2026/)
- [GearForge – Best NVMe SSDs in 2026](https://gearforge.blog/en/components/storage/ssd/best-ssd-2026)
- [StorageDiskPrices – SSD price history & 2026 forecast](https://storagediskprices.com/ssd-price-history/)
- [HardDrive.net – Best NVMe SSD in 2026](https://harddrive.net/best-nvme-ssd/)
