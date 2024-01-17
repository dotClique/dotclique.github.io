# How to install Minecraft modpacks without CurseForge

A lot of Minecraft modpacks use CurseForge to manage and simplify installing modpacks.
However, this usually means you need to install their launcher, which sometimes adds unnecessary overhead, or is unsupported on your platform (e.g. Arch Linux).

Follow these simple steps to install a CurseForge modpack using the vanilla launcher.

1. Download the vanilla launcher if you don't have it already.
    * [Minecraft.net/download](https://minecraft.net/download).
    * Depending on your platform, consider scrolling down for the Legacy Launcher or Distro-specific installations.
2. Navigate to the modpack on the CurseForge website (I will use [SkyFactory 4](https://www.curseforge.com/minecraft/modpacks/skyfactory-4) as an example, specifically version `4.2.4`).
3. Identify the correct version of Minecraft from the modpack-information (e.g. `1.12.2`).
4. Install the corresponding version of Vanilla.
    * `Minecraft: Java Edition > Installations > New installation > Version`.
5. Download and install [Minecraft Forge](https://files.minecraftforge.net/) for the correct Vanilla version (e.g. `1.12.2 - 14.23.5.2859`).
    * Download the installer and run it.
6. Download the modpack client-files
    * On the CurseForge website open the _Files_-tab and select the version you want.
    * Press _Download_ to receive the client-files (e.g. `SkyFactory 4 - 4.2.4.zip`.
7. Download the modpack server-files.
    * From the client-files site (step 6.) open the tab _Additional Files_ and press on the server-files.
    * Press _Download_ to receive the server-files (e.g. `SkyFactory 4 - 4.2.4 Server Files`).
8. Create a new installation in Minecraft Launcher for the modpack
    * `Minecraft: Java Edition > Installation > New installation`
    * Set _Name_ to the name of the modpack (e.g. `SkyFactory 4 - 4.2.4`).
    * For _Version_ you must select the installed Forge-version of Minecraft (e.g. `release 1.12.2-forge-14.23.6.2859`).
    * For _Game Directory_ it is recommended to create a new directory to separate Vanilla and modpack-files.
        * Press _Browse_ and create a new directory beside the default minecraft-folder.
        * e.g. `C:\Users\USERNAME\Appdata\Roaming\.minecraft_sf4` on Windows.
    * Usually you can leave _Resolution_ to default (auto).
    * For a smoother experience, you should usually increase the memory Minecraft can use.
        * Press on _More Options_ to show the Java options.
        * In _JVM Arguments_ increase maximum memory (`-Xmx`).
        * How much memory you should use depends on the modpack and your system.
        * Default is `-Xmx2G`, which provides Minecraft with 2 GB of RAM.
        * Change it to e.g. `-Xmx8G` to use 8 GB.
        * Leave the rest of the _JVM Arguments_ as is.
    * Press _Save_.
9. Navigate to the minecraft-installation directory.
    * From the _Installation_-tab in the Minecraft Launcher (`Minecraft: Java Edition > Installations`).
    * Hover over the installation created in step 8 and press on the folder-icon next to _Play_.
    * e.g. `C:\Users\USERNAME\Appdata\Roaming\.minecraft_sf4` on Windows.
10. Copy the _mods_ folder from the server files
    * Unzip the server-files downloaded earlier
    * Copy the contents of the _mods_ folder to the _mods_ folder in the installation directory.
        * e.g. into `C:\Users\USERNAME\Appdata\Roaming\.minecraft_sf4\mods` on Windows.
    * __NB:__ Only the _mods_ folder from the server files.
11. Copy the contents of the _overrides_ folder from the client files.
    * Unzip the client files downloaded earlier.
    * Copy the contents of the _overrides_ folder into the installation directory.
        * e.g. into `C:\Users\USERNAME\Appdata\Roaming\.minecraft_sf4` on Windows.
    * __NB:__ Not into a subdirectory called _overrides_, but directly into the installation directory.
    * Overwrite any conflicting files.
12. Launch the profile from the Minecraft Launcher.


# Resources

This article is based on [this answer](https://www.reddit.com/r/CurseForge/comments/w31zbp/comment/ih2gfk2/) by _Master_Timkles_ on reddit.
