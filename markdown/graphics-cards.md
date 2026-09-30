# PC Building Guide: Graphics Cards (GPUs)

## What a GPU does

The GPU (Graphics Processing Unit) renders the images you see on screen. It turns 3D scenes into frames by calculating geometry, lighting, textures and effects millions of times per second. A CPU has a handful of fast cores, while a GPU has thousands of smaller cores working in parallel. That design also makes GPUs good at video encoding, 3D rendering and local AI/machine learning. In a gaming PC, the GPU is usually the single component that matters most for frame rate, and it's often the most expensive part.

## What differs between models

| Spec | What it means | Why it matters |
|---|---|---|
| **Shader cores (CUDA cores / Stream Processors / Xe cores)** | The parallel processing units that do the rendering. | More cores means more raw performance, but only compare counts within the same brand and generation. |
| **VRAM (GB)** | The card's own dedicated memory for textures and frame data. | Running out causes stutter and texture pop-in. In 2026, 8GB is entry-level, 12GB is the minimum for 1440p, and 16GB+ is safe for 4K and future games. |
| **Memory type & bus width** | For example GDDR6 vs. GDDR7, or a 128-bit vs. 256-bit bus. | Together these set memory bandwidth, which is how fast the GPU can feed itself data. |
| **Architecture** | The generation of design, such as NVIDIA Blackwell, AMD RDNA 4 or Intel Battlemage. | Newer architectures are faster per core and add features like better ray tracing and AI upscaling. |
| **Ray tracing (RT)** | Hardware that simulates realistic light, reflections and shadows. | Looks great but costs a lot of performance. NVIDIA leads, and AMD closed much of the gap with RDNA 4. |
| **Upscaling & frame generation** | DLSS (NVIDIA), FSR (AMD) and XeSS (Intel) render at a lower resolution and upscale with AI, and can generate extra frames. | Big free FPS boosts. The quality and how many games support it vary by brand. |
| **Total board power (W)** | How much power the card draws. | Decides your PSU wattage, power connectors (8-pin vs. 12V-2x6) and cooling needs. |
| **Physical size** | Length, slot thickness and height. | High-end cards can be over 300mm long and 3+ slots thick, so check that they fit your case. |
| **Media encoder** | Hardware video encoding (NVENC, AMF, Quick Sync). | Matters for streaming, recording and video editing. |

**Resolution targets:** Choose a GPU based on your monitor. **1080p** is budget-class, **1440p** is the current sweet spot for most gamers, and **4K** needs high-end cards.

> **2026 market note:** A global memory (DRAM) shortage driven by AI demand has pushed GPU prices above MSRP, and there have been no major new gaming GPU launches this year. Compare current street prices before buying.

---

## NVIDIA (GeForce RTX)

NVIDIA's current lineup is the **RTX 50 series** (Blackwell architecture) with GDDR7 memory.

### Pros
- **Best ray tracing performance** at every price tier.
- **DLSS 4 with Multi Frame Generation.** The best upscaler available, and it's supported in the most games.
- **Most powerful card on the market.** The RTX 5090 has no competitor at the top end.
- **Best for creative and AI work.** Nearly every AI, 3D and video tool is built around CUDA, and NVENC is an excellent encoder for streaming.
- **Power efficient** for the performance it delivers.

### Cons
- **Most expensive** per frame of raw (non-ray-traced) performance.
- **Stingy VRAM** on lower tiers. The 5060 has 8GB and the 5070 has 12GB.
- **High-end cards use the 12V-2x6 connector**, which needs careful, fully seated installation.
- **Frame-gen numbers inflate marketing.** Generated frames add input latency and aren't the same as real performance.

### Options

| GPU | VRAM | Best for |
|---|---|---|
| **RTX 5060** | 8GB | Budget 1080p gaming |
| **RTX 5060 Ti 16GB** | 16GB | 1080p high / entry 1440p (skip the 8GB version) |
| **RTX 5070** | 12GB | Mainstream 1440p with DLSS and ray tracing |
| **RTX 5070 Ti** | 16GB | Best all-rounder for high-refresh 1440p and 4K |
| **RTX 5080** | 16GB | High-end 4K gaming |
| **RTX 5090** | 32GB | No-compromise 4K, AI and professional work |

---

## AMD (Radeon RX)

AMD's current lineup is the **RX 9000 series** (RDNA 4 architecture) with GDDR6 memory.

