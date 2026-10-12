# Operating Systems Workshop

## Welcome

Every computer needs an operating system before it does anything useful. The OS sits between your hardware and your programs: it manages the CPU, memory, storage and devices, and it gives you the desktop, files and apps you work with every day. Most people never choose their OS. It comes preinstalled, and they keep it. Today we're going to change that.

In this workshop we'll look at a range of operating systems, from the one almost everyone already knows to some that ask a lot more of you. We'll talk about who each one is for, then make a **live boot USB drive** so you can try one out without touching what's already on your computer. If you brought a laptop and you're feeling brave, you can leave with a fresh install.

---

## Today's Options

- Windows 11
- Ubuntu
- Debian
- Arch Linux
- Linux Mint
- Fedora
- Gentoo
- Kali Linux
- NixOS
- Hannah Montana Linux

There's no single "best" OS here. Each one makes different trade-offs between ease of use, stability, control and how much you're willing to learn. Think about what you use your computer for while we go through them.

---

## Making a Live Boot USB with Rufus

A **live boot USB** is a flash drive that holds a complete operating system. When you start a computer from it, the OS runs straight off the drive and leaves your internal drive alone. You can use it to test a system, check that your hardware works with it, rescue files from a broken install, or run the installer.

To make one on Windows we'll use **Rufus**, a free and open-source tool from [rufus.ie](https://rufus.ie). It doesn't need to be installed; you just download it and run it. The process looks like this:

1. **Download the ISO.** An ISO is a single file containing the whole OS installer. Always get it from the distribution's official website.
2. **Plug in your USB drive.** Use one that's 8 GB or larger. **Everything on it will be erased.**
3. **Open Rufus and pick your drive** under *Device*. Double-check it's the right one.
4. **Click *SELECT* and choose your ISO.** Rufus fills in sensible settings for you, so in most cases you can leave the partition scheme (GPT for modern computers) and file system alone.
5. **Click *START*.** If Rufus asks whether to write in *ISO Image mode* or *DD Image mode*, go with the recommended ISO mode first. If the drive won't boot, try again in DD mode.
6. **Boot from the drive.** Restart the computer and press the boot menu key (often F12, F11, F10, Esc or F8, depending on the manufacturer), then pick the USB drive.

Rufus also has a few extras worth knowing about. For Windows 11 ISOs it can remove the TPM, Secure Boot and Microsoft account requirements, which helps on older hardware. For Ubuntu-based ISOs it can add **persistence**, which saves your files and settings on the USB between boots.

Not on Windows? On Linux and macOS, **balenaEtcher** or **Fedora Media Writer** do the same job, and **Ventoy** lets you put several ISOs on one drive and pick between them at boot.

---

## Windows 11

Windows is what most people already use, and that's its biggest strength. It runs nearly every program and game ever written for a PC, every piece of hardware ships with Windows drivers, and every workplace and help desk knows it. That compatibility comes at a cost: a retail license is about $140, and the system comes with ads, telemetry, forced updates and a push toward a Microsoft account. Windows 11 also requires TPM 2.0, Secure Boot and a fairly recent CPU. This one is timely. Paid security updates for **Windows 10 end on October 13, 2026**, the day after this workshop, so anyone still on Windows 10 has to choose between upgrading and switching.

---

## Ubuntu

Ubuntu is the best-known Linux distribution and a common first step away from Windows. It's made by Canonical, releases a new version every six months, and puts out a **Long Term Support (LTS)** release every two years with five years of updates. Most Linux software and tutorials assume Ubuntu, so help is easy to find. It uses the GNOME desktop, which looks and works differently from Windows, and Canonical's **Snap** package format is a common complaint among users. Still, if you want something that just works and has the largest community behind it, Ubuntu is a safe choice.

---

## Debian

