# PC Building Guide: Monitors

## What a monitor does

The monitor turns the frames your GPU renders into the image you actually see. It's easy to overlook, but it sets a ceiling on your whole system. A powerful GPU is wasted on a 60Hz 1080p screen, and a great monitor can make a mid-range PC feel far better. You also look at it every second you use the computer, and it usually outlasts several PC upgrades, so it's worth budgeting for properly.

**Match the monitor to the GPU:** The resolution and refresh rate you choose decide how powerful a graphics card you need. See `graphics-cards.md`.

---

## Panel types

The panel is the display technology itself, and it has the biggest effect on picture quality.

| Panel | Contrast / blacks | Color & viewing angles | Motion / response | Brightness | Burn-in risk | Price |
|---|---|---|---|---|---|---|
| **TN** | Poor | Poor, washes out off-angle | Very fast | Medium | None | Cheapest |
| **VA** | Very good (≈3000:1) | Good color, weaker angles | Slower; dark smearing | Medium | None | Budget–mid |
| **IPS** | Fair (≈1000:1, "IPS glow") | Excellent | Fast | Good | None | Budget–high |
| **Mini-LED (LCD)** | Very good (local dimming) | IPS/VA-dependent | Fast; possible blooming | **Highest** | None | Mid–high |
| **OLED (QD-OLED / WOLED)** | **Perfect** (per-pixel light) | Excellent | **Near-instant** | Good (lower full-screen) | Some | Mid–high |

### Notes on each type
- **TN (Twisted Nematic):** Old, cheap and fast. It's now mostly limited to esports screens where the only goal is extreme refresh rates. Its colors and viewing angles are poor.
- **VA (Vertical Alignment):** The deepest blacks of any LCD, which makes it great for movies and dark rooms on a budget. The downside is "black smearing," a trail behind dark objects in fast motion. It's common in curved monitors.
- **IPS (In-Plane Switching):** The reliable all-rounder, with accurate colors, wide viewing angles and fast response. It's the best default for mixed work, creative use and gaming, and it handles bright rooms well. Its weakness is grayish blacks and "IPS glow" in dark scenes.
- **Mini-LED:** Not a panel type on its own. It's an LCD (usually IPS or VA) with thousands of tiny LEDs behind it, split into dimming zones. That gives very high HDR brightness and deep blacks, but bright objects can have a halo ("blooming") around them.
- **OLED:** Every pixel makes its own light and can turn fully off, which gives perfect blacks, infinite contrast and near-instant response. It's the best gaming and HDR experience available.
  - **QD-OLED** (Samsung Display) has more vivid, saturated color. It's best in a dark room, because blacks look slightly gray in bright light.
  - **WOLED** (LG Display) is brighter and handles well-lit rooms better.
  - **Tandem OLED** is the newest generation. It stacks several light-emitting layers, making the panel brighter and much more resistant to burn-in. It's reaching mainstream monitors from late 2026 to 2027.
  - **The caveats:** Static elements such as taskbars and game HUDs can slowly **burn in** over time, though modern panels have mitigation features and many brands offer a burn-in warranty. Text can show slight color fringing because of the subpixel layout.

---

## Resolution

Resolution is how many pixels the screen has. More pixels give a sharper image but make the GPU work harder.

| Resolution | Pixels | Ideal size | GPU demand | Notes |
|---|---|---|---|---|
| **1080p** (Full HD) | 1920×1080 | 24" | Low | Budget and esports. Looks soft above 24". |
| **1440p** (QHD) | 2560×1440 | 27" | Medium | **The sweet spot** for most gamers in 2026. |
| **4K** (UHD) | 3840×2160 | 27–32" | High | Very sharp text and detail. Needs a high-end GPU or upscaling (DLSS/FSR). |
| **Ultrawide 1440p** | 3440×1440 | 34" | Medium–High | 21:9 aspect ratio, great for immersion and productivity. Some games don't support it. |
| **5K / 5K2K** | 5120×2880 / 5120×2160 | 27" / 40"+ | Very High | Mostly for creative professionals and Mac users. |

**Pixel density (PPI)** is what makes an image look sharp. Higher resolution on a *smaller* screen looks crisper. A 27" 1080p screen looks blurry, while a 27" 1440p or 4K screen looks sharp.

---

## Refresh rate

Refresh rate (measured in **Hz**) is how many times per second the screen updates. A higher rate makes motion smoother and gameplay feel more responsive, but only if the PC can actually render that many frames per second (FPS).

| Refresh rate | Feel | Best for |
|---|---|---|
| **60Hz** | Basic, noticeably choppy in games | Office work and budget screens |
| **100–165Hz** | Big jump in smoothness | Budget and mainstream gaming |
| **240Hz** | Very smooth, the premium standard | Most enthusiast gamers, and the common OLED target |
| **360–600Hz** | Extremely responsive | Competitive esports (CS2, Valorant, Overwatch) with high-end CPU/GPU |

**The biggest noticeable jump is 60Hz to about 144Hz.** Past 240Hz the gains get smaller and matter mostly to competitive players. Some newer monitors are **dual-mode**: for example, 4K at 240Hz or 1080p at 480Hz at the press of a button.

---

## Other key specs

