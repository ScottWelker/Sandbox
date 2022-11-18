[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Apple](/Tech-Ref/Apple-Inc) | [Tech Ref](/Tech-Ref) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)) | [OS](/Tech-Ref/OS-\(Operating-System\)) | [Mac (Macintosh)](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\))
**Disambiguation:** [Linux](/Tech-Ref/Linux), [Windows](/Tech-Ref/Microsoft/Microsoft-Windows), [Unix](/Tech-Ref/Unix).

[[_TOC_]]

---
# Introduction
|:warning: CAUTION!|
|:-|
| This page started life related to macOS 11 '_Big Sur_'. [I (SWelker)](/Individuals/Scott-Welker) am now using macOS 12 '_Monterey_' but, I don't have enough [Mac](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\)/macOS) experience to know whether anything here is specific to one version or the other. |

"_***macOS*** macOS (previously Mac OS X and later OS X) is a proprietary graphical operating system developed and marketed by [Apple Inc](/Tech-Ref/Apple-Inc). since 2001. It is the primary operating system for [Apple's](/Tech-Ref/Apple-Inc) Mac computers. Within the market of desktop, laptop and home computers, and by web usage, it is the second most widely used desktop OS, after [Windows](/Tech-Ref/Microsoft/Microsoft-Windows)._"

