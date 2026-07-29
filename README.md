# XRKart 64

XRKart 64 brings Mario Kart 64 racing to standalone VR on Meta Quest.

It is a fan-made VR project built on the work of the SpaghettiKart and
LibUltraShip communities. XRKart 64 is not affiliated with or endorsed by
Nintendo.

## What you need

- A Meta Quest headset
- The XRKart 64 APK from the Releases section of this page
- Your own legally dumped copy of the US release of Mario Kart 64

XRKart 64 does **not** include a ROM or Nintendo-owned game assets. ROM
verification and game-data generation happen locally on your headset.

### Supported ROM

The launcher accepts these N64 ROM byte orders:

- `.z64`
- `.n64`
- `.v64`

The supported ROM is the 12 MiB US release with this normalized SHA-1:

`579C48E211AE952530FFC8738709F078D5DD215E`

## Installing the APK

Sideload the XRKart 64 APK with SideQuest or Android Debug Bridge (ADB).

Example ADB command:

```text
adb install -r XRKart-64.apk
```

After installation, open **XRKart 64** from your headset's Unknown Sources or
unverified-apps section.

XRKart 64 has been tested on Quest 2 and Quest 3. Other Quest-family headsets
listed by the application may work, but should be considered unverified until
they have been tested with the current release.

## First launch and game-data generation

The first time you open XRKart 64:

1. Select **Select legally dumped ROM**.
2. Choose your own Mario Kart 64 US ROM.
3. Wait for local verification to finish.
4. Select **Generate local game data**.

Generation can take several minutes. Testing on Quest 2 took approximately
eight minutes.

Keep XRKart 64 open and keep the headset awake until it finishes. The progress
indicator is intentionally indeterminate: the generated files appear only
after the complete generation pass succeeds.

When generation finishes, the game starts automatically. On future launches,
select **Start game**; you do not need to generate the data again.

The launcher also provides two cleanup options:

- **Forget selected ROM** removes XRKart 64's permission to reopen the selected
  ROM. It does not delete already generated game data.
- **Delete generated game data** removes the private generated archives. You
  will need to generate them again before playing.

Uninstalling XRKart 64 or clearing its application data removes generated game
data and saved settings.

## Comfort and Stereo presentation

XRKart 64 uses two presentation styles:

- **Comfort** displays the original game on a world-locked virtual screen.
- **Stereo** renders an unpaused, single-player race with native per-eye VR
  cameras and head tracking.

Comfort is the default presentation.

Native Stereo currently operates only while you are actively racing in
single-player mode. Front-end menus, character and course selection, results,
cutscenes, multiplayer modes, and the pause menu use the Comfort screen.

When you pause during Stereo, the game temporarily returns to the Comfort
screen so the original pause menu remains readable. This does not mean Stereo
has been disabled.

### Quickly entering Stereo

1. Begin a single-player race.
2. Wait until the race is actively running.
3. Hold the **left controller Menu button** for about 0.6 seconds.

Holding that button while in Comfort switches to Stereo. Holding it again
while already in Stereo switches between First Person and Third Person.

Stereo automatically recenters when it starts.

## Default racing controls

These mappings apply while the race is actively running:

| Quest control | Default racing action |
| --- | --- |
| Left stick | Steer / N64 analog stick |
| Left-stick click | Recenter VR view |
| Right trigger | Accelerate / N64 A |
| Left trigger | Brake and reverse / N64 B |
| Right grip | Hop and drift / N64 R |
| Left grip | N64 L |
| A button | Use item / N64 Z |
| B button | N64 C-Left |
| X button | N64 C-Up |
| Y button | N64 C-Right |
| Right stick | N64 C-buttons |
| Right-stick click | N64 C-Down |
| Tap left Menu button | Pause |
| Hold left Menu button for about 0.6 seconds | Enter Stereo or switch First/Third Person |

The face buttons intentionally emulate N64 controls while driving. For
example, the Quest A button uses your item during a race; it is not the menu
Select action until the game is paused.

### Recenter

The default in-race recenter control is **left-stick click**. Recenter is
available while the race is actively running and also repositions the
world-locked Comfort and menu screens.

You can change the recenter button under:

**VR Settings → Controls → Recenter View**

The selected recenter button becomes a dedicated action during a race. It will
not also perform its previous racing action.

## Menu controls

Menu navigation stays fixed even if you remap the racing controls:

| Quest control | Menu action |
| --- | --- |
| Left stick up/down | Move through entries |
| Left stick left/right | Change the selected setting |
| A button or right trigger | Select, toggle, or increase |
| B button or left trigger | Back |
| Left/right grip | N64 L/R menu tabs |
| Left Menu button | Start or pause |

## Opening VR Settings

