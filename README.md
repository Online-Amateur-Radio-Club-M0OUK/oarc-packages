# Welcome to the OARC Packet Radio Repository!

Hello, you've stumbled upon our repository of Debian, Raspberry Pi and Ubuntu packages, maintained by Hibby, MM0RFN. If you have any issues, annoy him on discord and things will get fixed.

## What is OARC?

OARC is the [Online Amateur Radio Club, M*0OUK & EI2OARC](https://oarc.uk) - a welcoming, international radio club with members from around the globe centered around Discord.

We have club callsigns in both the UK and Ireland, and are excited to welcome more new members that share our principles and excitement to play with radio and share knowledge, experience and experiments.

## OARC Packet Radio Project

We have been building a UK and Ireland wide packet network, mostly centred on the [NinoTNC](https://tarpn.net/t/nino-tnc/nino-tnc.html) hardware.
The network covers UHF, VHF and HF Links as well as axip links reflecting where we would have physical interconnections also with a longer term goal of ensuring those links happen over RF in the future.

We are also working with the RSGB ETCC to push for change and improvement for packet radio within the UK, hopefully rewarding other experimenters with simplified and improved regulation.

You can learn more about our packet project on [our wiki](https://wiki.oarc.uk/packet).

## OARC Packet Radio Repo

OARC-PRR is a collection of packages for Debian and some common derivatives, and will occasionally be shipped with opinionated patches by Hibby. Some of the packets are backports from Debian Unstable, some of them are new uploads that won't necessarily benefit the wider userbase of Debian.

We currently Support the amd64 distributions of Debian Unstable/Testing, Debian Stable, Ubuntu 22.04 LTS (with bonus arm64 for Ubuntu). We also support Raspberry Pi OS Stable 'bookworm'/12 and Oldstable 'bullseye'/11 on armhf/armv7 and arm64.  

### Software Improvements

Nino KK4HEJ is actively working with us to implement new waveforms allowing for faster packet radio speeds than before!

Nino and [John, G8BPQ](https://www.cantab.net/users/john.wiseman/Documents/) have been working together on implementing new waveforms and expanding availability for IL2P in QtSoundModem to allow those without the NinoTNC to join in also. 

Direwolf 1.7 (still under development) supports il2p, so it is being shipped as part of this repo to help improve accessibility for all users. 

## Who is doing this?
[Hibby, MM0RFN](https://foxk.it) is an experienced Debian maintainer and long-time packet radio enthusiast... and is also the author of the Readme!

I run the packet node GB7HIB in the City of Aberdeen, Scotland, which uses the Linux Kernel native packet stack, Direwolf and FBB - packages that I also maintain within Debian. 
My full list of current Debian commitments is available [here.](https://qa.debian.org/developer.php?login=d%40vehibberd.com&comaint=yes).

You'll find me in #scottishconsulate on hackint IRC, in the OARC Discord and on the fediverse as @red@woof.tech.  

# Repo Details:

To play along at home, please follow the below advice.

First up, install the GPG key used to sign everything: 

`curl https://online-amateur-radio-club-m0ouk.github.io/oarc-packages/hibby.key | sudo tee /etc/apt/trusted.gpg.d/hibby.asc`

Add the following to your `/etc/apt/sources.list`:

For Debian Testing (13, amd64):

`deb https://online-amateur-radio-club-m0ouk.github.io/oarc-packages testing main`

For Debian Stable (12, released June 2023) amd64:

`deb https://online-amateur-radio-club-m0ouk.github.io/oarc-packages bookworm main`

For Ubuntu 22.04 LTS (Jammy Jellyfish, amd64, released April 2022) amd64:

`deb https://online-amateur-radio-club-m0ouk.github.io/oarc-packages jammy main`

RaspiOS Stable (bullseye, 32 bit armv7/armhf AND arm64, released 2020):

`deb https://online-amateur-radio-club-m0ouk.github.io/oarc-packages bullseye main`

Run the below commands to pull in the package lists & install;

`sudo apt update`

`sudo apt install <PACKAGE>`

# Current packages available

| Package      | Revision                      | Install Name |
| -------      | --------                      | ------------ |
| QtTermTCP    | 0.0.0.69 - nice edition       | qttermtcp    |
| QtSoundModem | 0.0.0.68                      | qtsoundmodem |
| LinBPQ       | 6.0.24.15                     | linbpq       |
| Direwolf     | 1.7-dev                       | direwolf     |
| Uronode      | 2.15, hibby's twists edition* | uronode      |
| FBB          | 7.011                         | FBB          |

* Hibby's twists include: addition of MOTD for users connecting in via Net/Rom, removal of all ROSE & FLEXNET menu commands, removal of telnet/ping and other IP commands and likely some other stuff I've forgotten.