### Pros
- **Best raw performance per dollar.** The RX 9070 XT (about $600–650 street) comes close to the RTX 5070 Ti in rasterized (non-ray-traced) games for noticeably less money.
- **Generous VRAM.** 16GB across the 9070 and 9060 XT 16GB, which ages better.
- **Big ray tracing and upscaling improvements.** RDNA 4 greatly improved ray tracing, and FSR 4 is now AI-based with much better image quality.
- **Uses standard 8-pin power connectors** on most models.
- **Excellent Linux support** with open-source drivers built into the kernel.

### Cons
- **Still behind NVIDIA in heavy ray/path tracing.**
- **FSR 4 is in fewer games** than DLSS.
- **No flagship.** RDNA 4 tops out at the upper mid-range, with no answer to the RTX 5080/5090.
- **Weaker for AI and professional apps** because much of that software is built for CUDA.

### Options

| GPU | VRAM | Best for |
|---|---|---|
| **RX 9060 XT 16GB** | 16GB | Budget-to-mid 1080p/1440p with VRAM headroom |
| **RX 9070** | 16GB | Solid 1440p, trades blows with the RTX 5070 |
| **RX 9070 XT** | 16GB | Best value for high-refresh 1440p and entry 4K |

---

## Intel (Arc)

Intel's current lineup is **Arc B-series** (Battlemage architecture). It is budget-focused only.

### Pros
- **Great budget value.** The Arc B580 offers 12GB of VRAM at a price where competitors often ship 8GB.
- **Good XeSS upscaling** and decent ray tracing for its price.
- **Strong media engine** with AV1 encoding, which is great for streaming and media servers.
- **Popular for budget local AI** because of the 12GB of VRAM.

### Cons
- **Budget tier only.** The rumored Arc B770 was shelved (repurposed as the Arc Pro B70/B65 workstation cards), so there's no mid- or high-end option.
- **Needs a modern platform.** Resizable BAR must be enabled, and performance drops on older or slower CPUs.
- **Drivers are less mature.** Much improved, but older games (DX9/DX11) can still be inconsistent.
- **Uncertain future.** Intel's next-gen consumer GPUs are in doubt, and B580 stock is thinning with street prices around $290–330.

### Options

| GPU | VRAM | Best for |
|---|---|---|
| **Arc B570** | 10GB | Tightest budget 1080p builds |
| **Arc B580** | 12GB | Best budget 1080p card, entry 1440p |

---

**Quick verdict:** For the best features, ray tracing and creative/AI work, go **NVIDIA** (the RTX 5070 Ti is the all-round pick). For the most raw FPS per dollar at 1440p, go **AMD RX 9070 XT**. On a tight budget, the **Intel Arc B580** is hard to beat, as long as your CPU and motherboard support Resizable BAR. Whatever you choose, avoid 8GB cards if you can afford to.

## Sources
- [Tom's Hardware – Best Graphics Cards for Gaming 2026](https://www.tomshardware.com/reviews/best-gpus,4380.html)
- [Newegg – RTX 5070 vs RX 9070 XT](https://www.newegg.com/insider/rtx-5070-vs-rx-9070-xt-best-gpu-for-1440p-gaming-in-2026/)
- [Wikipedia – Radeon RX 9000 series](https://en.wikipedia.org/wiki/Radeon_RX_9000_series)
- [Tech Insider – RTX 5070 vs RX 9070 XT (2026)](https://tech-insider.org/rtx-5070-vs-rx-9070-xt-2026/)
- [ThePCEnthusiast – Best RX 9070 XT cards](https://thepcenthusiast.com/best-rx-9070-xt-graphics-cards-to-buy/)
- [PC Gamer – Arc B770 reportedly cancelled](https://www.pcgamer.com/hardware/graphics-cards/intels-arc-b770-gaming-graphics-card-claimed-to-be-dead-and-the-reason-is-inevitably-ai/)
- [How-To Geek – Recommending an Intel GPU in 2026](https://www.howtogeek.com/intels-arc-b580-might-be-the-only-gpu-worth-buying-in-2026/)
- [The FPS Review – Arc Pro B70/B65 launch](https://www.thefpsreview.com/2026/03/25/intels-big-battlemage-finally-arrives-arc-pro-b70-and-b65-launched-today-with-32gb-of-vram-and-up-to-367-tops/)
- [PC Guide – Arc B580 stock](https://www.pcguide.com/news/intel-arc-b580-stock-dries-up-but-three-models-of-the-flagship-gpu-are-still-available-two-with-a-discount-price/)
