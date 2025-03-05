# Lynx's GT New Horizons run repository

This repo contains various bits and bobs relating to my GT New Horizons run

**World version:** 2.7.3<br/>
**Tier:** IV<br/>
**Run playlist:** https://www.youtube.com/playlist?list=PL9frwGSBfRI82DXNy5mXZebMx1kzaXcUs

## Current goal

My current goal is a T8 rocket and we'll see how I feel after that, I may
go to Stargate but I'm along way away from having to even make that decision.

My play style is definitely suboptimal and I do play other games and other MC
packs so I expect this to take a while.

I may offer world downloads via this page when I hit certain milestones or
simply based on time but we'll see.

Although I'm not committing to gate just yet here are the GTNH run rules as of the time
this doc was written.

https://docs.google.com/document/d/1Iww1FNLkCuun6s6LW7Q6_1Z1aldtxYeRxYOeq_P-vK8/edit?tab=t.0

## Inspiration

I have watched both Kharax82's S2 series and Threefold's S2 series and they
have inspired me to not only see how far I can go but also to track and
share my run with the world.

GTNH is admittedly a long slog that needs a lot of time however I have found
if you play at your own pace, switch up projects now and then and take breaks
it proves to be a great experience and is probably the most well tuned mod
pack I've ever played.

As long you're prepared to be in it for the long haul GTNH will reward you
with countless hours of well designed content and astound with its technical
marvels considering it's MC 1.7 heritage.

Here are links to Kharax82's and Threefold's channels and I highly encourage
you to check them out.

[Kharax82](https://www.youtube.com/c/Kharax82)<br/>
[@Threefold](https://www.youtube.com/@Threefold.)

## Important bits

### Setup

My world is running 24x7 on a dedicated machine with the following specs:

- AMD Ryzen 7800X3D
- 32GB DDR5 memory (10GB allocated to GTNH, rest is for other packs)
- 2TB nVME drive
- World backed up hourly to my NAS
- Fedora Linux 40

Server restarts daily at 06:00 AEST mostly to keep performance feeling snappy but also
for OS patching.

I run the Java 17+ version of GTNH with GraalVM and the following launch args:

```text
-Xms10G -Xmx10G -Dgraal.LoopRotation=true -Dgraal.PartialUnroll=true -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 @java9args.txt -jar lwjgl3ify-forgePatches.jar nogui
```

I am running the Client under Prism Launcher with GraalVM and the following args:

```text
-Dgraal.LoopRotation=true -Dgraal.PartialUnroll=true -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1
```
I allocate 10GB RAM to the client as I'm running a large resource pack and
shaders

My PC specs are:

- AMD Ryzen 7800X3D
- 64GB RAM DDR5 memory
- Nvidia RTX 4090
- 512GB + 4TB nVME drives
- Windows 11

### Shaders and resource packs

I play with `Complimentary Unbound` shaders but this may change depending on
feedback around video quality.

I also play with Sphax PureBDCraft with mostly pre-made patches from the forums but I
have made a couple of changes.

### Mod changes

- Hardcore Darkness is disabled (Just not a big fan)
- Add Dynamic Surroundings (I like the ambience)

### Config changes

I have made a few config changes some mostly for QOL and a couple for personal
taste:

#### InfernalMobs
- Disabled the Vengeance effect cause I just don't like it

#### Gregtech
- Disabled pollution, can see why some people might like it for additional
challenge but just not for me
- `machineRainExplosions=false` and `machineThunderExplosions=false` because I like to
leave weather enabled in my void world as it makes for nice ambience with shaders and
the DSurround mod

#### Thaumcraft
- Changed research difficulty to `-1` so I can buy research directly with aspects,
 the mini game doesn't really appeal to me and I like the time saving of being able
 to buy research

#### Sever Utilities
- Max homes = 100
- Max claimed chunks = 1000
- Max chunkloaded chunks = 1000

#### IngameInfoXML

- Set `topleft=5 5`
- Set `"scale(new)"=8`
- Makes the display readable on my 4k monitor
