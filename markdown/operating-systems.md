# PC Building Guide: Operating Systems

## What an operating system does

The operating system (OS) is the software layer between your hardware and everything else you run. It manages the CPU, RAM, storage and devices through **drivers**. It provides the desktop, file manager and settings, handles users and security, and gives programs a consistent platform to run on. Every app is built for a particular OS, so **the OS you choose decides what software and games you can run**.

A newly built PC has **no OS installed**. You install one yourself from a USB stick. A prebuilt or laptop usually comes with Windows preinstalled.

---

## Windows

**Current version: Windows 11** (version 25H2). It's the default OS for the vast majority of desktops, and about 70% of Steam users run it as of mid-2026.

### Editions
| Edition | Notes |
|---|---|
| **Home** | Fine for most people. |
| **Pro** | Adds BitLocker drive encryption, Remote Desktop hosting, Group Policy and Hyper-V. Common in schools and businesses. |
| **Education / Enterprise** | Licensed through organizations. Adds management and security features. |

### Requirements
- **TPM 2.0** and **Secure Boot**, both built into modern motherboards (sometimes they need to be turned on in the BIOS).
- A supported CPU (roughly Intel 8th gen / AMD Ryzen 2000 or newer), 4GB+ RAM and 64GB+ storage.
- Setting up Home and Pro now **requires an internet connection and a Microsoft account** by default.

> **Windows 10 note:** Windows 10 left mainstream support in October 2025. Consumers could pay for **Extended Security Updates (ESU)** for one more year, which ends **October 13, 2026**. After that, Windows 10 PCs get no security patches. Upgrade to Windows 11 or switch to Linux.

### Pros
- **Runs almost everything.** It has the widest software and game support, including Microsoft Office, the full Adobe suite, industry, engineering and school software, and every PC game.
- **Best gaming compatibility**, including games with kernel-level anti-cheat (Valorant, Fortnite, Call of Duty, Battlefield and others).
- **Hardware just works.** Every device ships with Windows drivers, and GPU drivers and features like DLSS and frame generation arrive there first.
- **Familiar.** Most people, workplaces and IT help desks know it.
- **Comes preinstalled** on nearly every prebuilt and laptop.

### Cons
- **Costs money** if you build your own PC: about $140 for Home or $200 for Pro at retail.
- **Ads, telemetry and upselling.** Promotions for Microsoft services, data collection and pushes toward OneDrive and a Microsoft account.
- **Forced updates** can restart the PC at bad times or occasionally break things.
- **Bloat.** Preinstalled apps and background services use resources.
- **Less control** over the system than Linux.
- **Main target for malware**, simply because it's so widespread.

---

## Linux

### What is Linux?
Strictly speaking, **Linux is the kernel**: the core that talks to the hardware. A full operating system bundles the kernel with a desktop, apps, a package manager and settings, and each of these bundles is called a **distribution ("distro")**. There are hundreds of distros. They share the same core but differ in philosophy, release schedule, tooling and target audience.

**Key terms:**
- **Desktop environment (DE):** the look and feel. **GNOME** is modern and minimal, like macOS. **KDE Plasma** is Windows-like and very customizable. There are also lighter options like XFCE.
- **Package manager:** installs and updates *all* software from trusted repositories with one command or an app store, like a phone's app store but for the whole system. Examples are `apt` (Debian/Ubuntu), `pacman` (Arch) and `nix` (NixOS).
- **Flatpak / Snap / AppImage:** universal app formats that run on any distro.
- **Release model:** **Fixed/LTS** releases have stable versions with long support and predictable updates. **Rolling** releases get constant updates and always have the latest software.

### Windows vs. Linux: general differences