Debian is one of the oldest Linux distributions, running since 1993, and one of the most important: Ubuntu, Mint and hundreds of others are built on it. It's run entirely by a community of volunteers rather than a company. Debian's **stable** release is famously reliable because software is tested for a long time before it's included. The trade-off is that programs can be a version or two behind. It's a favourite for servers and for anyone who wants a solid desktop that stays out of the way.

---

## Arch Linux

Arch Linux gives you a minimal base system and has you build up the rest yourself. It's **rolling release**, so there are no big version upgrades; you get the newest software as soon as it's ready. Its package manager, **pacman**, is fast, and the community-run **Arch User Repository (AUR)** contains almost any software you can think of. The **Arch Wiki** is one of the best Linux references anywhere, and it's useful no matter which distro you run. Installing Arch used to mean typing every step by hand, but the included **archinstall** script now walks you through it. Expect to learn a lot and to fix things yourself now and then.

---

## Linux Mint

Linux Mint is built on Ubuntu LTS but aimed squarely at people coming from Windows. Its **Cinnamon** desktop has a taskbar, a start menu and a system tray right where you'd expect them. It skips Snap packages, comes with media codecs and everyday apps ready to go, and includes friendly tools for updates and drivers. It changes slowly and on purpose, which makes it one of the most comfortable and dependable desktops to start on. If you aren't sure which Linux to try first, try this one.

---

## Fedora

Fedora is sponsored by Red Hat and serves as the proving ground for technology that later ends up in Red Hat Enterprise Linux. It ships recent software, but every release is tested, so it sits between Debian's caution and Arch's constant updates. The main edition, **Fedora Workstation**, runs a clean, unmodified GNOME desktop, and there are versions called **Spins** with other desktops such as KDE Plasma. Linus Torvalds, the creator of Linux, uses Fedora. It's a great pick for developers and anyone curious about Red Hat systems used in industry.

---

## Gentoo

Gentoo takes the do-it-yourself idea even further: most software is **compiled from source code on your own machine**. Its package manager, **Portage**, uses **USE flags** to let you choose exactly which features each program is built with, so the system is tuned to your hardware and your needs. The downside is time. Installing Gentoo can take hours or days, and big updates mean long compiles, although binary packages are now offered for many programs. Nobody picks Gentoo for convenience. People pick it to understand how a Linux system is put together from the ground up.

---

## Kali Linux

Kali Linux is a Debian-based distribution built for **cybersecurity work**: penetration testing, digital forensics and security research. It's maintained by Offensive Security and comes with hundreds of security tools already installed, such as Nmap, Wireshark, Metasploit and Burp Suite. Kali is designed to run from a live USB, which makes it a natural fit for today's workshop, and it's also common in virtual machines. It isn't meant to be an everyday desktop, though; it's a specialized toolkit. Keep in mind that **these tools are only legal to use on systems you own or have written permission to test**. For practice, use your own lab or legal training sites like Hack The Box and TryHackMe.

---

## NixOS

NixOS works differently from every other system on this list. Instead of installing and changing things one command at a time, you describe your **entire system in a configuration file**: packages, services, users, settings. NixOS then builds the system to match. Because every change creates a new version of the system, you can **roll back** to an earlier one from the boot menu if an update breaks something. You can also copy your config to another machine and get an identical setup. The **Nix** language is notoriously hard to learn, but people who get past that often don't want to go back.

---

## Hannah Montana Linux

And now for something completely different. Hannah Montana Linux is a fan-made distribution from around 2009, based on Kubuntu 9.04, with a full Hannah Montana theme: wallpapers, icons, login screen and all. It became a running joke in the Linux world and a great example of how anyone can take an open-source system and remix it into their own. It hasn't been updated in over fifteen years, so **don't use it for anything real**: it has no security updates and won't support modern hardware. It's fun to boot in a virtual machine and see what desktop Linux looked like back then.

---

## Wrapping Up

The best way to choose an operating system is to try one. A live USB costs you nothing but a few minutes and a flash drive, and it won't touch your current setup. Start with something friendly like Mint or Ubuntu, and if you get curious, work your way down the list. Officers are around if you get stuck.
