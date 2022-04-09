# **HELL INTERFACING ESSENTIAL SOFTWARE**

Here we fill out the software we use and recommend to other HELL INTERACING users (and possibly beyond). This list will attempt to strike a balance between proprietary software and free software, there's no favoritism at either end (but we absolutely despise abhorrently bloated software and stuff you have to jump through countless hoops in order to get working without sacrificing a child in the process to the FAGMAN overlords).

## **Navigation**

- [Operating Systems](#operating-systems)
- [Package Managers](#package-managers)
- [Web Browsers](#web-browsers)
- [Utilities](#utilities)
- [Programming](#programming)
- [Multimedia - Music](#music)
- [Multimedia - Video](#video)

## **Operating Systems**

### *[Windows 8](https://www.microsoft.com/en-us/software-download/windows8ISO)*

Hot take, but once you strip Windows 8.1 out of its abhorrent design choices and remove all of the bloat, it's a great OS. EOL ends in 2023 so it's still going despite being on the brink of death. There's no lack of driver update issues like with Windows 7 in terms of modern devices and GPUs so it'd be great for gaymen. Only download official Windows 8.1 ISOs from the Microsoft site and then active with an activator of your choice (such as a clean version of KMS).

### *[Windows 10 (Modified)](https://www.microsoft.com/de-de/software-download/windows10)*

Underneath the TONS and TONS of Bill Gates turbo AIDS, there's a perfectly capable OS in here. You have to jump through quite a bit of hoops to get this thing clean for personal use, but once you do so, there isn't any debate - it's a good OS. Like earlier. Only download official ISOs from the Microsoft site instead of some Indian "Super Tech 64" Blogspot sites and activate with HWID. Note that in order to get the ISO download on the site instead of the Media Creation Tool, you'll have to change you're browser's User-Agent to either Linux or Mac OS. Next up you'll want to use something like Sycnex's [Windows10Debloater](https://github.com/Sycnex/Windows10Debloater) and run either the commandline PowerShell script or the GUI version.

### *[Windows 10 AME](https://ameliorated.info/)*

...alternatively you can instead get a version of Windows 10 named [Ameliorated](https://ameliorated.info/). This modified installer of Windows 10 removes a ton of the pre-installed bloatware, minimizes install time, eliminates things such as Windows Update and Cortana and removes many of the telemetry that Microsoft added. The changelist is massive and it is recommended to read up on AME yourself, or better yet, test drive it in a VM or a computer you might have lying around doing nothing.

### *GNU/Linux*

You knew this was coming. If you really, really love tinkering with your computer and want to immerse yourself in a new environment where knowledge of the inner workings of your OS and a lot of the installed software is incredibly useful, GNU/Linux might be for you. It's a vast world of [distributions](https://distrowatch.com/) which ranges from noob-friendly Windows replacements like [Linux Mint](https://linuxmint.com/) to l33t h4x0r + cunny-connoisseur distro like [Arch Linux](https://archlinux.org/). Speaking of Arch, appreciate the [ArchWiki](https://wiki.archlinux.org/) with all your power, because it is possibly one of the most comprehensive and well-maintained documentations in everything tech, going beyond just Arch but every aspect of GNU/Linux as well. Grab an ISO of whichever distro interests you and fire it up in a VM or install it on a Live USB and test drive it on your computer without having to install anything. Further info on GNU/Linux will be bellow.

## **Package Managers**

An advantage that has been enjoyed by Mac OS X and GNU/Linux users for years has been the concept of a package manager. Bluntly put, it's a piece of software that lets you connect to a central repository where other software is hosted and with it you can install applications within your commandline without the need to look for .exe's or any installer binaries yourself. A package manager can also batch update your installed software with a single command which is a selling point alone. The problem is that these repositories host mostly open-source software only and very rarely would you find closed-source, proprietary programs (but then again, you might be better off without them if there's a good open-source alternative instead).

### *[Chocolatey](https://chocolatey.org/)*

Choco is probably the largest package manager on Windows so far. It's super simple to install and figure out how to use it, especially if you have former package manager knowledge. On the website there is a ["search packages" function](https://community.chocolatey.org/packages) which will let you scour the entire repo and copy the install commands to paste into your commandline. The community is pretty large and the project seems to be in constant support, perhaps moreso than even Microsoft's own package manager winget.

### *winget*

In response to the surge in popularity that package managers have been receiving over the past couple of years, Microsoft responded with winget. It is included by default with Windows 11 and also available through Windows 10's 1709 version. It supposedly does what it says on the tin, but I personally have not used it and cannot speak for its quality especially compared to Chocolatey. Similarly to Choco's package repository search tool, there's also [winget.run](https://winget.run/) to browse the winget repo and conveniently copy commands.

## **Web Browsers**

### *[Firefox Nightly](https://www.mozilla.org/en-US/firefox/channel/desktop/)*

This is the beta channel of Mozilla Firefox, which I personally find to be (ironically enough) more stable than the stable channel. You do get quite a bit of "update available" notifications but it's definitely something you can disable in `about:config`. By now everyone should know what Firefox is, and despite Mozilla's [incomprehensibly dumb actions](https://blog.mozilla.org/en/mozilla/we-need-more-than-deplatforming/) over the recent years, this is still a fine browser that competes with the Chromium cancer that's infesting every other contemporary browser out right now. While it is factually slower in some use cases over Chrome or Edge, its extensibility and customization gives it a real advantage that you should consider when picking a browser.

>Install with...  
Choco: `choco install firefox-nightly --pre`  
winget: `winget install -e --id Mozilla.Firefox.Nightly`

### *[ungoogled-chromium](https://github.com/Eloston/ungoogled-chromium)*

ungoogled-chromium is a modification of Google Chromium which removes pretty much all of the features that phone back home to Google (even in normal Chromium). It does not allow the use of a Google account due to the stripped Google account integration. You might have to spend some time configuring its `chrome://settings` to your liking and enable things like saving cookies and site data upon closing of the browser, as such features are disabled by default for privacy reasons. Consult the [wiki](https://ungoogled-software.github.io/ungoogled-chromium-wiki/) for further information.

>Install with...  
Choco: `choco install ungoogled-chromium`

## **Utilities**

### *[Everything](https://www.voidtools.com/)*

Everything is an incredibly fast and lightweight file search engine for Windows which indexes your drive/s and monitors for changes to keep its index up to date. It also allows for Regex and advanced searches based on file metadata for extremely precise searches. It is recommended to exclude the Windows install folder by default as files within that directory could clog up your search results pretty often.

>Install with...  
Choco: `choco install everything`  
winget: `winget install -e --id voidtools.Everything`

### *[7zip](https://www.7-zip.org/)*

7zip is a free and open source file archiver which can extract and pack compressed files like ZIP, 7Z, TAR, XZ, etc. It should be noted that RAR is only supported in a "read-only" mode, meaning that 7zip cannot create or modify RAR files. Still, 7Z as an archive format should be preferred due to its better compression and efficiency.

>Install with...  
Choco: `choco install 7zip`

### *[HWiNFO](https://www.hwinfo.com/)*

HWiNFO is a Windows application which gives you extremely detailed information on your hardware and what it's currently doing. Think of Speccy, but on steroids. The program includes a sensor monitor which gives you a great view on every single aspect of your computer's hardware as well as a logger to monitor changes over time.

>Install with...  
Choco: `choco install hwinfo`  
winget: `winget install -e --id REALiX.HWiNFO`

### *[QTTabBar](http://qttabbar.wikidot.com/)*

QTTabBar gives you more control over customizing the Windows File Explorer by enabling tabs and changing Explorer's behaviour like double-clicking on an empty space to have you go up a directory. It's small stuff, but once you're used to it, there's no going back.

>Install with...  
Choco: `choco install qttabbar`

### *[JDownloader 2](https://jdownloader.org/jdownloader2)*

Open-source download manager written in J*va. Works great for batch downloading and queuing a bunch of links for sequential download. Supports all kinds of sites and allows logins for various premium file hosting services. This is what I personally use for downloading stuff from Archive. Because J**a sucks, the program feels slow, clunky and heavy, but otherwise works good.

>Install with...  
Choco: `choco install jdownloader`

### *[Bulk Crap Uninstaller](https://www.bcuninstaller.com/)*

// todo

>Install with...  
Choco: `choco install bulk-crap-uninstaller`  
winget: `winget install -e --id Klocman.BulkCrapUninstaller`

## **Programming**

### *[Notepad++](https://notepad-plus-plus.org/)*

Notepad++ is a free/libre source code/text editor for Windows that is deeply customizable to fit your needs. It features syntax highlighting for dozens upon dozens of languages and also has [plugin support](https://github.com/notepad-plus-plus/nppPluginList) for all sorts of things such as a Markdown viewer and encryption/decryption.

>Install with...  
Choco: `choco install notepadplusplus`  
winget: `winget install -e --id Notepad++.Notepad++`

### *[GNU Emacs](https://www.gnu.org/software/emacs/)*

GNU Emacs is an absurdly capable Lisp interpreter which goes beyond just being a simple text editor, but a self-contained "operating system", so to speak as well. It is highly extensible and customizable piece of software which is multiplatform and available to use anywhere, though ideally you'd want to use it on a GNU/Linux installation. org-mode is another very important component of GNU Emacs which serves as note-taking, checklisting, authoring, etc.

>Install with...  
Choco: `choco install emacs`  
winget: `winget install -e --id GNU.Emacs`

### *[vi/Vim](https://www.vim.org/)*

Speaking of configurable text editors, it's impossible to omit vi/Vim. With a very steep learning curve especially if you're not used to keyboard-centric editors, once you do get used to it you'll want those vi/Vim keybindings on any other editors, hence the dozens and dozens of keybind integrations in various editors and IDEs. Definitely not recommended for beginners who just want to modify a small config file or casually write text, but recommended to those who want to check out a touted editor.

>Install with...  
Choco: `choco install vim`  
winget: `winget install -e --id vim.vim`

### *[Visual Studio Code](https://code.visualstudio.com/)*

Somehow, Microsoft were able to make a genuinely great piece of software that's free and open source (and is also used to write this very document!). Despite being made using the abhorrent Electron framework, it somehow outperforms other software made with it, yet is still filled with tons of great features and good plugin library that's easy to access.

>Install with...  
Choco: `choco install vscode`  
winget: `winget install -e --id Microsoft.VisualStudioCode`

## **Multimedia**

## *Music*

### *[SoulseekQT](http://www.slsknet.org/)  /  [Nicotine+](https://nicotine-plus.org/)*

Soulseek is a peer 2 peer filesharing network and probably one of the best ways to obtain lossless or stupidly obscure music without having to do a blood sacrifice and study for a private tracker that will kick you out if you show up to your IRC invite interview a microsecond too late. It's a pretty large community (albeit not as large as it was back in its heyday) and there's tons of stuff to be found (sometimes even beyond music). The network operates on the concept of "shares" - publicly make your music library folder available for others on the network to access and others will do the same with theirs as well. The mantra here is "sharing is caring". The Soulseek network can be accessed with clients such as [SoulseekQT](http://www.soulseekqt.net/news/node/1) which has a QT interface or [Nicotine+](https://nicotine-plus.org/) alternatively using the GTK toolkit. VPN usage is advised, preferably with port-forwarding, due to some ~~wankstain~~ elitist users using plugins for publicly displaying users' IP's in their bios for shaming purposes.

>Install with...  
Choco: `choco install soulseek`  

### *[MusicBee](https://getmusicbee.com/downloads/)*

MusicBee is a Windows music player and library organizer similar to iTunes, but without any service integration and completely using your own curated library. Heavy emphasis on customizability ala Winamp via all kinds of available skins, UI adjustment options, and general things to make your library swaggy. Supports playback of all kinds of formats, even old school tracker program formats such as ImpulseTracker .IT and ScreamTracker .s3m files. MusicBee also has some super neat features like auto-playlist which are continualy-updated playlists based on a ruleset (unbelievably powerful feature for library organization) and synchronization with your DAP/phone with transcoding on the fly.

>Install with...  
Choco: `choco install musicbee`

### *[MP3Tag](https://www.mp3tag.de/en/)*

MP3Tag is very capable Windows freeware which takes care of audio file metadata tags. Despite the name, it allows you to edit all sorts of file types such as FLAC, OGG, Opus, M4A, etc. There's also batch editing and scripting which lets you automate tagging based on conditions, as well as metadata fetching from sources like Discogs.

>Install with...  
Choco: `choco install mp3tag`  
winget: `winget install -e --id Mp3tag.Mp3tag`

### *[MusicBrainz Picard](https://picard.musicbrainz.org/)*

MP3Tag, but for perfectionists. It's another audio metadata editor, but this one in particular is open-source and uses the highly-curated MusicBrainz database as its source. Useful features include AcousticID identification for files that do not already have tags written in them, album art fetching from the MB database and plugin support which makes Picard more extensible. Also make sure to grab this plugin which easily lets you submit metadata for a release which isn't present in the database (such as your own music, for example). It'll make the tagging experience of others much easier!

>Install with...  
Choco: `choco install picard`  
winget: `winget install -e --id MusicBrainz.Picard`

### *[beets](https://github.com/beetbox/beets)*

beets is a stupid powerful commandline-based music library organizer written in Python. In my particular use case, beets is scripted to run via a simple PowerShell script which scans a dedicated "for import" folder with Slsk downloads that have been fed thru Picard, then takes these files and imports them to my music library following a specifically formatted folder structure in order to make everything look neat, tidy and easy to navigate. During import, beets will run the files through another MusicBrainz check in order to make sure all of the tags are correct and nothing is missing. During this entire process, the program also creates a .db file which hosts a record of the entire database and can be explored in commandline. The way I utilize beets barely scratches the surface of what it's capable of doing and how extensible it is via plugins (such as one which embeds a BPM tag in which you tag along to your track's tempo in commandline). Takes a bit to set up, but an absolute essential for anyone with a music library which is slowly getting hard to manage.

>Install with...  
Choco: `choco install beets`  
pip: `pip install beets`

### *[fre:ac](https://www.freac.org/)*

// todo

>Install with...  
Choco: `choco install freac`

### *[foobar2000](https://www.foobar2000.org/)*

// todo

>Install with...  
Choco: `choco install foobar2000`  
winget: `winget install -e --id PeterPawlowski.foobar2000`

### *[spek](http://spek.cc/)*

// todo

>Install with...  
Choco: `choco install spek`  
winget: `winget install -e --id AlexanderKojevnikov.Spek`

### *[Exact Audio Copy](https://www.exactaudiocopy.de/)*

// todo

>Install with...  
Choco: `choco install eac`  
winget: `winget install -e --id AndreWiethoff.ExactAudioCopy`

### *[DeltaWave](https://deltaw.org/)*

// todo

>Install with...  
Binary: `https://deltaw.org/DeltaWaveSetup.zip`

## *Video*

### *[mpv](https://mpv.io/) / [mpv.net](https://github.com/stax76/mpv.net)*

// todo

>Install with...  
Choco: `choco install mpv` / `choco install mpvnet.install`

### *[HandBrake](https://handbrake.fr/)*

// todo

>Install with...  
Choco: `choco install handbrake`  
winget: `winget install -e --id HandBrake.HandBrake`

### *[ffmpeg](https://ffmpeg.org/)*

// todo

>Install with...  
Choco: `choco install ffmpeg`

### *[yt-dlp](https://github.com/yt-dlp/yt-dlp)*

// todo

>Install with...
Choco: `choco install yt-dlp`
