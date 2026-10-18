---
layout: page
title: PIEMulator
title_nav: PIEMulator
permalink: /piemulator/
extra_css: /assets/css/acknex-reborn.css
description: Play the games of Pie in the Sky's 3D Game Creation System, POWER 3D and the engines derived from it on modern Windows and Linux.


# ---- Edit these -----------------------------------------------------------
version: "Beta 0.2"
# Leave a download empty to show "Coming later".
download_win64: "https://ricardoreis.net/piemulator/PIEMulator-0.2-windows-x64.zip"
download_linux64: "https://ricardoreis.net/piemulator/PIEMulator-0.2-linux-x64.zip"
discord: "https://discord.gg/kKvzfqFTJ"

# Screenshots: put the images in /assets/img/ and fill in `src`.
# An entry with an empty `src` shows a placeholder box.
screenshots:
  - src: "/assets/img/piemulator_launcher.png"
    caption: "The game list"
  - src: "/assets/img/piemulator_widescreen.png"
    caption: "OpenGL view in widescreen, with the minimal HUD"
  - src: "/assets/img/piemulator_software.png"
    caption: "The original software renderer"
  - src: "/assets/img/piemulator_editor.png"
    caption: "The GCS level editor"

# Pie in the Sky Software's own games in the game list, each listed once
# (several have more than one release). The page ends the list with
# "Many more...": the games others made with GCS and its engines.
games:
  - name: "3D Game Creation System"
    year: 1995
  - name: "3D Xmas Adventure: Santa's Rescue"
    year: 1996
  - name: "Industrial Killers"
    year: 1995
  - name: "Lethal Tender"
    year: 1993
  - name: "Meltdown"
    year: 1995
  - name: "Stop Nick Macki"
    year: 1993
  - name: "Terminal Terror"
    year: 1994
---

<style>
  .pm-games {
    columns: 2;
    column-gap: 24px;
    margin-left: 20px;
  }
  .pm-games li {
    break-inside: avoid;
  }
  .pm-games .pm-year {
    color: #9ea3ac;
    font-size: 0.875em;
  }
  .ar-btn.pm-soon {
    background: transparent;
    color: #9ea3ac !important;
    border-color: #3a3e46;
    cursor: default;
  }
  @media screen and (max-width: 600px) {
    .pm-games {
      columns: 1;
    }
  }
</style>

<div class="ar-hero">
  <p class="ar-tagline">
    Play the games of Pie in the Sky's <strong>POWER engine</strong>
    family on modern Windows and Linux: those made with the
    <strong>3D Game Creation System</strong>, and those on
    <strong>POWER 3D</strong> and the engines derived from it. With
    widescreen, mouse look and a real 3D view.
  </p>
  <span class="ar-badge">{{ page.version }}</span>

  <div class="ar-downloads">
    {%- if page.download_win64 != "" %}
    <a class="ar-btn" href="{{ page.download_win64 }}">
      Download for Windows<small>64-bit &middot; {{ page.version }}</small>
    </a>
    {%- else %}
    <span class="ar-btn pm-soon">Windows<small>Coming later</small></span>
    {%- endif %}
    {%- if page.download_linux64 != "" %}
    <a class="ar-btn" href="{{ page.download_linux64 }}">
      Download for Linux<small>64-bit &middot; {{ page.version }}</small>
    </a>
    {%- else %}
    <span class="ar-btn pm-soon">Linux<small>Coming later</small></span>
    {%- endif %}
  </div>
  <p class="ar-note">
    PIEMulator is in beta: not every game has been played through to the
    end yet. Games are not included: you need the game's own files.
    {%- if page.discord != "" %}
    Questions and bug reports: <a href="{{ page.discord }}">Discord</a>.
    {%- endif %}
  </p>

  {% include kofi-banner.html %}

  <details class="ar-new">
    <summary>Update {{ page.version | remove: "Beta " }} available: what's new</summary>
    <ul>
      <li><strong>Linux:</strong> PIEMulator now runs on Linux too, as well as Windows.</li>
      <li><strong>Original pace:</strong> the games run at the speed of the PCs they were made for. Before, much of each game ran too fast: the machine gun, grenades (which could go off at your feet), animations, and enemies and your own moves.</li>
      <li><strong>Still smooth:</strong> the view keeps your display's refresh rate, so turning, walking and jumping stay smooth between the game's frames.</li>
      <li><strong>New Engine slider</strong> in the game list, to choose the game's frame rate, from 10 to 70 frames a second (see <a href="#the-game-list">The game list</a>).</li>
      <li><strong>Mouse look:</strong> walls and floor turn together, and objects keep facing you while you turn.</li>
      <li><strong>OpenGL view:</strong> the floor no longer shifts slightly against the walls as you walk.</li>
      <li><strong>Minimal HUD:</strong> the item boxes sit beside the weapon at the bottom left, and the row of objects to drop shows on top of them.</li>
      <li><strong>Fixed:</strong> after <kbd>Alt</kbd>+<kbd>Tab</kbd> or <kbd>Alt</kbd>+<kbd>F4</kbd>, <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> and <kbd>E</kbd> could stop working in the next game.</li>
      <li><strong>Game list:</strong> a tidier layout; the start options are now called <em>Maximized</em> and <em>Fullscreen</em>, with the sliders beside them.</li>
    </ul>
  </details>