| | **Windows** | **Linux** |
|---|---|---|
| **Cost** | Paid license | **Free** and open source |
| **Software** | Widest support | Most popular apps have Linux versions or alternatives. **No native** Microsoft Office desktop or Adobe Creative Cloud. |
| **Gaming** | Everything works | **Most games work through Steam's Proton**, but many games with kernel-level anti-cheat (Valorant, Fortnite, CoD, Battlefield) **don't** |
| **Installing software** | Download .exe files from websites | Package manager or app store from trusted repositories |
| **Updates** | Microsoft decides when | You decide. Updates everything at once, including apps. |
| **Customization** | Limited | Nearly unlimited: desktop, look, behavior, even the kernel |
| **Privacy** | Telemetry, ads, account push | No ads, and telemetry is minimal or opt-in |
| **Resource use** | Heavier | Usually lighter, which revives older hardware |
| **Security** | Frequent malware target | Strong permission model and a much smaller malware target |
| **Hardware support** | Universal | Excellent for most hardware. **AMD GPUs work best** because their open-source drivers are built into the kernel, while **NVIDIA** needs its proprietary driver (much improved). Niche peripherals may lack software. |
| **Learning curve** | Familiar | Beginner distros are easy, but troubleshooting sometimes means using the terminal |
| **Where it's used** | Most home and office desktops | **Most of the world's servers, the cloud, supercomputers, Android and the Steam Deck** |

### Linux pros
- **Free** with no licenses, ads or forced accounts.
- **Private and under your control.** Nothing updates or restarts without your permission.
- **Secure and stable.** It's the backbone of most of the internet's servers.
- **Gaming has improved dramatically** thanks to Valve's **Proton** and the Steam Deck. Linux passed 5% of Steam users in March 2026.
- **Great for learning IT, programming and servers**, and a core skill in cloud, DevOps and cybersecurity careers.
- **Makes older hardware feel fast again.**

### Linux cons
- **Some software is missing:** Microsoft Office desktop, Adobe Creative Cloud and some industry or school programs. Web versions or alternatives (LibreOffice, GIMP, Krita, DaVinci Resolve) may or may not be enough.
- **Some games won't run**, mainly multiplayer titles with kernel-level anti-cheat.
- **Troubleshooting can require the terminal** and reading documentation.
- **Many choices** (distros and desktops) can overwhelm beginners.
- **Few PCs come with it preinstalled**, and workplaces and schools usually standardize on Windows.

---

## Linux distributions

### Ubuntu
**Current version: Ubuntu 26.04 LTS "Resolute Raccoon"**, released April 2026. Made by Canonical, a company that backs it commercially. It uses the GNOME desktop by default and is based on Debian.

- **Release model:** fixed. An **LTS** (long-term support) release every 2 years with 5 years of standard support (more with Ubuntu Pro), plus interim releases every 6 months.
- **Package manager:** `apt` (.deb packages), plus **Snap** for many apps.

**Pros**
- **The most beginner-friendly major distro**, with the largest community. Almost every Linux guide or error message has an Ubuntu answer online.
- **Broad hardware and software support.** Vendors target Ubuntu first, and it includes a one-click NVIDIA driver install. Version 26.04 packages AMD ROCm and NVIDIA CUDA for GPU compute.
- **Dominant in the cloud and servers.** The skills transfer directly to IT jobs.
- **"Flavors"** with other desktops: Kubuntu (KDE), Xubuntu (XFCE), Lubuntu (LXQt). There are also popular derivatives like **Linux Mint** and **Pop!_OS**.

**Cons**
- **Canonical pushes Snap packages**, which some users dislike for slower launches and Canonical's control over the Snap store.
- **Some corporate decisions** (Snap, Ubuntu Pro prompts) have annoyed parts of the community.
- Software versions on LTS releases can lag behind the latest.

**Best for:** Linux beginners, students, developers, and anyone who wants things to just work with maximum online help.

---

### Debian
**Current version: Debian 13 "Trixie"**, released August 2025. One of the oldest distros (from 1993), run entirely by a volunteer community with no company. It's the **foundation Ubuntu, Mint and many others are built on**.

- **Release model:** fixed. A new stable release about every 2 years, with ~5 years of support (Trixie is supported until June 2030). There are also **Testing** and **Unstable** branches for newer software.
- **Package manager:** `apt` (.deb packages).

