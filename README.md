# EasyEffects-Presets
**Presets for [EasyEffects](https://github.com/wwmm/easyeffects) on [Pipewire](https://pipewire.org/) (Bose, Music, Sony and Video).**

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
* You can use the `Import Preset` button that is beside the `Add` preset button.

Or
* Move the **JSON** presets to `~/.config/easyeffects/output`.
* If you have installed EasyEffects with Flatpak, it's here `~/.var/app/com.github.wwmm.easyeffects/config/easyeffects/output`.

### Presets dependencies
You will need to install the `mda.lv2` or `mda-lv2`, `lsp-plugins-lv2` and `zam-plugins-lv2` or `zam-plugins` packages from your GNU/Linux distribution to enable the presets effects.


## Settings
* **Bass**
	* Adjust your bass to the speaker levels if the presets are not suitable or use EasyEffects in `Preset`, select a preset and then change `Loudness` in dB from `Bass Loudness` effect.
	* Saves the changes in `Preset`.

* **Video Preset**
	* If you get audio crackling when using this preset, you'll need to increase Pipewire's Quantum. **The following command is valid for the current session only.**
```console
pw-metadata -n settings 0 clock.force-quantum VALUE
```

**VALUE:** This is a multiple of 8 and greater than 1024. Its maximum value is 8192. For example `2048`.
This number should be as small as possible (without cracking), because increasing the Quantum also increases latency. You can see this with `pw-top`.

* If for any reason you wish to revert to the default Quantum during the session.
```console
pw-metadata -n settings 0 clock.force-quantum 0
```

# 🖤️ Enjoy the sound 🖤️