| Spec | What it means | Why it matters |
|---|---|---|
| **Response time (ms)** | How fast a pixel can change color (usually "GtG," gray-to-gray). | Slow response causes ghosting and blur. OLED takes about 0.03ms, and good IPS about 1–5ms real-world. Don't trust the "1ms" marketing on LCDs. |
| **Adaptive sync (G-Sync / FreeSync)** | The monitor matches its refresh rate to the GPU's frame rate. | Removes screen tearing and stutter without the lag of V-Sync. It's essential for gaming, and most monitors support both brands' GPUs. |
| **HDR** | High Dynamic Range: brighter highlights and a wider range between dark and bright. | Real HDR needs OLED or Mini-LED. **DisplayHDR 400** on a regular LCD is basically marketing. Look for **DisplayHDR True Black 400/500** (OLED) or **HDR 1000** (Mini-LED). |
| **Color gamut** | The range of colors the monitor can show (sRGB, DCI-P3, Adobe RGB). | Matters for photo and video work. Wide gamut makes games and HDR look more vivid. |
| **Size & aspect ratio** | Screen size and shape: 16:9 standard, 21:9 ultrawide, 32:9 super-ultrawide. | Bigger isn't always better. For competitive games, a 24–27" screen keeps everything in view. |
| **Curvature** | For example 1800R or 1000R. A smaller number means a stronger curve. | Helps on ultrawides to keep the edges in view. Unnecessary on 24–27" 16:9 screens. |
| **Ports** | DisplayPort (1.4 / 2.1), HDMI (2.0 / 2.1), USB-C with DisplayPort Alt Mode and power delivery. | High resolution and high refresh together need **DisplayPort 1.4+ or HDMI 2.1** (DSC compression helps). USB-C with power delivery lets one cable connect and charge a laptop. |
| **Stand & ergonomics** | Height, tilt, swivel and pivot adjustment, and VESA mount support. | Makes a big difference to comfort over long sessions. A VESA mount lets you use monitor arms. |
| **Coating** | Matte (anti-glare) or glossy. | Matte hides reflections in bright rooms. Glossy looks punchier and shows deeper blacks, especially on OLED. |

---

## Example options

| Category | Example | Why |
|---|---|---|
| **Budget / office** | Any 24" 1080p IPS at 100Hz | Cheap, clear, a big upgrade over 60Hz for everyday smoothness |
| **Budget gaming** | 27" 1440p IPS at 165–180Hz | Best value; a well-reviewed LCD sweet spot |
| **Best-value OLED** | **MSI MAG 272QP QD-OLED X24** (27" 1440p 240Hz) | QD-OLED at 240Hz for about $400 |
| **Competitive esports** | **ASUS ROG Strix XG27ACDNG** (27" 1440p 360Hz OLED) | Very high refresh rate with OLED response time |
| **Entry 4K OLED** | **Gigabyte MO27U2** (27" 4K 240Hz) | Sharp 4K OLED gaming for about $650 |
| **Premium 4K OLED** | **ASUS ROG Swift PG32UCDM Gen3** (32" 4K 240Hz QD-OLED) | Rated best overall gaming monitor, about $1,300 |
| **Bright-room HDR** | 27–32" Mini-LED with 1000+ dimming zones | Highest brightness, no burn-in risk |

---

**Quick verdict:**
- **Most gamers:** a **27" 1440p monitor at 165–240Hz** is the sweet spot. Choose **IPS** for value, or a **QD-OLED/WOLED** if you can afford about $400+.
- **High-end GPU (RTX 5080/5090 class):** go **4K 240Hz OLED**. Prices have dropped sharply in 2026.
- **Competitive players:** prioritize **refresh rate (360Hz+)** and response time over resolution.
- **Office, school or mixed use with static windows all day:** a quality **IPS** avoids OLED burn-in worries.
- **Always make sure your GPU can drive the resolution and refresh rate you pick.**

## Sources
- [RTINGS – Best Gaming Monitors of 2026](https://www.rtings.com/monitor/reviews/best/by-usage/gaming)
- [RTINGS – WOLED vs. QD-OLED](https://www.rtings.com/monitor/learn/woled-vs-qd-oled)
- [Tom's Hardware – Best Gaming Monitors 2026](https://www.tomshardware.com/reviews/best-gaming-monitors,4533.html)
- [TFTCentral – Best OLED Gaming Monitors 2026](https://tftcentral.co.uk/recommendations/the-best-oled-gaming-monitors-to-buy-in-2026)
- [PCWorld – Best gaming monitors 2026](https://www.pcworld.com/article/813301/best-gaming-monitors.html)
- [WePC – Best OLED monitors 2026](https://www.wepc.com/gaming-monitor/guide/best-oled-monitors/)
- [Newegg – Best 4K 240Hz OLED gaming monitors 2026](https://www.newegg.com/insider/best-4k-240hz-oled-gaming-monitors-2026-top-picks-for-every-setup/)
- [Newegg – Best 1440p OLED gaming monitors 2026](https://www.newegg.com/insider/best-1440p-oled-gaming-monitors-in-2026-your-questions-answered/)
- [Newegg – Gaming monitor panel types explained](https://www.newegg.com/insider/gaming-monitor-panel-types-explained-ips-va-tn-and-oled/)
- [ASUS ROG – QD-OLED vs Tandem OLED vs RGB Stripe OLED](https://rog.asus.com/articles/gaming-monitors/qd-oled-vs-tandem-oled-vs-rgb-stripe-oled-the-complete-gaming-monitor-panel-guide/)
- [DisplayMaster – Mini LED vs OLED](https://displaymaster.dev/blog/mini-led-vs-oled-monitor/)
