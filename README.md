<h1 align="center">EasyEffects-Presets</h1>


**Presets for [EasyEffects](https://wwmm.github.io/easyeffects) on [Pipewire](https://pipewire.org) (Bose, Music, Serie&Film, Sony and TV&Docu).**

## Installation for GNU/Linux distributions using AUR
You can now install the presets with an AUR-Helper such as `pikaur` (recommended).
```console
pikaur -S easyeffects-bundy01-presets
```

Or manually
```console
pacman -S --needed git base-devel
git clone https://aur.archlinux.org/easyeffects-bundy01-presets.git
cd easyeffects-bundy01-presets
makepkg -fsri
rm -rf easyeffects-bundy01-presets
```

## Installation for other distributions
* Install `easyeffects` and its dependencies.

### Download of presets
* Click on `Code` in this repository.
* Then select `Download ZIP`.

### Import of presets
* You can use the `Presets` button in Easyeffects, select `Local` and choose `Import preset file`.
Or
* Move the **JSON** presets to `~/.config/easyeffects/output`.
* If you have installed EasyEffects with Flatpak, it's here `~/.var/app/com.github.wwmm.easyeffects/config/easyeffects/output`.

### Presets dependencies
You will need to install the `calf` or `calf-plugins`, `mda.lv2` or `mda-lv2` and `lsp-plugins-lv2` packages from your GNU/Linux distribution to enable the presets effects.

## Settings
* **Bass adjustment**
    * Change the bass settings to suit the level of your speakers if the presets aren’t to your liking, use EasyEffects in `Presets`, select an audio preset and then change `Loudness` in dB from `Bass Loudness` effect if your speakers don’t have a bass control.
	* Save preset changes if the settings are adjusted using EasyEffects.

* **Video presets**
	* If you get audio crackling when using this presets, you'll need to increase Pipewire's Quantum. **The following command is valid for the current session only.**
```console
pw-metadata -n settings 0 clock.force-quantum VALUE
```

**VALUE:** This must be a value between 1024 and 8192. For example `2048`.
This number should be as small as possible (without cracking), because increasing the Quantum also increases latency. You can see this with the `pw-top` command.

* If for any reason you wish to revert to the default Quantum during the session.
```console
pw-metadata -n settings 0 clock.force-quantum 0
```


<h1 align="center">🖤️ Enjoy the Sound 🖤️</h1>
