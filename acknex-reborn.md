---
layout: page
title: ACKNEX Reborn
title_nav: ACKNEX Reborn
permalink: /acknex-reborn/
extra_css: /assets/css/acknex-reborn.css
description: Play classic 3D GameStudio A3 games on modern Windows and Linux.

# ---- Edit these -----------------------------------------------------------
version: "Beta 0.3"
download_win64: "https://ricardoreis.net/acknexreborn/ACKNEXReborn-0.3-windows-x64.zip"
download_linux64: "https://ricardoreis.net/acknexreborn/ACKNEXReborn-0.3-linux-x86_64.tar.gz"
discord: "https://discord.gg/Fdz6kjX8Jk"

# Compatible games. `download` is optional; leave it out when there is no
# official download.
games:
  - name: "3D Hunting: Grizzly"
  - name: "3D Hunting: Shark"
  - name: "3D Hunting: Trophy Game"
  - name: "3D Hunting Trophy: Whitetail"
  - name: "Alien Anarchy"
  - name: "Angst: Rahz' Revenge"
  - name: "Black Bekker"
    download: "https://minbekker.itch.io/blackbekker"
  - name: "Der Name des Bruders"
  - name: "Hades 2"
    download: "http://www.espacoinf.com/hades2.htm"
  - name: "Incidente em Varginha"
  - name: "Mr. Pibb: The 3D Interactive Game"
  - name: "Saints of Virtue"
    download: "https://saintsofvirtuex.com/page/download/"
  - name: "Shadow of the Lost Citadel"
  - name: "Skaphander: Der Auftrag"
  - name: "Taco Bell Tasty Temple Challenge"
  - name: "Virus Explosion"

# Screenshots: put the images in /assets/img/ and fill in `src`.
# An entry with an empty `src` shows a placeholder box.
screenshots:
  - src: "/assets/img/acknex_widescreen.png"
    caption: "OpenGL renderer in widescreen"
  - src: "/assets/img/acknex_hardware.png"
    caption: "OpenGL renderer"
  - src: "/assets/img/acknex_software.png"
    caption: "The original software renderer"
  - src: "/assets/img/acknex_launcher.png"
    caption: "The launcher"
---

<div class="ar-hero">
  <p class="ar-tagline">
    Play classic <strong>3D GameStudio A3</strong> games on modern Windows and
    Linux, with widescreen, mouse look and smooth high frame rates.
  </p>
  <span class="ar-badge">{{ page.version }}</span>

  <div class="ar-downloads">
    <a class="ar-btn" href="{{ page.download_win64 }}">
      Download for Windows<small>64-bit &middot; {{ page.version }}</small>
    </a>
    <a class="ar-btn" href="{{ page.download_linux64 }}">
      Download for Linux<small>64-bit &middot; {{ page.version }}</small>
    </a>
  </div>
  <p class="ar-note">
    Games are not included: you need the game's own files.
    Questions and bug reports: <a href="{{ page.discord }}">Discord</a>.
  </p>

  {% include kofi-banner.html %}

  <details class="ar-new">
    <summary>Update {{ page.version | remove: "Beta " }} available: what's new</summary>
    <ul>
      <li><strong>Game videos:</strong> Incidente em Varginha, Alien Anarchy and Saints of Virtue can play their videos from <code>.MPG</code> files, with their own volume setting (see <a href="#game-videos">Game videos</a>).</li>
      <li><strong>Game options:</strong> some games ask about their own options before starting, such as the language, left-handed mouse buttons or skipping the intro.</li>
      <li><strong>Alien Anarchy:</strong> starts in English and plays past the first level.</li>
      <li><strong>Hades 2:</strong> starts with the game's own WASD and mouse controls.</li>
      <li><strong>Mouse:</strong> the sensitivity also sets a game's own mouse speed when mouse look is off.</li>
      <li><strong>New option:</strong> "Don't fall through narrow gaps".</li>
      <li><strong>Starting:</strong> a game can be started by naming its folder (see <a href="#getting-started">Getting started</a>).</li>
    </ul>
  </details>
</div>

ACKNEX Reborn is a native port of the ACKNEX 3 engine, the runtime behind games
made with 3D GameStudio A3 in the late 1990s. It runs those games directly on
today's systems, with no DOS box or Windows 98 needed. You can play them just as
they looked in 1998, or turn on modern graphics and controls.

## Screenshots

