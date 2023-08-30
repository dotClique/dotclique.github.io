# eGPU on Arch Linux

Personally I am running any games I want in my dual-booted Windows-partition.
However, it is really nice to use my Razer Core X for power and to connect my 2 external monitors when I am at home.

This short article details my process for running an AMD Radeon Vega 64 GPU in a Razer Core X with Arch Linux on a Framework Laptop 13" 12th-gen Intel.


## 1. Install the eGPU

First and foremost, install the eGPU.
I recommend also doing this with a Windows computer or partition first if you want more official support in throubleshooting potential issues.


## 2. Ensure your laptop has Thunderbolt 3 / USB 4

I have only attempted this with a Framework Laptop 13" 12th-gen Intel, which has official Thunderbolt 3 support.
The process should be the same with USB 4, though I haven't tested.

If necessary on your machine, enable Thunderbolt in the BIOS.

If necessary, authorize the Thunderbolt eGPU.
I note multiple sources mention authorizing Thunderbolt, but I didn't have to on my machine.


## 3. Install the necessary drivers.

Check the [AMDGPU](https://wiki.archlinux.org/title/AMDGPU) ArchWiki-page for details.

For me I only had to install `xf86-video-amdgpu` and `vulkan-radeon`.

__NB:__ It is recommended to upgrade your machine first: `sudo pacman -Syu`


## 4. Install 'egpu-switcher'

Install [egpu-switcher](https://aur.archlinux.org/packages/egpu-switcher) from Arch User Repository.

```
# NB: If you don't know how to install apps from AUR, try reading up on it first!
# This is how I do it, but you should know what the commands do before running them!
git clone https://aur.archlinux.org/egpu-switcher.git
cd egpu-switcher
makepkg -sri
```


## 5. Enable `egpu-switcher`

Open a terminal and configure the switcher-tool:

```
sudo egpu-switcher config
```

You should see a list showing your internal GPU and your external GPU. Enter the number for your external GPU to configure `egpu-switcher`.

> If you cannot see your eGPU yet, do step 6 once before finishing step 5.
>
> You can also try `lspci` to list PCI-devices.

Then enable it:

```
sudo egpu-switcher enable
```


## 6. Restart your machine

Shutdown your machine fully and then start it again.

If necessary, unplug the eGPU while the machine is turned off,
and start it with the eGPU disconnected.
Reconnect the eGPU when you're in GRUB, before starting the OS.


# Resources:

This article is based on the following articles/resources:
- [eGPU Linux Core X Chroma](https://y.tsutsumi.io/2020/08/15/egpu-linux-core-x-chroma/)
- [egpu-switcher](https://github.com/hertg/egpu-switcher)