VR Settings are accessed through the original pause menu:

1. Tap the **left controller Menu button** during a race.
2. Scroll down to the final pause-menu entry, **VR SETTINGS**.
3. Press A or the right trigger.

Settings save automatically when you change them.

Use B or the left trigger to move backward through the VR Settings levels.
Press Back repeatedly to return to the original pause menu, then choose
Continue to resume the race.

> **Important: some VR Settings sections contain more than one page.**
>
> Continue pressing the left stick down after reaching the bottom visible row.
> Watch the page counter in the lower-right corner of the menu.

The sections with hidden second pages are:

- **Controls:** page 2 contains X, Y, right-stick click, and right-stick
  direction mappings.
- **VR Camera:** page 2 contains chase-camera height, distance, and tilt.

The main VR Settings sections are:

- **Controls**
- **Stereo Settings**
  - Stereo Mode
  - VR Camera
  - VR HUD
  - VR Performance
- **Comfort Settings**
  - Comfort Camera
  - Comfort Menu
- **Advanced**

## Important VR settings

### Stereo Mode

- **VR Presentation:** Comfort or Stereo
- **Player Mode:** Seated or Standing
- **Recenter View:** manually centers tracking and world-locked screens

Seated is the default and recommended starting mode.

### VR Camera

- **Camera View:** First Person or Third Person
- **World Scale:** changes perceived world scale and physical movement
- **Head Translation:** changes positional head movement without disabling
  rotational tracking
- **Lock Head Roll:** keeps the horizon level while preserving head yaw and
  pitch
- **Driver Eye Height/Forward:** adjusts the First Person viewpoint
- **Hide Kart:** hides your local kart model in First Person
- **Chase Camera Height/Distance/Tilt:** adjusts Third Person view; these
  settings are on the second page

Third Person is the default camera. The local kart is hidden by default in
First Person.

World Scale accepts positive values only. Setting Head Translation to `0`
disables positional head movement while keeping head rotation and correct
stereo eye separation.

### VR HUD

The race HUD uses its own Stereo plane. You can:

- Show or hide it
- Change its distance
- Expand or contract its spread around the center of your view

### Comfort Settings

The main game screen and the pause/settings screen have separate position and
size controls. Adjusting the Comfort Camera does not automatically move the
Comfort Menu, and vice versa.

### Performance and Advanced

- **Render Scale requires restarting XRKart 64.**
- Increasing Render Scale improves clarity but costs performance.
- **High Detail Models** may reduce performance.
- **Disable Culling** is substantially slower and should be treated as an
  experimental or troubleshooting option.
- Headset frame pacing and the native game update rate are locked to their
  required VR behavior.

## Comfort and safety

VR racing can cause motion discomfort.

- Start with Comfort presentation or Seated mode.
- Try **Lock Head Roll** if natural camera roll feels uncomfortable.
- Use Third Person before trying First Person.
- Stop playing and remove the headset if you feel dizzy, nauseated, or
  disoriented.
- Make sure you are in a safe play area before using Standing mode.

## Troubleshooting

### Stereo does not activate

Make sure:

- You are in a single-player race.
- The race has started and you are actively driving.
- VR Presentation is set to Stereo, or you held the left Menu button for about
  0.6 seconds.
- The game is not paused.

Menus, results, cutscenes, multiplayer, and paused gameplay intentionally use
the Comfort screen.

### The camera is off-center

Click the left stick while actively racing, or use:

**VR Settings → Stereo Settings → Stereo Mode → Recenter View**

### A or B behaves differently during a race

This is intentional. While actively driving, the face buttons use their
remappable N64 racing assignments. When paused or in a menu, A is Select and B
is Back.

### A setting appears to be missing

Scroll past the bottom visible row. Controls and VR Camera both have second
pages, shown by the page counter in the lower-right corner.

### Render Scale did not change

Close and restart XRKart 64 after changing Render Scale.

### Generated game data is missing

Return to the XRKart 64 launcher, select your legally dumped supported ROM, and
run **Generate local game data** again.

## Privacy and game-data boundary

ROM verification and extraction happen locally on your Quest. XRKart 64 does
not upload your ROM, bundle it in the APK, or write a ROM copy into generated
game data.

Generated archives are stored in private, non-backed-up application storage.
Do not distribute your ROM or generated game data.

## Credits

- XRKart 64: J4nky
- Upstream project: Harbour Masters — SpaghettiKart
- SpaghettiKart maintainers: MegaMech, Coco875, KiritoDv
- LibUltraShip: Kenix3 and contributors
- Quest VR foundation: Poregon
- VR methods reference: Alex-LeTux

Thank you to everyone who contributed to the decompilation, recompilation,
tooling, documentation, testing, and VR research that made this project
possible.
