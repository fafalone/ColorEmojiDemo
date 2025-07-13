**NOTE** - A similar but much more useful project based on this code now exists-- I turned this concept into a full-featured Label control: [ColorFontLabel](https://github.com/fafalone/ColorFontLabel), which can be used as a tbcontrol in project or compiled into an ocx for VBA and VB6.

<img width="284" height="61" alt="462729117-1b239fa8-4d44-44eb-9e56-cb1737d2091c" src="https://github.com/user-attachments/assets/8ee9161d-32df-4ab0-82a9-5c37e1d4519c" />


# ColorEmojiDemo
twinBASIC DirectX Color Emoji Demo

![image](https://github.com/fafalone/ColorEmojiDemo/assets/7834493/eb559c48-a58c-4d63-a4bf-084552cbd274)

Unfortunately the basic Windows GDI functions don't support colored fonts, so even if you have Unicode-supporting controls, your emojis would only show in black and white, just like when you paste them in Windows Explorer. This is a simple demo that shows how to use Direct2D and DirectWrite to display emojis in color. It's mostly based on [this C++ example](https://stackoverflow.com/a/71640767/6065864) by Code Doggo; for simplicity, I render it directly onto a Form rather than create my own window, which would be less useful for tB programmers anyway. There's limited use in this current forum, the ultimate goal here would be to turn this into an edit control.

## Updates

**Update (04 Jul 2025):** Updated to remove Public Consts now treated as errors and update to linked newer WDL version to clear (irrelevant to this project) package bug now treated as an error.

**Update (03 Mar 2024):** .twinproj has been updated to use a more recent version of WinDevLib (formerly tbShellLib) due to errors in the package tB did not raise at the time this project was released.

**Update (19 Dec 2023):** .twinproj updated to reference WinDevLib (formerly tbShellLib) 7.0-- this eliminates package errors that tB did not raise at the time this project was initially released.

**Update (12 May 2023):** Project updated to use new public current version of tbShellLib; it previously used a private version that different from the current public release. If you had issues with this in a new project, simply update the tbShellLib reference.

## Requirements

Officially, colored fonts are only supported on Windows 8 and newer. If you have the proper updates installed, it *may* work on 7, but if it doesn't, since MS says it can't at all, I wouldn't be inclined to go crazy trying to find the exact steps.

twinBASIC Beta 299 or newer is reommended to compile; older versions will only work when compiled.

This requires my tbShellLib package, version 4.6.142 or higher, to be added to your project, if you're starting a new one (it's already included in the .twinproj file here). 

There's no external dependencies.

## Other versions

There's also a VB6 version of this project, using oleexp.tlb instead of tbShellLib

[[VB6/Win8+] Using DirectX to show emojis with color](https://www.vbforums.com/showthread.php?899901-VB6-Win8-Using-DirectX-to-show-emojis-with-color)
