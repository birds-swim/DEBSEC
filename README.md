# DEBSEC
A humble and lightweight "guide" for Linux users looking for a more security-hardened desktop experience, but don't quite have the free time to read the vast amount of documentation required to achieve such a setup. Spoiler-alert: Reading ahead!

# Table of Contents:

Table here


# Introduction
I stand on the shoulders of giants. I humbly offer this "guide" in the hopes that it will be useful. I don't pretend to make anything new or call anything mine. All the software referenced in this guide were created by companies, organizations, and individuals much smarter and greater than Yours Truly! Their hardwork should be praised. This guide is more like a grocery shopping list of software than an actual in-depth detailed guide on how to lock down your system like Fort Knox. Use it appropriately. You (the User) are solely responsible for the security of your system. Security isn't a software, it's a journey. Please keep up with the relevant security notices regarding Kicksecure and Debian.

I greatly admire the work of OpenBSD, but I still require a more maintsream OS like Linux for popular software like Steam and other things. So I sought to find the next best alternative for my particular needs. After daily driving security-centric software projects like Kicksecure for a month, I created this guide. This "guide" (if you can call it a guide) is more of a grocery list of software projects and applications that I think are great and could meet the widest needs of most desktop Linux users.

My hope is that by completing this guide, the user will have a more secure Debian-based system that is moderately hardened beyond the defaults of a vanilla Debian/SpiralLinux installation. I believe Linux is a secure OS, but that there's always room for improvement!

To clarify, I am not an Engineer/Inventor: I am a traffic cop. Yours Truly is simply here to direct you to the f.ine work others before him have already done.

My goal with this guide is to consolidate all the choice morsels of the most common security advice and suggestions any Privacy/Security beginner can find on social media (various YouTubers, Reddit, PrivacyGuides.org, distro forums, etc.) and put it all into one burrito.  

# Target Audience
Intermediate Linux users looking for a security-focused desktop Linux experience. Linux Users who wish to be secure but don't always need the extreme privacy/anonymity of Whonix or TAILS. QubesOS is most certainly a secure operating system, but not everyone meets the recommended hardware requirements for a comfortable experience. Plus, the user must radically change their habits if they wish to use QubesOS effectively.

If you're looking to secure a server, then I don't know if this guide is for you. It might?

If you're trying to avoid state actors, then this guide is definitely not for you.

I doubt Advanced Linux users will be interested in this guide (for themselves) as I assume they already have their own dotfiles, configs, and shell scripts already prepared for security related stuff. But your feedback is certainly welcome!

# Features
Key Features of DEBSEC:
- SpiralLinux as the starting point (a vanilla Debian distro that uses Btrfs as default filesystem and nonfree hardware support OOTB)
- Kicksecure (the flagship security feature of DEBSEC) 
- Portmaster (consider a premium subscription for Safing.io's SPN)
- Mullvad Browser (as default browser)
- usbguard
- LUKS
- doas
- lynis, tiger, rkhunter, fail2ban, endlessh, auditd, 
- apt-listbugs, apt-listchanges, needrestart, debsecan, debsums
- Password Manager (Bitwarden and KeePassXC are my favorites, but 1Password and Dashlane are good too).
- Brave Web Browser (for PWAs/Web Apps). Strong anti-fingerprinting and support for PWA's
- Picocrypt AppImage (for local file/folder encryption)
- Flatseal
- Singal
- Notesnook

Optional Features:
- micro, tldr, glances, hstr
- Bash-it from Terminalsare.sexy
- 

# Disclaimers
WARNING:  The Kicksecure Team officially supports *only* vanilla Debian. See https://www.kicksecure.com/wiki/Unsupported for details.  I personally haven't bumped into any catestrophic (or minor) issues using SpiralLinux + Kicksecure on a daily basis, but technically we're breaking Kicksecure's rules here. You're Milage May Vary.
WARNING:  I am by no means a security expert or IT professional, nor do I claim to be one.

# Requirements
- A fresh install of SpiralLinux Builder Edition with a single user account named "User" (Kicksecure requirement).
- NextDNS account.

# Installation

1. SpiralLinux 
---> Grab a copy of SpiralLinux here: https://spirallinux.github.io/ (Builder Edition recommended for this guide; otherwise, choose your favorite Desktop Environment.)
- SpiralLinux recommends [Balena Etcher](https://etcher.balena.io) or [ROSA ImageWriter](http://wiki.rosalab.com/en/index.php/ROSA_ImageWriter) for a successful installation.
- After flashing the SpiralLinux ".iso" file to a USB flashdrive, boot the installation media.  Open a Terminal and type these commands:
- `cd /etc/calamares/modules`
- Then edit the `fstab.conf` file to add additional Btrfs mount options appropriate to your system. Look here for details: https://btrfs.readthedocs.io/en/latest/ch-mount-options.html
- Save the file and start the installer. 
- REQUIRED: The name and username must be "User" for Kicksecure to work properly. If you don't, you'll have to start all over.
- Do not set a swap file, change the default filesystem, or make any custom partitions. Leave them as they are.
- I highly recommend enabling full disk encryption for this build with a DiceWare password. https://diceware.dmuth.org/  Try to keep it between 3-5 DiceWare words and easy to remember. Write it down if you need.
- Set name and username as "user". Create a password.
- Install the system. Reboot.

2. SpiralLinux Post-Installation
- You have a lot of freedom from here to choose what kind of Debian system you want. Kicksecure officially supports Xfce, so you'll be installing Xfce apps those devs are most familiar with. Although, I did ask a question on [Reddit](https://www.reddit.com/r/Kicksecure/comments/129tsn6/debian_xfce_vs_kicksecure_xfce)


# Driving the Tank
Flatpak everything. Use Flatseal for permissions management. Some sandboxing is *still* better than no sandboxing at all. Use Firejail for Picocrypt. Consider DistroBox for any additional software you can't find in Debian's repos or in a Flatpak (i.e., packages from the AUR).

# Sources
-->references to Arch Wiki and other security guides here
-->references to YouTube guides and social media posts
  
# Conclusion
Security is a journey; it's not a destination. Hopefully, by the end of this guide, you should have a moderately secure system hardened beyond the defaults of a typical Debian/SpiralLinux installation. A good starting point to choose to add or subtract software packages from your new system.

# Special Thanks
Many thanks to these fine folks and their projects for creating amazing software for the Linux Community. Yours Truly included!
-->list software projects here
-->list cool folks here
Debian GNU/Linux
Software in the Public Interest, Inc.
SpiralLinux
Whonix and Kicksecure
Mullvad
Safing.io
OpenBSD