</div>

PIEMulator runs the DOS games of Pie in the Sky Software's POWER engine
family on today's computers: Pie in the Sky's own, from Lethal Tender
(1993) on; the games made with its **3D Game Creation System** (GCS,
1993-95); and the games on **POWER 3D** and the engines derived from it. It
also runs GCS itself, with its level editor, paint program and build tools.
No DOS box is needed. You can play the games just
as they looked in 1995, or turn on an OpenGL view with widescreen, mouse
look and modern controls.

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
    <p>64-bit builds for both. No DOSBox, no virtual machine.</p>
  </div>
  <div class="ar-card">
    <h4>Fast and smooth</h4>
    <p>Each game runs as native code, made on your computer as it loads. Games keep their original pace, while the view stays smooth at your display's refresh rate.</p>
  </div>
  <div class="ar-card">
    <h4>A real 3D view</h4>
    <p>An OpenGL view draws the game's world as true 3D, at your screen's resolution. Switch to the original renderer at any time.</p>
  </div>
  <div class="ar-card">
    <h4>Widescreen</h4>
    <p>The view fills a wide window or monitor, with the HUD kept in proportion.</p>
  </div>
  <div class="ar-card">
    <h4>Mouse look and WASD</h4>
    <p>Turn and look up and down with the mouse, walk with W, A, S and D, fire with the mouse button.</p>
  </div>
  <div class="ar-card">
    <h4>Your own controls</h4>
    <p>Rebind any key or mouse button, for every game or for one, in play, in the inventory and in the menus.</p>
  </div>
  <div class="ar-card">
    <h4>Sound and music</h4>
    <p>Sound Blaster effects and AdLib music, as the games played them.</p>
  </div>
  <div class="ar-card">
    <h4>Over a hundred games</h4>
    <p>See the <a href="#games">list below</a>.</p>
  </div>
  <div class="ar-card">
    <h4>GCS itself</h4>
    <p>The level editor, GCS Paint and the build tools work too, so you can still make a game.</p>
  </div>
  <div class="ar-card">
    <h4>A game list in the spirit of DOS</h4>
    <p>Pick a game and play. Its window stays the same from the list to the game, ready for screen recording.</p>
  </div>
</div>

## No original code inside

PIEMulator is not built from the source code of GCS, its engine or any game.
Pie in the Sky's source code was never used. Everything PIEMulator knows
about those programs was learnt from the programs themselves, as they were
shipped.

The download does not contain the original programs either, nor any
recompiled code made from them. It holds only PIEMulator's own code: a
reimplementation of the PC the games were written for, and the tools that
recompile a game.

**Games are recompiled on your own computer, each time you play.** When a
game starts, PIEMulator reads the game's own programs from your folder and
turns them into native code in memory. When you close the game, that code is
gone. Nothing made from a game is ever sent anywhere or shipped with
PIEMulator.

## Games

PIEMulator's game list has over a hundred games. Pie in the Sky's own:

<ul class="pm-games">
{%- for game in page.games %}
  <li>{{ game.name }}{% if game.year %} <span class="pm-year">{{ game.year }}</span>{% endif %}</li>
{%- endfor %}
  <li><em>Many more...</em></li>
</ul>

The many more are the games other people made with GCS, POWER 3D and the
engines derived from them, from 1995 to the 2010s. Each runs from your own
copy of its files; PIEMulator includes none of them.

