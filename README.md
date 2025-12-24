# 🫐 S&box Blueberry Configurator 🫐

A lightweight GUI application written in **Go + Fyne** for generating a `graphics_config.vcfg` file for **S&box**.  
It allows users to set graphical options through a simple interface and save them directly to the game’s configuration folder.

---

## Purpose

- Provides a small, user-friendly GUI for configuring S&box graphics options.
- Generates a ready-to-use `graphics_config.vcfg` file in the correct game directory.

---

## Features

- Displays a predefined set of options (boolean, integer, and float) with labels and default values.
- Boolean options are represented as checkboxes; numeric/text options use Entry fields.
- **Path field** at the top lets the user specify the root S&box folder manually or via a folder selection dialog.
- **Save button**:
  - Creates `<path>/core/cfg` folder if it doesn’t exist.
  - Writes `graphics_config.vcfg` in the folder.
  - File format: header comment + lines in `key value` format (boolean values as 1/0).
- **Select Folder button** opens a folder selection dialog.

---

## Steam Launch Option

To automatically apply the configuration on game start, add the following to **Steam Launch Options**:

-exec graphics_config.vcfg


Make sure the `graphics_config.vcfg` file is saved in:

<path_to_sbox>/core/cfg/graphics_config.vcfg


This ensures the game executes your custom graphics configuration every time it launches.
