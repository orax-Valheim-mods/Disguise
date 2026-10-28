# Changelog

## [0.1.0] - 2026-10-28

### Added

- Add a frame time meter (disguise perf)
- Add a Logs option to switch the mod's own Info messages off
- Add .gitignore
- Add .prettierrc.json for formatting code

### Changed

- Init
- Deploy to both installs and clean up all warnings
- Move the Harmony patches into Patch.cs
- Expose an internal API for the Harmony patches
- One class per file for the Harmony patches
- Split Disguise.cs into config, game access, prefab and applier classes
- Split observer refresh, console command and create/destroy flag into their own classes
- Hide the equipment of a disguised player from the other machines
- Rename HideShoulder to HideCape and change the defaults
- See your disguise on your own screen (rebuilt, cost-neutral)
- ShowAsAlly - display the creature as an ally or as an enemy
- SetFakePosition - show a fake position on the other players' map
- The bridge picks the creature's own normal / special attack
- The block key plays the creature's own third attack
- Install only into BepInEx plugins in the package README
- The creature can fly while your player stays on the ground
- Record the flight shortcuts by pressing them instead of typing them
- The mouse wheel climbs and descends while the flight is on
- Format with CSharpier 1.3.0
- Disguise window - step 1: frame, key chord and the input rule
- Disguise window - step 2: creature list, filter and focused typing rule
- Disguise window - step 3: the 3D preview of the creature under the pointer
- Disguise window - step 4: the command buttons and the status line
- Disguise window - step 5: Escape closes it, without pausing the game
- Disguise window - the title row shows the GuiKey chord
- Any registered prefab - six category checkboxes over the window list
- The prefab lists only show vanilla prefabs
- The prefab lists drop the effect prefabs (fx_, sfx_, vfx_)
- Disguise list writes its output to the log too
- A Static category for the prefabs that can never follow
- The prefab list drops the Ships category
- The filter row of the window gets a Clear button
- The state line carries the flight and the altitude
- The console moves and turns the costume
- The window edits the pose of the costume
- The status line moves under the title and carries the size of the costume
- The window marks prefabs as favorites and lists them alone
- The Favorite button marks the selected prefab, not the hovered one
- The checkbox row shows Favorites first, then the categories alphabetically
- A gold star marks the favorite rows of the list
- The place of the window is kept in the config, centred by default
- The catalogue drops every prefab nothing can be drawn of
- The checkbox of the row becomes a builder the window can call
- A box takes the shimmer off an item costume
- The window says what the element under the pointer is for
- A Disguise line in the pause menu
- The settings of a working install become the defaults
- A switch for the Disguise line of the pause menu
- The log stays quiet by default
- DEV.md, how a pause menu line is added and taken out
- The config file is bound section by section
- The window's repeated text writes and its two measures get one home
- Every static readonly field carries the s_ prefix
- The costume carries the game's own level
- The console and the window set the level
- The copies we build are dressed for their level
- The level has no ceiling, the game itself has none either
- The level is kept inside 1 to 9, like the spawn command
- The window's rows in the order asked for - favorite first, level left of the sparkle
- A humanoid costume is born with its armor and its weapon
- The costume's gear travels to the machines running no DLL
- The costume's hands are chosen, weapon by weapon, in the Whose list
- The weapons row, its list and the three filters of the pool
- DEV.md gives way to PLAN.md
- The weapons list takes the picture's width, without its Whose word, and reads Creature default
- Option to leave your line out of the player list others receive
- The flight comes into the window - its four chords on their own line, the wheel switch and the speed and step fields in the band, and the help band back to three lines
- An All box beside Favorites in the checkbox row
- The command buttons stand taller and wider - the picture grows with them
- Generate changelog and upload release to GitHub in post-build script
- Call the reusable workflows from orax-modding/publish
- Enforce LF line endings via .gitattributes and .editorconfig
- Use 7-Zip instead of .NET compression for release archives
- Create README.md
- Update mod icon
- Update LICENSE

### Fixed

- Ship a correct ThunderStore README instead of the stale 'unlimited stamina' one
- Discard the clone when a game component survives the strip
- Translate footstep effects to the disguise creature
- The owner decides what equipment stays hidden
- The creature now plays your melee attack (own view + vanilla observers)
- The melee bridge now reads trigger lists from active objects
- Raise the flight in the packet header, where a position really travels
- Default the scroll step to 0.2 metres per notch
- Disguise window - filter inside the frame, beige rows with an orange selection, wheel option
- Disguise window - clamped list ends and a 3000 pixel wheel step
- Disguise window - the list takes the wheel back from the preview listener
- The own-view clone keeps its mesh filters
- Hold the relayed position of a disguised player still
- A costume is relayed with its own health, not the player's
- Relay a costume where it rests, so it stops shivering
- The relayed band holds a disguised player's position only
- Lay a costume on the ground it rests on, not on level ground
- Read the ground three ways before giving up on a costume
- Read the ground a fourth way, from the zone the server never built
- The window only builds the rows of the categories it shows
- The state line reports the flight offset instead of the altitude
- The pose rows were built over the last rows of the list
- The ground rest erased the turn around X and Z
- Small prefabs trembled in the preview, framed a hand's width from the stage
- The preview keeps the row the pointer was on instead of reverting
- Marking a favorite no longer throws the list back to its first row
- Reopening the window finds the list where it was
- The preview frames every prefab to fill its picture
- The preview frames only the meshes it draws, and says what it measured
- The preview measures a skinned mesh from its pose
- The size on the status line is the size of what is drawn
- The size on the status line is back for every prefab
- The ground rest only counts colliders the machines really simulate
- The reload draws the Disguise line only once
- The terrain the probe built goes with the plugin that built it
- The save's Player prefab comes back even when the save threw
- A hit points measurement is only cached when one was taken
- The costume's footstep is looked up again while the prefab is not there
- The costume's gear was rolled but every item was skipped
- The Whose list gives the Fuling its weapons back
- A new Whose pick redraws your own costume and the picture at once
- A wielded utility piece answers Show weapons - the shamans' staffs are no armor
- The window's picture draws the gear - the stage layer is re-applied after VisEquipment spawns it
- The help line gets seven lines of its own - the panel grows for the long helps
- Drop the leftover JotunnModStub identity and align on Jotunn 2.30.2
- Declare the Jotunn dependency so BepInEx loads it first
- Write forward slashes in release ZIP entry paths

### Removed

- Remove Unity project

[0.1.0]: https://github.com/orax-Valheim-mods/Disguise/tree/0.1.0

<!-- generated by git-cliff -->
