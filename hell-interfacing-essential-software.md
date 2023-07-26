# **HELL INTERFACING ESSENTIAL SOFTWARE**

// Revision 1, 7.26.2023 //

This list will attempt to prioritize open source and FOSS software, though if need be, proprietary software will be included as well.

## **Navigation**

- [Operating Systems](#operating-systems)
- [Package Managers](#package-managers)
- [Web Browsers](#web-browsers)
- [Utilities](#utilities)
- [Programming](#programming)
- [Multimedia - Music](#music)
- [Multimedia - Video](#video)

## **Operating Systems**

### *[Windows 10 (Modified)](https://www.microsoft.com/de-de/software-download/windows10)*

Underneath the TONS and TONS of Bill Gates turbo AIDS, there's a perfectly capable OS in here for the common man. You have to jump through quite a bit of hoops to get this thing clean for personal use if you're using the standard consumer ISO image, but once you do so, there isn't any debate - it's a good OS. As mentioned earlier, only download official ISOs from the Microsoft site instead of some Indian "Super Tech 64" Blogspot sites and activate with HWID or the [Microsoft-Activation-Scripts](https://github.com/massgravel/Microsoft-Activation-Scripts). Note that in order to get the ISO download on the site instead of the Media Creation Tool, you'll have to change your browser's User-Agent to either Linux or macOS. Post-installation you'll want to use something like Sycnex's [Windows10Debloater](https://github.com/Sycnex/Windows10Debloater) and run either the commandline PowerShell script or the GUI version. Further optimizations or scripts should not be necessary unless you want to break something system dependency, but it should be noted that despite how many tools and PowerShell GitHub scripts you throw at an installation, you won't get away from the botnet. However...

### *[Windows 10 AME](https://ameliorated.info/)*

...you can instead get a version of Windows 10 named [Ameliorated](https://ameliorated.info/). This modified installer of Windows 10 removes a ton of the pre-installed bloatware, minimizes install time, eliminates things such as Windows Update and Cortana and removes many of the telemetry that Microsoft added. The changelist is massive and it is recommended to read up on AME yourself, or better yet, test drive it in a VM or a computer you might have lying around doing nothing. As mentioned earlier, it is highly recommended against downloading a random ISO image and installing it on bare metal, but the nice thing about AME is that it's also a handbook that teaches you how to ameliorate a clean Windows 10 ISO yourself using what they call "playbooks" which are scripts that allow you to batch modify aspects of your installation (think of the way GNU/Linux handles distributions). It takes a while, and ultimately it should be noted that debloating and despooking a proprietary closed-source OS like Windows might be pointless and you're better off using GNU/Linux unless your use case explicitly requires Windows.

### *[GNU/Linux](https://www.gnu.org/gnu/linux-and-gnu.en.html)*

You knew this was coming. If you really, really love tinkering with your computer and want to immerse yourself in a new environment where knowledge of the inner workings of your OS and a lot of the installed software is incredibly useful, GNU/Linux might be for you. It's a vast world of [distributions](https://distrowatch.com/) which ranges from noob-friendly "Windows replacements" like [Linux Mint](https://linuxmint.com/) to l33t h4x0r + Mental Luke Smith Outlaw cunny-connoisseur distro like [Arch Linux](https://archlinux.org/). Speaking of Arch, appreciate the [ArchWiki](https://wiki.archlinux.org/) as it will be your most referred-to website once you start using GNU/Linux due to how informative and widely applicable to various distros it is. Grab an ISO of whichever distro interests you and fire it up in a VM or install it on a Live USB and test drive it on your computer without having to install anything.

A quickfire list of recommended distros, (somewhat) sorted from easiest to hardest:
- [Linux Mint](https://linuxmint.com/)
- [Pop!_OS](https://pop.system76.com/)
- [Manjaro](https://manjaro.org/)
- [Arch Linux](https://archlinux.org/)

## **Package Managers**

An advantage that has been enjoyed by macOS and GNU/Linux users for years has been the concept of a package manager. Bluntly put, it's a piece of software that lets you connect to a central repository where other software is hosted and with it you can install applications within your commandline or a GUI "App Store" without the need to look for individual .exe's or any installer binaries yourself. A package manager can also batch update your installed software with a single command which is a selling point alone. The problem is that these repositories host mostly open-source software only and very rarely would you find closed-source, proprietary programs (but then again, you might be better off without them if there's a good open-source alternative instead). Package managers are rather diverse and rabbit holes on their own, but here's a rundown on some Windows-based ones to get your feet wet with:

### *[Chocolatey](https://chocolatey.org/)*

Choco is probably the largest package manager on Windows so far. It's super simple to install and figure out how to use it, especially if you have former package manager knowledge. On the website there is a ["search packages" function](https://community.chocolatey.org/packages) which will let you scour the entire repo and copy the install commands to paste into your commandline. The community is pretty large and the project seems to be in constant support, perhaps moreso than even Microsoft's own package manager winget.

### *winget*

In response to the surge in popularity that package managers have been receiving over the past couple of years, Microsoft responded with winget. It is included by default with Windows 11 and also available through Windows 10's 1709 version. It supposedly does what it says on the tin, but I personally have not used it and cannot speak for its quality especially compared to Chocolatey. Similarly to Choco's package repository search tool, there's also [winget.run](https://winget.run/) to browse the winget repo and conveniently copy commands.

On GNU/Linux, it should be noted that the family tree your distribution belongs to will have a common package manager, meaning for example Linux Mint being based on Ubuntu will use the `apt` package manager, Manjaro being Arch-based will use `pacman`, etc. For the most part you'll be stuck with one main package manager on your distro for stability reasons, but there are more advanced ones such as [Nix](https://nixos.wiki/wiki/Nix_package_manager) and [Guix](https://guix.gnu.org/). Arch Linux benefits from having the community-maintained Arch user repository (AUR) which is a selling point alone on using Arch due to how much software there is on it, sometimes even Windows software pre-wrapped in a compatibility layer to work out of the box.

## **Web Browsers**

### *[Mozilla Firefox](https://www.mozilla.org/en-US/firefox/download/thanks/)*

By now everyone should know what Firefox is, and despite Mozilla's [incomprehensibly dumb actions](https://blog.mozilla.org/en/mozilla/we-need-more-than-deplatforming/) over the recent years, this is still a fine browser that competes with the Chromium cancer that's infesting every other contemporary browser out right now. While it is factually slower in some use cases over Chrome or Edge, its extensibility and customization gives it a real advantage that you should consider when picking a browser. It is recommended to spin up an userprofile with [Firefox Profilemaker](https://ffprofile.com/) upon a fresh install which will eliminate some of the telemetry and more annoying features that you'd have to manually disable in `about:config`.

### *[ungoogled-chromium](https://github.com/Eloston/ungoogled-chromium)*

ungoogled-chromium is a modification of Google Chromium which removes pretty much all of the features that phone back home to Google (even in normal Chromium). It does not allow the use of a Google account due to the stripped Google account integration. You might have to spend some time configuring its `chrome://settings` to your liking and enable things like saving cookies and site data upon closing of the browser, as such features are disabled by default for privacy reasons. Consult the [wiki](https://ungoogled-software.github.io/ungoogled-chromium-wiki/) for further information.

## **Utilities**

### *[Everything](https://www.voidtools.com/)*

Everything is an incredibly fast and lightweight file search engine for Windows which indexes your drives and monitors for changes to keep its index up to date. It also allows for Regex and advanced searches based on file metadata for extremely precise searches. It is recommended to exclude the Windows install folder by default as files within that directory could clog up your search results pretty often.

### *[7zip](https://www.7-zip.org/)*

7zip is a free and open source file archiver which can extract and pack compressed files like ZIP, 7Z, TAR, XZ, etc. It should be noted that RAR is only supported in a "read-only" mode, meaning that 7zip cannot create or modify RAR files. Still, 7Z as an archive format should be preferred due to its better compression and efficiency.

### *[HWiNFO](https://www.hwinfo.com/)*

HWiNFO is a Windows application which gives you extremely detailed information on your hardware and what it's currently doing. Think of Speccy, but on steroids. The program includes a sensor monitor which gives you a great view on every single aspect of your computer's hardware as well as a logger to monitor changes over time.

### *[QTTabBar](http://qttabbar.wikidot.com/)*

QTTabBar gives you more control over customizing the Windows File Explorer by enabling tabs and changing Explorer's behaviour like double-clicking on an empty space to have you go up a directory. It's small stuff, but once you're used to it, there's no going back.

### *[JDownloader 2](https://jdownloader.org/jdownloader2)*

Open-source download manager written in J*va. Works great for batch downloading and queuing a bunch of links for sequential download. Supports all kinds of sites and allows logins for various premium file hosting services. This is what I personally use for downloading stuff from Archive.org. Because J**a sucks, the program feels slow, clunky and heavy, but otherwise works good.

### *[Bulk Crap Uninstaller](https://www.bcuninstaller.com/)*

Free and open source bulk uninstaller for Windows featuring leftover file deletion. It's capable of detecting and removing Microsoft Store applications, Steam installs and Windows Features. Recommended over the more well-known alternative Revo Uninstaller which is proprietary and freemium.

## **Programming**

### *[Notepad++](https://notepad-plus-plus.org/)*

Notepad++ is a free/libre source code/text editor for Windows that is deeply customizable to fit your needs. It features syntax highlighting for dozens upon dozens of languages and also has [plugin support](https://github.com/notepad-plus-plus/nppPluginList) for all sorts of things such as a Markdown viewer and encryption/decryption.

### *[GNU Emacs](https://www.gnu.org/software/emacs/)*

GNU Emacs is a fully capable Lisp interpreter which goes beyond just being a simple text editor, but a self-contained "operating system", so to speak as well. It is highly extensible and customizable piece of software which is multiplatform and available to use anywhere, though ideally you'd want to use it on a GNU/Linux installation. org-mode is another very important component of GNU Emacs which serves the functions note-taking, checklisting, authoring, etc. Community spinoffs such as [Doom Emacs](https://github.com/doomemacs/doomemacs) and [Spacemacs](https://www.spacemacs.org/) are worth considering if you've never used Emacs before, as they are far more user-friendly and featurefull with things that most users nowadays would seek in an editor and development environment out of the box.

### *[vi/Vim](https://www.vim.org/)*

Speaking of configurable text editors, it's impossible to omit vi/Vim. With a very steep learning curve especially if you're not used to keyboard-centric editors, once you do get used to it you'll want those vi/Vim keybindings on any other editors, hence the dozens and dozens of keybind integrations in various editors and IDEs. Definitely not recommended for absolute beginners who just want to modify a small config file or casually write text, but recommended to those who want to check out a touted editor and try something new that can be utilized in a console environment.

### *[Visual Studio Code - Open Source (Code - OSS)](https://github.com/Microsoft/vscode)*

Somehow, Microsoft were able to make a genuinely great piece of software that's free and open source. It's a fully featured IDE with a plugins repository, version control via Git and user-friendly UI that is easy to navigate. Code - OSS is highly preferred over the standard Visual Studio Code release by Microsoft as it is the base development release stripped of any telemetry that is added downstream by M$.

## **Multimedia**

## *Music*

### *[Nicotine+](https://nicotine-plus.org/)*

Soulseek is a peer 2 peer filesharing network and probably one of the best ways to obtain lossless or stupidly obscure music without having to do a blood sacrifice and study for a private tracker that will kick you out if you show up to your IRC invite interview a microsecond too late. It's a pretty large community and there's tons of stuff to be found (sometimes even beyond music). The network operates on the concept of "shares" - publicly make your music library folder available for others on the network to access and others will do the same with theirs as well. The mantra here is "sharing is caring". The Soulseek network can be accessed with clients such as [SoulseekQT](http://www.soulseekqt.net/news/node/1) which has a Qt interface, but is proprietary or [Nicotine+](https://nicotine-plus.org/) which would be the recommendation here as it is fully open source and highly extensible with many more features than the standard Qt client. VPN usage should be considered, preferably with port-forwarding, due to some ~~wankstain~~ elitist users using plugins for publicly displaying users' IP's in their bios for shaming purposes.

### *[MusicBee](https://getmusicbee.com/downloads/)*

MusicBee is a Windows music player and library organizer similar to iTunes, but without any service integration and completely using your own curated library. Heavy emphasis on customizability via all kinds of available skins, UI adjustment options, and general things to make your library swaggy. Supports playback of all kinds of formats, even old school tracker program formats such as ImpulseTracker .IT and ScreamTracker .s3m files. MusicBee also has some super neat features like auto-playlist which are continualy-updated playlists based on a ruleset (unbelievably powerful feature for library organization) and synchronization with your DAP/phone with transcoding on the fly.

### *[MP3Tag](https://www.mp3tag.de/en/)*

MP3Tag is very capable Windows freeware which takes care of audio file metadata tags. Despite the name, it allows you to edit all sorts of file types such as FLAC, OGG, Opus, M4A, etc. There's also batch editing and scripting which lets you automate tagging based on conditions, as well as metadata fetching from sources like Discogs.

### *[MusicBrainz Picard](https://picard.musicbrainz.org/)*

MP3Tag, but for perfectionists. It's another audio metadata editor, but this one in particular is open-source and uses the highly-curated MusicBrainz database as its source. Useful features include AcousticID identification for files that do not already have tags written in them, album art fetching from the MB database and plugin support which makes Picard more extensible. Also make sure to grab this plugin which easily lets you submit metadata for a release which isn't present in the database (such as your own music, for example). It'll make the tagging experience of others much easier.

### *[beets](https://github.com/beetbox/beets)*

beets is a stupid powerful commandline-based music library organizer written in Python. In my particular use case, beets is scripted to run via a simple shell script which scans a dedicated "for import" folder with Slsk downloads that have been fed thru Picard, then takes these files and imports them to my music library following a specifically formatted folder structure in order to make everything look neat, tidy and easy to navigate. During import, beets will run the files through another MusicBrainz check in order to make sure all of the tags are correct and nothing is missing. During this entire process, the program also creates a .db file which hosts a record of the entire database and can be explored in commandline. The way I utilize beets barely scratches the surface of what it's capable of doing and how extensible it is via plugins (such as one which embeds a BPM tag in which you tap along to your track's tempo in commandline). Takes a bit to set up, but an absolute essential for anyone with a music library which is slowly getting hard to manage.

### *[fre:ac](https://www.freac.org/)*

Free and open-source audio transcoding utility which supports tag editing, CD ripping and signal processing. A good GUI alternative to using ffmpeg to transcode audio if you can't be bothered to use the commandline or make a script for a batch process.

### *[foobar2000](https://www.foobar2000.org/)*

The "it just werks" of music players, foobar2000 is one of the most customizable and light-weight audio players out there. It's unfortunately proprietary and Windows-only, but getting it to work on WINE is very easy and worth doing. Lots of plugins, DSP support including the ability to use VST's in a signal processing chain, etc.

### *[spek](http://spek.cc/)*

Stupid simple open-source spectrum analyser for audio files. No fuss, no nagging, no 15 windows to get to a result. Recommended use is to check if a lossless file is *really lossless*.

### *[Exact Audio Copy](https://www.exactaudiocopy.de/)*

Perfectionist CD ripping software and possibly the only one you'll ever need. If your drive is EAC-friendly the software will make full use of its AccurateRip support to verify that your rips have come out crisp clean and with some metadata.

## *Video*

### *[mpv](https://mpv.io/) / [mpv.net](https://github.com/stax76/mpv.net)*

mpv should be the gold-standard for video players by this point. Out of the box, for super simple video playback, it works great and utilizes very minimal resources, but once you delve deep into configuration, scripting and extensions, it can be *your* video player. For reference [here](https://github.com/nikolamihaylov-hellio/mpv) is my personal configuration which I can easily deplot on a clean installation and have my video player tailored to me out of the box on a fresh installation.

### *[HandBrake](https://handbrake.fr/)*

Free and open-source video transcoding utility based on ffmpeg, therefore having a wide variety of codecs supported. It can also be used as a DVD video ripper and has batch conversion capabilities using a queue system.


### *[ffmpeg](https://ffmpeg.org/)*

You've heard it mentioned multiple times throughout this document already, so chances are you might be slowly figuring out what it is. In case you haven't, ffmpeg is a suite of video and audio libraries and codecs to process media files with. It's commandline-based piece of software that can be tightly integrated into scripts for batch conversion processes which is capable of decoding, encoding, transcoding, muxing, demuxing and streaming all sorts of media. You can even take it as far as making it a screen capturing utility ala OBS due to how powerful it is.


### *[yt-dlp](https://github.com/yt-dlp/yt-dlp)*

The only internet video downloader you should consider using. It's a fork of the now dead [youtube-dl](https://github.com/ytdl-org/youtube-dl) which aims at succeeding it by keeping it maintained and updated with more sites supported. It's commandline-based and with a lot of features useful for archival purposes such as keeping a record of videos you've downloaded, grabbing JSON files and thumbnails, queuing up entire YouTube channels and playlists and more. It should be noted that, despite its name, this software works for many, many more sites beyond YouTube, including most social media like Instagram, Reddit, Twitter, TikTok, etc.