<div class="ar-gallery">
{%- for shot in page.screenshots -%}
  <figure>
    {%- if shot.src != "" -%}
    <a href="{{ shot.src | relative_url }}"><img src="{{ shot.src | relative_url }}" alt="{{ shot.caption | escape }}" loading="lazy"></a>
    {%- else -%}
    <div class="ar-shot-empty">Screenshot coming soon</div>
    {%- endif -%}
    <figcaption>{{ shot.caption }}</figcaption>
  </figure>
{%- endfor -%}
</div>

## Features

<div class="ar-features">
  <div class="ar-card">
    <h4>Native Windows and Linux</h4>
    <p>64-bit builds for both.</p>
  </div>
  <div class="ar-card">
    <h4>Two renderers</h4>
    <p>A new OpenGL renderer, or the original software renderer. Switch between them while you play.</p>
  </div>
  <div class="ar-card">
    <h4>Widescreen and any resolution</h4>
    <p>Fill the whole screen, at any window size up to 4K and beyond.</p>
  </div>
  <div class="ar-card">
    <h4>Better graphics</h4>
    <p>Filtered textures, optional ambient occlusion and an adjustable field of view.</p>
  </div>
  <div class="ar-card">
    <h4>Modern controls</h4>
    <p>Mouse look, WASD movement, key rebinding, and joystick look and button bindings.</p>
  </div>
  <div class="ar-card">
    <h4>Smooth at high frame rates</h4>
    <p>Games run at a constant speed on every device.</p>
  </div>
  <div class="ar-card">
    <h4>Fixes for modern computers</h4>
    <p>Issues that only show up on today's computers are fixed, so games play the way they were meant to.</p>
  </div>
  <div class="ar-card">
    <h4>Many compatible games</h4>
    <p>See the <a href="#compatible-games">list below</a>.</p>
  </div>
  <div class="ar-card">
    <h4>Easy launcher</h4>
    <p>Pick a game, choose your options and play.</p>
  </div>
  <div class="ar-card">
    <h4>In-game panel</h4>
    <p>Press <kbd>F11</kbd> while playing to change options.</p>
  </div>
</div>

## Compatible games

These are some of the games known to work. Many other A3 games have been
tested as well, so this is not a complete list: if a game you have isn't
here, try it, and tell us on [Discord]({{ page.discord }}) how it went.

<ul>
{%- for game in page.games %}
  <li>{{ game.name }}{% if game.download %} (<a href="{{ game.download }}">Download</a>){% endif %}</li>
{%- endfor %}
</ul>

Downloads are on each game's own site. ACKNEX Reborn does not include any
game.

## Getting started

1. **Download** the build for your system and extract it to a folder of its
   own, for example `C:\Games\ACKNEX Reborn` or `~/acknex-reborn`.
2. **Start it.** Run `acknexreborn.exe` on Windows, or `acknexreborn` on Linux. It
   opens the launcher.
3. **Pick the game.** On the **Game** tab, press **Browse** next to *Script*
   and choose the game's `.WDL` file. For a game shipped as one archive, choose
   its `.WRS` file under *Archive* instead. The game's folder is filled in for
   you.
4. **Press Run.** Your choices are saved and will be there next time.

