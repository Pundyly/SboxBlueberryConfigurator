# S&box Blueberry Configurator

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

## Interface Layout

- **Top:** Welcome text, brief description, Path Entry + Select Folder button.
- **Center:** Scrollable list of options (`container.NewVScroll`) filling available space.
- **Bottom:** Large "Save to vcfg" button stretched across the window width (`container.NewBorder + container.NewMax`).

---