Several of these were released in more than one version (shareware,
registered, earlier or later releases); the list knows each of them. A game
with adult content is left out of the list unless you ask for it (see
[Settings file](#the-settings-file)).

## Getting started

1. **Download** the build for your system and extract it to a folder of its
   own, for example `C:\Games\PIEMulator` or `~/piemulator`.
2. **Add your games.** Make a folder named `games` next to `piemulator`,
   and put each game in a folder of its own inside it. Each game in the
   list has a usual folder name, shown on the right when you select it;
   a game in a folder with that name is found by itself. Or keep the game
   where it is and choose its folder with **...**.
3. **Start it.** Run `piemulator.exe` on Windows, or `piemulator` on Linux. It opens the
   game list.
4. **Pick a game and press Play.** The game starts in the same window, and
   the list comes back when it ends.

The game's folder needs the game as it was shipped, its programs included.
PIEMulator finds the game anywhere up to three folders deep inside it, so an
unpacked archive can be used as it is. To use GCS itself, put its folder,
named `GCS`, next to `piemulator`. For example:

```
C:\Games\PIEMulator\
    piemulator.exe
    games.ini
    GCS\                                                 GCS itself
    games\
        Lethal_Tender_(1993)_(Pie_in_the_Sky_Software)\
        Stop_Nick_Macki_(1993)_(Pie_in_the_Sky_Software)\
        ...
```

On Linux the `games` folder's name is lower case.

## The game list

| Key | Does |
|---|---|
| <kbd>Enter</kbd> | Play the selected game |
| <kbd>Tab</kbd> | Type the game's folder |
| <kbd>F2</kbd> | Controls: the key bindings |
| <kbd>F3</kbd> | Save the folders and settings |
| <kbd>F4</kbd> | Sort the list by name, year or author |
| <kbd>Esc</kbd> | Exit |
| A letter | Jump to the games starting with it |

On the right are the selected game's name, author and year, anything a
player should know about it, and the keys below. Under them:

<div class="ar-options" markdown="1">

| Option | What it does |
|---|---|
| Game data folder | Where the game's files are. Type it, or choose it with **...**. |
| Controls | The key bindings, for this game or for every game (see [Controls](#controls)). |
| Save | Saves the folders and the settings. **Play** saves them too. |
| Play | Starts the game. |
| Maximized | Every game's window opens maximized. |
| Fullscreen | Every game opens in fullscreen. |
| Engine | How many frames a second the game itself runs in 3D play, from 10 to 70. The default, 17.5, is the speed of the PCs the games were made for, and keeps weapons, grenades and animations at their original pace. The view stays smooth whatever you choose. |
| Mouse | Mouse sensitivity, from 0.25&times; to 2.5&times;. |
| Volume | The volume of sound and music. |

</div>

## While playing

| Key | Does |
|---|---|
| <kbd>=</kbd> / <kbd>-</kbd> | Less or more HUD: the full HUD; a minimal one with only the weapon, the readouts, health, the compass, the radar or map, and the item a door asks for, along the window's edges; or none at all |
| <kbd>Alt</kbd>+<kbd>Enter</kbd> | Fullscreen or a window |
| <kbd>Alt</kbd>+<kbd>F7</kbd> | Modern controls on or off |
| <kbd>Alt</kbd>+<kbd>F8</kbd> | Widescreen on or off |
| <kbd>Alt</kbd>+<kbd>F9</kbd> | The OpenGL view, or the engine's own renderer |
| <kbd>Alt</kbd>+<kbd>F10</kbd> | Show the frame rates over the view |
| <kbd>Alt</kbd>+<kbd>F11</kbd> | Capture the mouse, or let it go |
| <kbd>Alt</kbd>+<kbd>F12</kbd> | Smooth textures and picture |
| <kbd>Alt</kbd>+any key | Sends that key itself, not what it is bound to (to type a name, say) |

## Controls

While the 3D view is being played, PIEMulator adds modern controls. Each
key or button below sends one of the game's own keys, so the game handles
it as it always did.

<div class="ar-options" markdown="1">

| Press | Does | Game's own key |
|---|---|---|
| <kbd>W</kbd> / <kbd>S</kbd> | Walk forward / backward | Keypad up / down |
| <kbd>A</kbd> / <kbd>D</kbd> | Sidestep left / right | Keypad 1 / 3 |
| Mouse | Turn, and look up and down in the OpenGL view | |
| Left mouse button | Fire | <kbd>Ctrl</kbd> |
| Right mouse button, <kbd>E</kbd> | Pick up, read a memo | <kbd>I</kbd> |
| <kbd>Space</kbd> | Jump | Keypad 0 |
| <kbd>Q</kbd> | Choose an object to drop | <kbd>S</kbd> |

</div>

All the game's other keys still work: weapons <kbd>1</kbd> to <kbd>9</kbd>,
the map, <kbd>Esc</kbd> and the rest.

### The default bindings

There are three sets of bindings: one while playing, one while you choose an
object to drop, and one for the menus, the map and the pause and help
screens. A key that isn't listed sends itself.

<div class="ar-options" markdown="1">

| Press | Playing | Choosing an object to drop | Menus |
|---|---|---|---|
| <kbd>W</kbd> | Walk forward | <kbd>W</kbd> | Up |
| <kbd>S</kbd> | Walk backward | <kbd>S</kbd> | Down |
| <kbd>A</kbd> | Sidestep left | The previous object | Left |
| <kbd>D</kbd> | Sidestep right | The next object | Right |
| <kbd>E</kbd> | Pick up, read a memo | Drop it | Choose (<kbd>Enter</kbd>) |
| <kbd>Q</kbd> | Choose an object to drop | Cancel (<kbd>Esc</kbd>) | <kbd>Q</kbd> |
| <kbd>Space</kbd> | Jump | <kbd>Space</kbd> | <kbd>Space</kbd> |
| Left mouse button | Fire | | The game's mouse |
| Right mouse button | Pick up | | The game's mouse |

</div>

Some games come with bindings of their own, to match their controls. In
**Stop Nick Macki**, whose 1993 engine kicks and fires with
<kbd>Space</kbd>, the left mouse button and <kbd>Ctrl</kbd> send
<kbd>Space</kbd>. The Controls screen shows these as the game's defaults.

**Controls** (<kbd>F2</kbd> in the game list) changes the bindings, for the
selected game or for every game. There are three sets: *Playing*,
*Inventory* (while you choose an object to drop) and *Menus*. Click an input
and press the game's key it should send, or choose *Pick up*, *None*, or
*Clear* to go back to the default. *Add input* takes any key, mouse button
or the mouse wheel.

## The settings file

The game list keeps its settings in `piemulator.cfg`, next to `piemulator` (or in your
user settings folder, if that one can't be written). It can also be edited
by hand:

```
start_maximized=1        # every game's window opens maximized
start_fullscreen=1       # every game opens in fullscreen
engine_fps=17.5          # the game's frame rate: 10, 11.7, 14, 17.5, 23.3, 35 or 70
mouse_sensitivity=1.5    # 0.25 to 2.5
volume=80                # 0 to 100
show_adult=1             # list games with adult content
bind.all.e=i             # E picks up in every game
bind.all.wheelup=2       # the mouse wheel picks weapons 2 and 3
bind.all.wheeldown=3
bind.all.menu.q=esc      # in the menus, Q backs out
```

What PIEMulator knows of each game (its name, folder, default bindings, and
for a few games a frame rate of their own, used instead of the Engine slider)
is in `games.ini`, next to `piemulator`. A `games.ini` in your user settings folder is
read after it, to add games or change them, without touching the installed
one.

<div class="ar-faq ar-options" markdown="1">

<details markdown="1">
<summary>Advanced: starting options and the command line</summary>


| Variable or switch | What it does |
|---|---|
| `piemulator --play FOLDER` | Starts the game in that folder, as the game list would. |
| `piemulator --root FOLDER P3D.EXE` | Runs one program from a folder, here GCS's level editor. |
| `GCS_WINDOW=1280x720` | The window's size at start. |
| `GCS_RENDER=soft` | Starts with the engine's own renderer. |
| `GCS_WIDE=0` | Starts with widescreen off. |
| `GCS_SMOOTH=1` | Starts with smooth textures on. |
| `GCS_HUD=minimal` / `none` | Starts with the minimal HUD, or none. |
| `GCS_MODERN=0` | Starts with the modern controls off. |
| `GCS_MOUSE_INVERT=1` | Inverts looking up and down. |
| `GCS_VSYNC=0` | Doesn't wait for the display's refresh. |
| `GCS_ENGINE_FPS=17.5` | The game's frame rate in 3D play, over the Engine slider and `games.ini`. |
| `GCS_GAMETIME=0` | Leaves the game's speed as the original engine works it out, which runs a little fast on modern PCs. |

</details>

</div>

## Troubleshooting

<div class="ar-faq" markdown="1">

<details markdown="1">
<summary>The game list can't find a game</summary>

Select the game and choose its folder with **...**. The folder must hold
the game as it was shipped, programs included; an installer or a
compressed archive must be installed or unpacked first.
</details>

<details markdown="1">
<summary>A game runs slowly</summary>

If the console says the game "is not a known game executable", its program
was changed or comes from a release PIEMulator doesn't know. It still runs,
but slower. Please tell us on Discord which game and release it is, so it
can be added.
</details>

<details markdown="1">
<summary>Windows warns that the program is from an unknown publisher</summary>

The beta builds are not signed yet; the warning does not mean anything
harmful was found. Choose **More info**, then **Run anyway**. Or, before
unpacking, right-click the downloaded `.zip`, choose **Properties**, tick
**Unblock** and press **OK**.
</details>

<details markdown="1">
<summary>Enemies and animations move less smoothly than the view</summary>

That is the original pace: the game itself runs at 17.5 frames a second,
as on the PCs it was made for, while PIEMulator keeps the view smooth
between its frames. To make them smoother, raise **Engine** in the game
list; above the default, the machine gun, grenades and animations run
faster than they should.
</details>

<details markdown="1">
<summary>The mouse doesn't turn the view</summary>

The modern controls only take over while the 3D view is being played. If
the mouse is still free, press <kbd>Alt</kbd>+<kbd>F11</kbd> to capture it,
and check that the modern controls are on (<kbd>Alt</kbd>+<kbd>F7</kbd>).
</details>

<details markdown="1">
<summary>The controls don't match the game's instructions</summary>

The modern controls change them on purpose. <kbd>Alt</kbd>+<kbd>F7</kbd>
turns them off, for the game's original keys. To change a single key, use
**Controls** in the game list.
</details>

<details markdown="1">
<summary>I can't type a name, or a letter does something else</summary>

Hold <kbd>Alt</kbd> while typing: <kbd>Alt</kbd> with a key sends that key
itself, whatever it is bound to.
</details>

<details markdown="1">
<summary>Something looks wrong in the OpenGL view</summary>

Press <kbd>Alt</kbd>+<kbd>F9</kbd> to switch to the engine's own renderer,
and let us know which game and where.
</details>

<details markdown="1">
<summary>On Linux, the folder picker doesn't open</summary>

It needs `zenity` or an xdg-desktop-portal. You can also type the folder:
select the game and press <kbd>Tab</kbd>.
</details>

</div>

## Limitations

- No network, modem or serial play.
- No joystick: it reads as absent, as on a PC without one.
- PIEMulator is a beta. Not every game has been played through to the end.

## Games are not included

PIEMulator does not include, sell or distribute any game, nor GCS itself,
nor any part of them. To play, you need your own copy of the game's files.
Please don't ask for copies of games in the project's channels.

The games, GCS and the POWER 3D engine belong to their owners. PIEMulator,
its developers and contributors are not responsible for unauthorised or
illegal redistribution of copyrighted game files.

## About

<div class="ar-about" markdown="1">

3D Game Creation System, POWER 3D and Lethal Tender are (C) Pie in the Sky
Software. The games made with them belong to their authors.

PIEMulator is developed and maintained by Ricardo Reis. It is not affiliated
with or endorsed by Pie in the Sky Software.

PIEMulator is free. It may not be sold, or included with anything that is
sold, without permission.

Third-party software:

- SDL 3 - zlib License
- Capstone - BSD 3-Clause License
- TinyCC - GNU LGPL 2.1, as `libtcc.dll` (`libtcc.so` on Linux), which you may replace with your own build ([source](https://repo.or.cz/tinycc.git), commit `43c7708b85681a2fd4451c8a541af4494a8919b2`, unmodified)

The licences, and how TinyCC was built, come with the download, in its `licenses` folder.

Website: [https://rickomax.github.io/piemulator](https://rickomax.github.io/piemulator)<br>
{%- if page.discord != "" %}
Discord: [{{ page.discord }}]({{ page.discord }})<br>
{%- endif %}
Support the project: [https://ko-fi.com/{{ site.kofi_username }}](https://ko-fi.com/{{ site.kofi_username }})

</div>