**Pros**
- **Very stable and reliable.** Packages are tested thoroughly before release.
- **Fully community-run** with a strong free-software philosophy and no corporate agenda or Snap.
- **Lightweight and clean,** with no extras you didn't ask for.
- **The go-to for servers**, home labs, Raspberry Pis and low-maintenance machines.
- **Runs on many architectures** (x86, ARM, RISC-V and more).

**Cons**
- **Older software versions.** "Stable" means frozen, so apps, drivers and the kernel can be well behind. That's a problem for the newest GPUs and games.
- **Somewhat less beginner-friendly** than Ubuntu: fewer defaults, and some setup such as proprietary drivers takes more steps.
- **Slower release cycle.**

**Best for:** servers, home labs, older hardware, and users who value stability and a clean, community-run system over the newest features.

---

### Arch Linux
A **minimal, rolling-release** distro built around the "Keep It Simple" philosophy. You build the system up from almost nothing and install only what you choose. It's also the base of SteamOS (Steam Deck) and user-friendly spinoffs like **CachyOS**, **EndeavourOS** and **Manjaro**.

- **Release model:** **rolling**. There are no versions, and you always get the latest software.
- **Package manager:** `pacman`, plus the **AUR** (Arch User Repository), a huge community collection of build scripts for almost any software.

**Pros**
- **Always the newest software:** the latest kernel, drivers and Mesa graphics stack. That's great for new hardware and gaming.
- **Total control.** Nothing is installed that you didn't choose, which makes it lean and fast.
- **The Arch Wiki** is widely considered the best Linux documentation, and it's useful even on other distros.
- **The AUR** means almost any app is available.
- **Deep learning experience.** Installing and maintaining Arch teaches how Linux actually works.

**Cons**
- **Hands-on install.** It's traditionally done manually in the terminal. The `archinstall` script helps, but it's still aimed at experienced users.
- **Rolling updates can occasionally break things.** Read the news before big updates and update regularly.
- **You maintain it yourself.** There's no hand-holding, and community support expects you to have read the wiki first.
- **AUR packages are user-submitted.** Check what you install.

**Best for:** enthusiasts, gamers who want the latest drivers, and anyone who wants to deeply learn Linux. Beginners who want Arch's benefits can try **CachyOS** or **EndeavourOS**.

---

### NixOS
**Current version: NixOS 26.05**, released May 2026. A unique distro built on the **Nix package manager**. The **entire system is described in configuration files**: packages, settings, services and users. NixOS builds the system from that description.

- **Release model:** fixed releases twice a year (**YY.05** and **YY.11**, each supported for about 7 months), or the rolling **unstable** channel.
- **Package manager:** `nix`, with **nixpkgs**, one of the largest package collections of any distro.

**Key concepts**
- **Declarative:** Instead of running install commands, you write what the system should look like in `configuration.nix` and run `nixos-rebuild switch`.
- **Reproducible:** The same config file produces the same system on any machine. Copy your config to a new PC and get an identical setup.
- **Atomic updates and rollbacks:** Every change creates a new system "generation." If an update breaks something, **pick the previous generation from the boot menu**, and you're instantly back to a working system.
- **Flakes and Home Manager** (popular add-ons) pin exact versions and manage your personal dotfiles and settings the same way.

**Pros**
- **Almost impossible to break permanently**, because rollbacks are built in.
- **Reproducible and easy to share**, with the whole system in version-controlled config files.
- **Huge package collection** that's very up to date on the unstable channel.
- **Different versions of a program can live side by side** without conflicts, which is great for developers.
- **Excellent for servers, fleets and dev environments** (`nix-shell` gives each project its own dependencies).

**Cons**
- **Steepest learning curve** of these four. You have to learn the **Nix language**, and it works very differently from other distros.
- **Documentation is scattered** and can be hard to follow, and error messages can be cryptic.
- **Standard Linux instructions often don't apply** because files live in unusual places (`/nix/store`). Some prebuilt programs need workarounds.
- **Uses more disk space** because it keeps old generations (cleaned up with garbage collection).

**Best for:** developers, sysadmins, home-lab builders, and experienced Linux users who want a reproducible, rollback-safe system and are willing to put in the learning time.

