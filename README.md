# TerrainService
Something I worked on for quite a bit. Decided to open source it because why not.

## How to use
Intent is to just edit `TerrainService/TerrainConfig` and add features in `TerrainService/Features`
- You should be able to edit `TerrainConfig` at runtime.
- While Features are technically static, you could rig it so that it itself is also dynamic. Look at the codebase for inspiration
  - Currently just one feature called `FlowerGenerator`. Take a look at it and add other generators too!
- `FlowerGenerator` Requires a folder named `Flowers` in `ServerStorage/Assets`. Within it, add a folder named `Default`, and put flowers inside `ServerStorage/Assets/Flowers/Default`.
  - Note that you need not use this storage scheme, and can edit the storage scheme to however you desire.

Simply drag the rbxmx file to your place of choice and move `TerrainService` into `ServerScriptService`.

## Tips
**Highly recommend publishing the place before testing it out.** Unless your computer has a lot of cores it will run slow.

It's designed to be standalone, though a primitive API interface is available if you want.

### Performance
If you want maximal speed, do the following
1. Disable Features (Cloning assets is surprisingly very slow)
2. Disable Water
3. Make the terrain kinda short
4. Decrease chunk size and/or render distance
5. Run it on a roblox server (not your laptop)

## Some Fun Facts
- It uses roblox actors (it was a nightmare)
- Extensively uses `--!native` (further optimizations soon through better type hinting)
- Significant portion was vibe-coded (Any AI companies here?)
- It turns out I'm not very good at designing Terrain yet, but it's very easy for you to tune it to your liking.
  - Maybe next update will have better pre-configured `TerrainConfig`

## Issues and Feedback
If you have any issues or feedback you would like to give, feel free to do so!
- Please note that I may not be able to get through each and every piece of feedback myself.
