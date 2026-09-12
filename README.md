# MyFedorainstall
Was thinking of using arch until yay had malware getting into it so i'm looking into fedora 
but i'll still need to know some commands compared to debian 

Step 1 is first getting the .iso i'm still desiding if i want to use fedora or something like bazzite
but the install process should be the same 

Step 2 after install and if you want going though the secure boot part (next part is for fedora) is install rpm-fusion using graphical setup or use the command line from this page 
https://rpmfusion.org/Configuration

Then after install full ffmpeg using this because of some reason fedora doesn't support H264 out of the box 
sudo dnf swap ffmpeg-free ffmpeg --allowerasing

STEP 2.5 The other part is customizing the OS with these quick settings they should be the same as my arch page 
since i'm still plan on using KDE

"Also to customize it so something like kdewallet stops popping up here's some helpful guides Startup with nothing opened: https://forum.manjaro.org/t/restart-shut-down-and-resume-from-sleep-dont-work/170282/4

Auto log in: https://forum.manjaro.org/t/automatic-login-on-off/168182

Disable kdewallet https://www.youtube.com/watch?v=pzpPBTlmnco&t=28s

For appimages to put on desktop us this to get by the root problem in arch or anything to do with KDE use KATE make a new text document add the desktop entry then save in \user\share\applications then use kde menu editor to move to where you want [Desktop Entry] Name= Exec=/path/to/your/App.AppImage Icon=/path/to/an/icon.png Type=Application Categories=Utility;"

Step 3 is browsers i would try and avoid using flatpaks for browsers but here's the ways for 3 popular ones

Brave: sudo dnf install dnf-plugins-core

sudo dnf config-manager addrepo --from-repofile=https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo

sudo dnf install brave-browser

unless you wanna use flatpak or for bazzite you might get away with this "run0 curl -fsSLo /etc/yum.repos.d/brave-browser.repo https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo" "rpm-ostree install brave-browser"

LibreWolf: sudo dnf config-manager addrepo --from-repofile=https://repo.librewolf.net/librewolf.repo

sudo dnf install librewolf
they also say on the Librewolf site "You should agree to all prompts that want to import the OpenPGP key with the key ID 0x2B12EF16 and the fingerprint 662E 3CDD 6FE3 2900 2D0C A5BB 4033 9DD8 2B12 EF16."

or go though their offical flatpak or use sudo dnf config-manager addrepo --from-repofile=https://repo.librewolf.net/librewolf.repo and rpm-ostree install librewolf for bazzite

Chromium: for chromium open up the store and type in chromium and it should come up as fedora linux but if you want you can enable the google chrome option in settings and get the unverified flatpak
or use sudo dnf install chromium and for bazzite rpm-ostree install chromium

Step 4 is installing games i'll leave some different way depending on the launcher 

Steam: after doing the multimedia step for KDE go to the store then settings then go to "RPM Fusion for Fedora 44-Nonfree-Steam" then search Steam i found this easier than going by the fedora site but i left it here if you wanna do it that way 
https://docs.stg.fedoraproject.org/gl/gaming/proton/

Heroic Launcher: Either use the appimage or use the flatpak 

Lutris: you could either use the flatpak or use sudo dnf install lutris

Minecraft use the other distribution download button or i wouldn't recommand this but there is a unverified fatpak for this

Clone hero just install like a appimage

step 4.5 GAME ADD ONS

Mangohud use releases on github and use ./mangohud-setup.sh install command

Goverlay use appimage or apparently sudo dnf install goverlay -y will work 

Step 5 is the other stuff 

Discord use flatpak unless someone wants to use the tar file

Video editors: kdenlive and shotcut use appimage or flatpak don't know commands and but both editors flatpaks versions i've had problems with

Libreoffice: looks like you can download the .rpm from their site or this might work sudo dnf install libreoffice

ProtonVPN: use either the flatpak version or use the instructions from here 
https://protonvpn.com/support/official-linux-vpn-fedora#install

Timeshift: use this command 'sudo dnf update' and 'sudo dnf install timeshift'

GIMP use flatpak or appimage