---

## Distro comparison

| | **Ubuntu** | **Debian** | **Arch** | **NixOS** |
|---|---|---|---|---|
| **Difficulty** | ★☆☆☆ Easy | ★★☆☆ Easy–Moderate | ★★★☆ Advanced | ★★★★ Advanced+ |
| **Release model** | Fixed (LTS every 2 years) | Fixed (~2 years) | Rolling | Fixed (6-monthly) or rolling |
| **Software freshness** | Moderate | Older / conservative | Newest | New (very new on unstable) |
| **Stability** | High | **Very high** | Good (needs care) | High (**with rollbacks**) |
| **Package manager** | apt + Snap | apt | pacman + AUR | nix |
| **Backed by** | Canonical (company) | Community | Community | Community (NixOS Foundation) |
| **Gaming** | Good | OK (older drivers) | **Excellent** (newest drivers) | Very good |
| **Best for** | Beginners, devs, cloud | Servers, stability | Enthusiasts, learners | Devs, reproducible setups |

---

## Tips
- **Try before you commit:** Most distros boot from a **live USB** (made with a tool like Rufus, balenaEtcher or Ventoy) so you can test them without installing.
- **Dual-boot:** Install Windows *first*, then Linux alongside it, ideally on **separate drives**, and choose which to start at boot. **Back up first.**
- **Check your games** at **ProtonDB.com** and **AreWeAntiCheatYet.com** before switching a gaming PC to Linux.
- **Virtual machines** (VirtualBox, VMware, or GNOME Boxes on Linux) let you try distros inside your current OS with no risk.

---

**Quick verdict:**
- **Windows 11** is the safe default for a gaming PC, especially if you play competitive multiplayer games with anti-cheat or need Office, Adobe or school software.
- **Linux** is a great free alternative if your apps and games are supported. Start with **Ubuntu** (or Mint or Pop!_OS), use **Debian** for rock-solid servers and older machines, try **Arch** (or CachyOS) for the latest drivers and a deep learning experience, and move to **NixOS** when you want a fully reproducible system with built-in rollbacks.

## Sources
- [Microsoft – Windows 11 update KB5124008 (Sept 2026)](https://support.microsoft.com/en-us/servicing/os/windows-11/2026/09/kb5124008-windows-11-24h2-25h2-security-update)
- [Tech Insider – Steam Hardware Survey Aug 2026](https://tech-insider.org/steam-hardware-survey-august-2026/)
- [Tech Times – Steam Hardware Survey June 2026](https://www.techtimes.com/articles/319581/20260703/steam-hardware-survey-june-2026-windows-11-tops-70-amd-closes-intel.htm)
- [Windows Forum – Linux gaming hits 5.33% on Steam (Mar 2026)](https://windowsforum.com/threads/linux-gaming-hits-5-33-on-steam-mar-2026-steam-deck-proton-windows-10-end.413359/)
- [Notebookcheck – Windows 11 grows as Linux pulls back](https://www.notebookcheck.net/Windows-11-continues-to-grow-among-Steam-users-as-Linux-pulls-back.1288709.0.html)
- [TechPowerUp – Windows 10 share dips below 30%](https://www.techpowerup.com/343637/windows-10-market-share-dips-below-30-as-gamers-migrate-to-windows-11?cp=2)
- [Wikipedia – Ubuntu](https://en.wikipedia.org/wiki/Ubuntu)
- [Tux Machines – Ubuntu 26.04 review](https://news.tuxmachines.org/n/2026/05/16/Ubuntu_26_04_Review_and_More_Canonical_Ubuntu_Picks.shtml)
- [Serverspace – Ubuntu 26.04 LTS vs Debian 13](https://serverspace.us/about/blog/ubuntu-26-04-lts-vs-debian-13-which-one-should-you-choose-in-2026/)
- [Wikipedia – Debian](https://en.wikipedia.org/wiki/Debian)
- [NixOS – NixOS 26.05 released](https://nixos.org/blog/announcements/2026/nixos-2605/)
