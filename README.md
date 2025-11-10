# TerrainService
Something I worked on for quite a bit. Decided to open source it because why not.

## How to use
Intent is to just edit `TerrainService/TerrainConfig` and add to the features in `TerrainService/Features`
- You should be able to edit TerrainConfig at runtime.
- While Features are technically static, you could rig it so that it itself is also dynamic. Look at the codebase for inspiration
  - Currently just one feature called `FlowerGenerator`. Take a look at it and add other generators too!

Simply drag the rbxmx file to your place of choice and move TerrainService into ServerScriptService.

## Tips
Highly recommend publishing the place before testing it out. Unless your computer has a lot of cores it will not work.

It's designed to be standalone, though a primitive API interface is available if you want

### Performance
If you want maximal speed, do the following
1. Disable Features (Placing down assets is surprisingly very slow)
2. Disable Water
3. Make the terrain kinda short
4. Decrease chunk size and/or render distance
5. Run it on a roblox server (not your laptop)

## Some Fun Facts
- It uses roblox actors (it was a nightmare)
- Extensively uses `--!native` (further optimizations soon through better type hinting)
- Significant portion was vibe-coded (Any AI companies here?)
