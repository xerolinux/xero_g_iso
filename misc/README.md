# XeroLinux "G" ISO Repo

Repo for the **Xero-G** Project. Feel free to go through files and learn how it's all done. To build ISO need to use **ABS** Script via guide below.

<p align="center">
    <img width="300" src="https://i.imgur.com/QWqMIsr.png" alt="logo">
</p>

<h1 align="center">You must be on an *Arch* based Distro to build ISO.</h1>

> The following are not supported Distros to build on since they
> don't use Arch repos which will result in errors building the ISO.
> - Manjaro (Own Repos)
> - CachyOS (Arch v3)
> - KaOS (Limited Repos)
> - Artix (No Systemd)
-----------------------------------------------------------------
### Note
> This here, is a side project, it will keep changing, keeping my skills sharp GNOME wise...
> There will **Never** be a public ISO. In case you can't for whatever reason, one will be made available,
> only on Patreon, via our $25 Tier. Feel free jo join us [There](https://patreon.com/XeroLinux) <sup>[**`Why Paid ?`**](https://github.com/xerolinux/xero_g_iso/blob/main/support.md)</sup>
-----------------------------------------------------------------

<h1 align="center">.:: Video Guide ::.</h1>

<p align="center">

   <a href="https://youtu.be/RMFfumECkmg" target="_blank" title="Video Guide"><img src="https://i.imgur.com/dtKGQgJ.jpeg" alt="Watch Video Guide" /></a>

</p>

### Step 1 - Get Repo in to build :

Before we get started we will need to get the **ABS** repo in, that's where the new build tool is located. To do so need to edit the "pacman.conf" :

```
sudo nano /etc/pacman.conf
```

Now we need to add the repo at the end of the file, so add this,
```
# Valen Repository
[valen_repo]
SigLevel = Never
Server = https://keyaedisa.github.io/$repo/$arch
```
Now install the tool via,
```
sudo pacman -S abs
```
### Step 2 - Clone Build Repo :

Once you got Repos in, time to grab the build environment that you will be building from. Just note that you will need Git installed in order to do that.

**Install Git with :**
```
sudo pacman -S git
```
**Grab Build Env.**
```
cd ~ && git clone https://github.com/xerolinux/xero_g_iso.git
```

### Step 3 - Building the Xero ISO :

Now that we have build environment on our system, it's time to build it.

**Build ISO :**
```
cd ~/xero_g_iso/ && abs XeroG
```

Follow the prompts and you good to go...

I hope this helps.. In case of other issues kindly find me on [**Discord**](https://discord.gg/Xg6T78ahtK)

Happy building