# MoreAccessories v2 for KK, KKS and EC
This is an updated fork of the original MoreAccessories by Joan6694 (originally included as part of the [HSPlugins repository](https://github.com/IllusionMods/HSPlugins)).
The plugin has been overhauled by jalil49 to make it less hacky and more compatible with other plugins and mods.

Note that this is fork is only for the Koikatsu branch (KK, KKS and EC) since the AI and HS2 branch of MoreAccessories is already using the new approach introduced by the overhaul.

You can get the latest nightly builds of all plugins from the [CI workflow](https://github.com/IllusionMods/MoreAccessories/actions/workflows/ci.yaml). Open the latest successful run and download the build from the Artifacts section.

## How to use
1. Install latest BepInEx5 and BepisPlugins.
2. Download the latest release zip for your game from the releases page.
3. Extract the release zip into your game directory (the .dll files should end up inside the BepInEx\plugins folder).

## What exactly changed in the overhaul?
- Previously MoreAccessory data was stored separately from the main 20 accessories. The overhaul expands the fixed 20 arrays in multiple places and as such requires more fine tuning.
- In maker the slots showed will be based on the largest coordinate while in maker to avoid having to do weird stuff just to copy and transfer accessories.
- Scroll bars have been added for accessory slots in maker and H accessory list
- MoreAccessories now directly adds the scrolling to the accessory window (previously implemented in KKAPI)
- Excess slots are trimmed when saving, unfortunately I can't compress them since it would be breaking plugins.

You can find the old unmodified v1 version of MoreAccessories source code [here](https://github.com/IllusionMods/HSPlugins).

## How to contribute?
If you'd like to contribute code fixes and improvements: fork this repository, create a new branch, push your changes, and open a new PR.

To build this repository you will need VisualStudio2022+ with the `.NET desktop development` and `Game development for Unity` workloads, and `.NET Framework 3.5 development tools` + targetting packs and SDKs for at least `.NET Framework 4.6` (best to just install them all).
All dependencies are downloaded via nuget on first build of the solution. Check the wiki if you are having issues with build steps failing.

You can discuss modding on the Koikatsu Discord server in the modding channels. There are also various modding guides linked in the pins of these channels you may want to check out.