## Reference
1. [Wikipedia: MacOS](https://en.wikipedia.org/wiki/MacOS)
1. [StackExchange: Ask Different (Apple and macOS)](https://apple.stackexchange.com/)

---
# Topics
1. [Multi-Tenant Available LoC (Client Project)](/Clients/Apple/FruitCo-\(Apple\)/FruitCo-FnB/FruitCo-FnB-LoC/Multi%2DTenant-Available-LoC).
1. [News Entity Model Update (NEMU)](/Clients/Apple/FruitCo-\(Apple\)/FruitCo-FnB/NEMU-\(News-Entity-Model-Update\)) project.
1. [Setup MacBook Pro Laptop (Cepheid)](/Clients/Cepheid/Infrastructure-\(Cepheid\)/Systems-and-Services-\(Cepheid\)/Setup-MacBook-Pro-Laptop).
1. [Some Project (Amazon)](/Clients/Amazon/AWS-Marketplace/SBUX-and-Containers/Some-Project).

---
# User Interface

## Dock
The macOS ***Dock*** is shown across the bottom of this image, with sub-sections labeled. The Dock combines elements of a traditional applications menu (Launcher) and elements of the traditional running applications (Status) menu. The Dock is customizable and by default it includes items applie does not want you to miss, [Finder](#finder-(~windows-explorer)), Siri, News, Apple Store, Mail, the Safari [web browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser), etc. 
- ![image.png](/.attachments/image-0474a7e3-2490-46e7-8435-9918f0db5d18.png).

## Top-Level Menu Bar & Application Windows
Notice there is only a single top-level `Menu Bar` and it changes to match your application context. This is unlike [Microsoft Windows applications](/Tech-Ref/Microsoft/Microsoft-Windows#new-to-windows%3F) where each has it's own `Menu Bar`. Mac applications share this singular, system-wide `Menu Bar`, with the active application having control over it.
- See also [Graphical User Interface (GUI)](/Tech-Ref/Software-Development/UX-\(User-Experience\)/GUI-\(Graphical-User-Interface\)).
- :warning: The aforementioned `Menu Bar` is not illustrated in this image.
- ![image.png](/.attachments/image-3b29ec97-1e4a-4f28-92ab-ab9717890a67.png)

---
# Components
1. [Zsh (Z shell)](/Tech-Ref/Unix/Zsh-\(Z-shell\)).
1. [User Experience (UX)](/Tech-Ref/Software-Development/UX-\(User-Experience\)).

## Finder (~Windows Explorer)
Finder is the [Windows Explorer](NameMe) equivalent. However, the out-of-the box preferences provide a "_dumbed down_" interface that [I (SWelker)](/Individuals/Scott-Welker) found initially confusing. Consider these updates:
1. `Finder` | `Preferences` 
   - `Show these items on the desktop:`
      - :ballot_box_with_check: `Hard disks
   - `New Finder windows show`:
      - `Macintosh HD` (_or your preferred drive's name_)

### Keyboard Shortcuts
- [16 Finder Shortcuts Every Mac User Should Know](https://www.howtogeek.com/325983/16-finder-shortcuts-every-mac-user-should-know/)

| Activity | Key Combination<br/>([Win KBD on macOS](#windows-keyboard)) | Notes |
|:-|:-|:-|
| Delete selected file| `Win` + `Backspace` | replaces `cmd` + `Delete`|


---
# Tools
1. [Homebrew (Package Manager)](/Tech-Ref/Homebrew-\(Package-Manager\)).

---
# Tips and Tricks

## Fix Disappearing Doc
|:+1: Tip!|
|:-|
| [I (SWelker) ](/Individuals/Scott-Welker) appear to have solved this by positioning the `Dock` left on the screen (`System Preferences`\| `Dock & Menu Bar`, `Position on screen`: `Left`) |

- [How to fix a disappearing Dock on Mac](https://www.chriswrites.com/how-to-fix-a-disappearing-dock-on-mac/#:~:text=Navigate%20to%20%E2%80%9CSystem%20Preferences%E2%80%A6%20%3E,become%20a%20permanent%20onscreen%20fixture.)
   - The following command, issued within a terminal window worked for [me (SWelker)](/Individuals/Scott-Welker):
   `killall Dock`
## Learning Mac OS X Basics
- [Learning Mac OS X Basics](https://apple.com/voiceover/info/guide/_1122.html)

## Mac Keyboard Shortcuts
- [Mac keyboard shortcuts](https://support.apple.com/en-us/HT201236)

## Screen Shots
- See [Windows Keyboard, Activities, Screen Shot (this page)](#screenshot).
- [How to copy an image from Markup?](https://apple.stackexchange.com/a/388700/456056)

## The Mac's Hidden Image 'Markup' Tools
- [Markup (Apple)](/Tech-Ref/Apple-Inc/Markup-\(Apple\)#markup).

## Verify Encryption Status
- [How to determine if your Mac is encrypted](https://uit.stanford.edu/guide/encrypt/faq/encrypted_mac#:~:text=To%20confirm%20the%20encryption%20status,that%20FileVault%20is%20turned%20on.)

To confirm the encryption status of your Mac, navigate to `System Preferences` > `Security & Privacy` > `FileVault`.

If your hard drive is encrypted, the FileVault displays a message saying that FileVault is turned on.
- ![image.png](/.attachments/image-a5e1efa7-df8a-4b32-aaf4-e845202c727d.png)

## Windows Explorer Equivalent (Finder)
- See [Finder (this page)](#finder-(~windows-explorer)).

## Windows Keyboard
|:+1: Tip!|
|:-|
| **04/2022 [SWelker](/Individuals/Scott-Welker):** Subsequent to drafting this section I setup another MacBook Pro. During that setup my Windows keyboard was detected and `mapped`, providing an improved experience. |

You can use the macOS with a [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) keyboard. It's not optimal but it may be useful, especially when you have a ***keyboard, video, and monitor (KVM)*** switch.

- :+1: [Using a Windows keyboard with a Mac](https://edu.gcfglobal.org/en/osxbasics/using-a-windows-keyboard-with-a-mac/1/)
   - `Windows` key is used instead of the `Command` key.
   - `Alt` key is used in place of the `Option` key.
   - ![image.png](/.attachments/image-4d81185d-78e1-425b-8680-1eea6567eb1e.png)

### Cheat Sheet (SWelker's)
- [I've (SWelker)](/Individuals/Scott-Welker) "_roughed out_" this cheat sheet for using the Mac on my Windows keyboard, video, mouse (KVM) switch and [Microsoft Windows](/Tech-Ref/Microsoft/Microsoft-Windows) keyboard.

#### See also VS Code
- [VS Code, Windows Keyboard with macOS](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)#windows-keyboard-with-macos)

#### Key Equivalents
- :+1: The `Control` and `Option` keys are called the "***VoiceOver keys***" or “***VO keys***” for short. They are shown in commands as `VO`, as in `VO-F1`.
   - See [Introducing VoiceOver](https://www.apple.com/voiceover/info/guide/_1121.html#:~:text=You%20enter%20VoiceOver%20commands%20by,%2C%20as%20in%20VO%2DF1.)

| macOS<br/>Key| macOS<br/>Image | Windows<br/>Key |
|:-|:-|:-|
| `Ctl` | ![image.png](/.attachments/image-44f01d28-bbe6-4dd4-b1e7-13f1c1d732f2.png =25x25) | `Ctl` |
| `Option`<br/>sometimes `Alt` | ![image.png](/.attachments/image-e3373812-d634-488e-af0a-cc19582fe31f.png =25x25) | `Alt` |
| `Cmd` | ![image.png](/.attachments/image-93c058ab-6f47-406e-808a-85f7e91a9845.png =25x25) | `Win` |

#### Activities
| Activity | Key Combination<br/>([Win KBD on macOS](#windows-keyboard)) | Notes |
|:-|:-|:-|
| Select Text | <ul><li>Mouse click at the start of the text.</li><li>Press and hold `Sft` key.</li><li>Mouse click at the end of the text.</li></ul> | They way I've always done this on [Microsoft Windows](/Tech-Ref/Microsoft/Microsoft-Windows) proved problematic on the Mac. |
| Move cursor one word | Forward one Word:<br/><ul><li>`Alt` + `Win` + `R arrow`</li></ul>Backward one Word:<ul><li>`Alt` + `Win` + `L arrow`</li></ul>:+1: Adding `Sft` to this selects. | |
| Copy | `Win` + `c` | |
| Paste | `Win` + `v` | |
| Paste plain text | `Alt` + `Win` + `Sft` + v | [Strip Formatting When You Copy and Paste](https://www.makeuseof.com/tag/5-ways-strip-formatting-copy-paste-text/#:~:text=To%20paste%20as%20plain%20text,Windows%2C%20it%20should%20work%20everywhere.) |
| Screen Shot <span id="screenshot"></span>| Full Screen:<br/><ul><li>`Sft` + `Win` + `3`</li></ul>Region:<ul><li>`Sft` + `Win` + `4`</li></ul>Window or Menu:<ul><li>`Sft` + `Win` + `4`, `space bar`</li></ul> | See also: <ul><li>[The Complete Guide to Taking Screenshots and Screen Recordings](https://www.intego.com/mac-security-blog/how-to-shoot-screenshots-on-macos/#:~:text=On%20the%20Mac%2C%20Command-Shift,time%20the%20screenshot%20was%20taken.).</li><li>[Markup (Apple)](/Tech-Ref/Apple-Inc/Markup-\(Apple\))</li></ul>|
| Switch Between Windows | `Win` + `Tab` | |
| Terminal's Cursor Movement | Beginning of line:<br/><ul><li>`Ctrl` + `a`</li></ul>End of  line:<ul><li>`Ctrl` + `e`</li></ul>  |  |

#### Finder Shortcuts
- See [Finder (this page)](#finder-(~windows-explorer)).

### Remap Windows keyboard to match the Mac layout
| :mask: Deprecated! |
|:-|
| **04/2022 [SWelker](/Individuals/Scott-Welker):** Subsequent to drafting this section I setup another MacBook Pro. During that setup my Windows keyboard was detected and `mapped`, providing an improved experience. |

- [How-To: Remap Windows keyboards to match the Mac keyboard layout](https://9to5mac.com/2016/03/17/how-to-remap-windows-keyboard-buttons-match-mac-layout/)
   - :warning: **08/2021 [SWelker](/Individuals/Scott-Welker):** I have not tried this - yet.

## wget Missing
I found no `wget` command. Worse the simple `brew install wget` command that should have installed it gave the error `Error: Unknown command: install`. I could find no help for this. Oddly simply bumbling around I mistakenly entered `brew install` and that command did a bunch of stuff, complained (didn't record the noise). Oddly, after that `brew install wget` worked and I was "_in business_."

## Z shell (Zsh)
- [Zsh, Tips and Tricks](/Tech-Ref/Unix/Zsh-\(Z-shell\)#tips-and-tricks).

### History - Why truncated?
- [Zsh, Tips and Tricks, History, Why Truncated](/Tech-Ref/Unix/Zsh-\(Z-shell\)#why-truncated%3F).

### Prevent Command Recording
- [Zsh, Tips and Tricks, History, Prevent Command Recording](/Tech-Ref/Unix/Zsh-\(Z-shell\)#prevent-command-recording).