For most of the [compatible games](#compatible-games) there is a quicker way:
extract the package into the game's own folder and run `acknexreborn` there.
The game starts straight away. A few games first ask about their own options,
such as the language or skipping the intro.

While playing:

| Key | Does |
|---|---|
| <kbd>F11</kbd> | Opens the in-game panel (you can change this key in the launcher) |
| <kbd>Alt</kbd>+<kbd>Enter</kbd> | Switches between fullscreen and a window |
| <kbd>F10</kbd> | Quits, in most games |

You can also skip the launcher and start a game from its folder:
`acknexreborn GAME.WDL` followed by any of the switches listed below, for example
`acknexreborn GAME.WDL -GL -WS -ML`. For one of the compatible games you can
name its folder instead, from anywhere: `acknexreborn D:\games\hades2`.
Settings from the launcher still apply; switches on the command line win.

## Launcher options

Every option in the launcher also has a command-line switch, shown in
brackets in the launcher and below. The **Command line** box at the bottom of
the launcher shows exactly what will be used. **Reset settings...** puts
everything back to the defaults listed here. Hover over any option in the
launcher for a short description.

<div class="ar-options" markdown="1">

### Game

| Option | Switch | What it does |
|---|---|---|
| Script | `-WDL` | The game's main script (`.WDL`) to run. |
| Archive | `-WRS` | The game's resource archive (`.WRS`), for games shipped as one file. |
| Map | `-WMP` | Loads a different map instead of the one the game names. |
| Data file | `-WDF` | Uses a different data file. Only needed if a game's instructions ask for it. |
| Game folder | | The game's folder. Filled in when you pick a file with Browse. |
| Save path | `-DIR` | Where saved games go. |
| Define | `-D name,value` | Passes a setting to the game. Only needed if a game's instructions ask for it. |
| Error limit | `-E` | Keeps going past this many script errors instead of stopping at the first. |

### Devices

| Option | Switch | What it does |
|---|---|---|
| No sound | `-OS` | Turns off sound effects. |
| No music | `-OM` | Turns off MIDI music. |
| No CD audio | `-OCD` | Turns off CD audio. |
| No audio at all | `-OT` | Turns off all sound and music at once. |
| No joystick | `-NJ` | Ignores any joystick. |
| No mouse | `-NM` | Ignores the mouse. |
| Sound volume | `-SVOL` | Sound effects volume, in percent. Default 100. |
| Music volume | `-MVOL` | Music volume, in percent. Default 100. |

### Display

| Option | Switch | What it does |
|---|---|---|
| Start in a window | `-WND` | Starts in a window instead of fullscreen. **On** by default. |
| Show the console | `-CONSOLE` | Opens a window with the engine's messages. Useful when reporting a problem. |
| Exclusive fullscreen | `-FSEXCL` | Fullscreen changes the monitor's resolution. Off: borderless fullscreen at desktop resolution. |
| Fullscreen as a window | `-FSWIN` | Fullscreen as a borderless window. Use it if the Windows Game Bar or another overlay doesn't appear over the game. |
| No vsync | `-NVSYNC` | Turns off vsync. Very high frame rates can break some games. |
| Frame cap when vsync is off | `-MAXFPS` | Limits the frame rate while vsync is off. Default 500; 0 is no limit. |
| Window size | `-RESW` / `-RESH` | The window's size. Default 1600 &times; 1200. |

### Network

Two players can play games made for network play, over the local network or
the internet.

| Option | Switch | What it does |
|---|---|---|
| Node number | `-NODE` | Starts a two-player game. One player picks node 0, the other node 1. |
| Player name | `-PLAYER` | Your name in a network game. |
| Peer address | `-NETIP` | The other player's address. Leave it empty to find them on the local network. |
| Base port | `-NETPORT` | Both players need the same value. For internet play, open this port and the next one. Default 2300. |

### Demo

Records what you play to `WDLTape.REC` in the game's folder with
**Record a demo** (`-R`), and plays it back with **Replay a demo** (`-P`).

### Enhancements

These options are new in ACKNEX Reborn. Options marked *OpenGL* need the
OpenGL renderer.

**Graphics**

| Option | Switch | What it does | Default |
|---|---|---|---|
| OpenGL renderer | `-GL` | Draws with OpenGL instead of the original software renderer. | On |
| Override the field of view | `-FOV` | Sets the field of view in degrees. The game's own zoom effects stop working. | Off, 90&deg; |
| Widescreen | `-WS` | *OpenGL.* Fills the whole window instead of 4:3 with black bars. | On |
| Stretch the HUD to the widescreen | `-SHUD` | *OpenGL.* Stretches the HUD across the wide view instead of keeping it 4:3. | On |
| Ambient occlusion | `-SSAO` | *OpenGL.* Darkens corners and creases for extra depth. Costs GPU time. Radius and Strength set how far and how dark. | Off |
| Smooth distant textures | `-MIPMAPS` | *OpenGL.* Smooths distant textures and stops shimmering. Uses more memory. | On |
| Smooth fog | `-SMOOTHFOG` | *OpenGL.* Distant surfaces fade into darkness smoothly instead of in bands. | On |
| Show FPS | `-FPS` | Shows the frame rate in the corner of the view. | Off |

**Input**

| Option | Switch | What it does | Default |
|---|---|---|---|
| Mouse look | `-ML` | Turns the view with the mouse, with separate X and Y sensitivity. Some cutscenes that turn the camera may not work. | On |
| Modern WASD movement | `-MI` | The keys set on the Keys tab walk and sidestep, replacing the game's own movement. | On |
| Trigger WASD events | `-MIEV` | W, A, S and D still work for the game's own keys, such as cheats. Turn it off if one of them does something odd while you walk. | On |
| Pin the cursor to the view's centre | `-CURLOCK` | Keeps the cursor on the crosshair, so clicks hit what you face. | Off |

**Timing and physics**

| Option | Switch | What it does | Default |
|---|---|---|---|
| Fixed game speed | `-DETERMINISTIC` | The game runs at a fixed rate, the same on every computer. | On |
| Steps per second | `-SIMHZ` | Higher is smoother. | 32 |
| Smooth movement between steps | `-INTERP` | Smoother motion on high refresh rate displays. | On |
| Fix texture animation speed | `-FCD` | Animated textures run at their intended speed, not as fast as the frame rate. | On |
| Fix jumps and falls | `-FVZ` | Jumps and falls behave the same at any frame rate. *Jump and fall strength* adjusts them. | Off, 400% |
| Fix walking through walls at corners | `-FWALL` | Stops the player slipping through walls at some corners. | On |
| Don't fall through narrow gaps | `-FEDGE` | Stops the player falling into gaps narrower than they are. | Off |

**Compatibility**

| Option | Switch | What it does | Default |
|---|---|---|---|
| CD music from .ogg files | `-OGGCD` | Plays `track2.ogg`, `track3.ogg`... from the game's folder instead of the CD. | On |
| Play game videos | `-VIDEOS` | Plays a game's videos from `.MPG` files in its folder. Any key skips. | On |
| Video volume, percent | `-VVOL` | Volume of the game videos' sound. | 100 |
| Load game patches | `-PATCH` | Applies ACKNEX Reborn's fixes for some games. | On |
| Engine default keys | `-IWDL` | Adds standard keys such as <kbd>F10</kbd> to quit, unless the game uses them itself. | On |
| Support games for engine V3.680 | `-V368` | Lets games made for the older V3.680 engine load. | On |
| Support games for engine V3.56 | `-V356` | Lets games made for the older V3.56 engine load. | On |
| Support games for engine V3.08 | `-V308` | For some games from 1995. Known games turn it on by themselves; leave it off for others. | Off |

Some games need particular settings to work, for example with mouse look off.
ACKNEX Reborn recognises these games and applies those settings for you.

### Keys

| Option | What it does | Default |
|---|---|---|
| Open the in-game panel | The key that opens the in-game panel. | <kbd>F11</kbd> |
| Modern WASD movement keys | Walk forward, walk backward, strafe left, strafe right. Used when *Modern WASD movement* is on. | <kbd>W</kbd> <kbd>S</kbd> <kbd>A</kbd> <kbd>D</kbd> |
| Key rebinding (`-REBIND`) | A list of rows, each making one key or mouse button also press another. The key you press keeps doing what it did before. | On |

The **...** button next to a key lets you press the key instead of choosing it
from the list (Windows only). The default rebinding rows give most games
modern controls:

| Press | Also presses | Usually means |
|---|---|---|
| <kbd>Space</kbd> | <kbd>Home</kbd> | Jump |
| <kbd>C</kbd> | <kbd>End</kbd> | Duck |
| <kbd>E</kbd> | <kbd>Space</kbd> | Use / open |
| <kbd>F</kbd> | <kbd>E</kbd> | Whatever <kbd>E</kbd> did before |
| Left mouse button | <kbd>Ctrl</kbd> | Fire |

### Joystick

| Option | Switch | What it does | Default |
|---|---|---|---|
| Turn the view with the stick | `-JL` | Turns the view with a second stick. | Off |
| Look axis X / Y | `-JLAX` / `-JLAY` | Which axes turn the view. | 3 and 4 |
| Yaw / Pitch speed | `-JLX` / `-JLY` | 100% is one full turn a second with the stick pushed all the way. | 100% |
| Deadzone | `-JLDZ` | Ignores small stick movements near the centre. | 8% |
| Invert pitch | `-JLINV` | Flips up and down. | Off |
| Strafe instead of turning | `-JSTRAFE` | Pushing the stick left or right sidesteps instead of turning. Use it with joystick look or mouse look. | Off |
| Strafe axis X / Y | `-JSAX` / `-JSAY` | Which axes walk and sidestep. | 0 and 1 |
| Joystick bindings | `-JBIND` | A list of rows, each making a button or trigger press a key. A trigger counts as an axis: pick *Axis +* and its number. | Off |

When joystick bindings are turned on, the default rows are: right trigger
presses <kbd>Ctrl</kbd>, the bottom face button presses <kbd>Space</kbd>, and
the left face button presses <kbd>E</kbd>. To find a stick's axis and button
numbers, open the in-game panel's **Joystick** tab, which shows each axis and
button live.

</div>

## The in-game panel

Press <kbd>F11</kbd> while playing to open the panel. It has most of the
launcher's options, and changes apply right away. They are saved for the
next time you play.

## Troubleshooting

<div class="ar-faq" markdown="1">

<details markdown="1">
<summary>The Run button is greyed out</summary>

Choose the game first: on the **Game** tab, use **Browse** to pick the game's
`.WDL` script or `.WRS` archive.
</details>

<details markdown="1">
<summary>"The script name is longer than 12 characters"</summary>

Use **Browse** rather than typing a path: it puts just the file name in the
box and the folder in *Game folder*.
</details>

<details markdown="1">
<summary>Windows warns that the program is from an unknown publisher</summary>

The beta builds are not signed yet; the warning does not mean anything harmful
was found.

- Choose **More info**, then **Run anyway**.
- Or, before unpacking, right-click the downloaded `.zip`, choose
  **Properties**, tick **Unblock** and press **OK**. Files unpacked from it
  will then start without the warning.
</details>

<details markdown="1">
<summary>Windows Defender or another antivirus removes or blocks the program</summary>

This is a false alarm.

- Download ACKNEX Reborn only from this page or [Discord]({{ page.discord }}).
- Restore the file from quarantine (Windows Security > Virus & threat
  protection > Protection history) and allow it.
- You can report the false alarm to Microsoft at
  <https://www.microsoft.com/wdsi/filesubmission>, and let us know on Discord
  so we can follow it up.
</details>

<details markdown="1">
<summary>On Linux, nothing happens when I start it</summary>

- Make sure the file is executable: `chmod +x acknexreborn`.
- Start it from a terminal to see any error message.
- The launcher needs GTK 3, which most desktops already have. You can also
  skip the launcher and start a game directly: `./acknexreborn GAME.WDL`.
</details>

<details markdown="1">
<summary>The game stops with a script error while loading</summary>

- Check that *Support games for engine V3.680* and *V3.56* are on
  (Enhancements tab). Many older games need one of them. For a game from
  1995, also try *V3.08*.
- If the game still stops, turn on *Error limit* on the Game tab and set it
  to a few errors, so the game keeps going past them.
- Please report the game on Discord, with the error message.
</details>

<details markdown="1">
<summary>A cutscene freezes, or the camera doesn't turn when the game wants it to</summary>

Turn off *Mouse look*, and *Modern WASD movement* if the controls also feel
wrong.
</details>

<details markdown="1">
<summary>The controls don't match the game's instructions</summary>

*Modern WASD movement* and *Key rebinding* change the controls on purpose. To
play with the game's original controls, turn both off. To change a single
key, edit the rows on the **Keys** tab.
</details>

<details markdown="1">
<summary>A cheat or a typed word doesn't work</summary>

Make sure *Trigger WASD events* is on (Enhancements tab), or turn *Modern WASD movement* off.
</details>

<details markdown="1">
<summary>The game runs too fast, or animations are too fast</summary>

Keep *Fixed game speed* and *Fix texture animation speed* on, and leave vsync
on (*No vsync* off). If you turned vsync off, set
*Frame cap when vsync is off* to a normal value such as 144.
</details>

<details markdown="1">
<summary>Jumps are too high or too low</summary>

Turn on *Fix jumps and falls* (Enhancements tab) and adjust *Jump and fall
strength*. You can do this live in the in-game panel (<kbd>F11</kbd>) to find
the right value for a game.
</details>

<details markdown="1">
<summary>Widescreen, ambient occlusion or other graphics options are greyed out</summary>

Those options only work with the *OpenGL renderer*. Turn it on first.
</details>

<details markdown="1">
<summary>I can't open the Windows Game Bar</summary>

Turn on *Fullscreen as a window* (Display tab).
</details>

<details markdown="1">
<summary>The game stutters or runs slowly</summary>

- Turn off *Ambient occlusion*, which costs the most.
- Try a smaller window size, or turn off *Smooth distant textures*.
- Update your graphics driver.
- If it happens only in OpenGL, try the original software renderer (turn
  off *OpenGL renderer*).
</details>

<details markdown="1">
<summary>There is no music</summary>

- For MIDI music, keep `FluidR3_GM.sf2` in the same folder as `acknexreborn`.
- For CD music, copy the CD's audio tracks into the game's folder as
  `track2.ogg`, `track3.ogg` and so on (the same numbers as on the CD), and
  keep *CD music from .ogg files* on.
- Check that *Music volume* is above 0 and that *No music* and *No audio at
  all* are off.
</details>

<details markdown="1">
<summary>Mouse clicks miss what I'm aiming at</summary>

Turn on *Pin the cursor to the view's centre*, so clicks land on the
crosshair while mouse look is on.
</details>

<details markdown="1">
<summary>Two-player games can't find each other</summary>

- One player must be node 0 and the other node 1.
- Both must use the same *Base port*.
- Enter the other player's address, or leave it empty on the same local
  network.
- Allow the program through your firewall (it uses UDP).
</details>

<details markdown="1">
<summary>I changed too many settings and want to start over</summary>

Press **Reset settings...** in the launcher. Your settings are stored in
`wwrun.cfg` next to the program; deleting that file does the same.
</details>

<details markdown="1">
<summary>The game crashed</summary>

Note the message in the crash window, turn on *Show the console* on the
Display tab, and try again. Then report it on
[Discord]({{ page.discord }}) with the game's name, what you were doing and
what the console showed.
</details>

</div>

## Game videos

Some games' videos have to be converted to `.MPG` files before ACKNEX Reborn
can play them. Put the files in the game's folder. Any key skips a video.

| Game | Files |
|---|---|
| Incidente em Varginha, Alien Anarchy | `INTRO01.MPG`, `INTRO02.MPG`, `END01.MPG` |
| Saints of Virtue, Saints of Virtue X | `INTRO.MPG` |

### Making the files

The videos must come from your own, legally obtained copy of the game. They are
usually in the game's original installation or distribution files: Smacker
(`.SMK`) files, video EXEs, or other containers.

With [FFmpeg](https://ffmpeg.org), convert each video like this, keeping its
name:

```
ffmpeg -i INTRO01.SMK -c:v mpeg1video -q:v 5 -c:a mp2 -b:a 128k -ar 44100 -f mpeg INTRO01.MPG
```

Or upload the files to an AI assistant that can process files, and ask it to:

- Look for standalone Smacker (`.SMK`) files, but also inspect EXEs and other
  files for embedded videos.
- Not assume a format: games may use Smacker, Bink, AVI, MPEG or other old
  formats.
- Check the actual video stream before extracting it, since EXEs may contain
  false signatures or several matches.
- Extract the complete video and convert it to MPEG-1 video (`mpeg1video`) in
  an `.mpg` file, with MP2 audio.
- Keep the original resolution and aspect ratio.
- Resample the audio or change the frame rate only when MPEG-1 needs it.
- Check with FFprobe that the final video codec really is `mpeg1video`.
- Keep the original name where possible: `INTRO01.SMK` or `INTRO01.EXE` becomes
  `INTRO01.mpg`.
- Put all the converted files in a ZIP if there are several.

Then put the `.mpg` files in the game's main folder.

These files are for your personal use. ACKNEX Reborn does not distribute them,
and ACKNEX Reborn, its developers and contributors are not responsible for
unauthorised or illegal redistribution of copyrighted game files.

## About

<div class="ar-about" markdown="1">

ACKNEX 3 (3D GameStudio 3) is (C) oP group Germany GmbH.

ACKNEX Reborn is developed and maintained by Ricardo Reis, with permission
from Johann Christian Lotter (oP group).

ACKNEX Reborn is free. It may not be sold, or included with anything that
is sold, without permission. The games it runs belong to their owners, and
ACKNEX Reborn includes none of them.

Special thanks to:

Johann Christian Lotter, creator of ACKNEX / 3D GameStudio, and the entire
ACKNEX Reborn community.

Third-party software:

- SDL 3 - zlib License
- SDL_mixer - zlib License
- TiMidity - Artistic License
- stb_vorbis - MIT License
- TinySoundFont - MIT License
- PL_MPEG - MIT License
- Dear ImGui - MIT License
- libui-ng - MIT License
- FluidR3_GM SoundFont, by Frank Wen and Toby Smithe - MIT License

Website: [https://rickomax.github.io/acknex-reborn](https://rickomax.github.io/acknex-reborn)<br>
Discord: [{{ page.discord }}]({{ page.discord }})<br>
oP group: [https://www.opgroup.de](https://www.opgroup.de)<br>
Support the project: [https://ko-fi.com/{{ site.kofi_username }}](https://ko-fi.com/{{ site.kofi_username }})

</div>
