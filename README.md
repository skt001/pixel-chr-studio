# 🎨 Pixel CHR Studio

A web-based NES Character ROM (CHR) editor for editing 8x8 pixel tiles and 16x16 metatiles.

[日本語版はこちら](README.ja.md)

## Features

- **Edit NES Character Data** - Load and edit CHR ROM files from NES games
- **Dynamic Tile Management** - Expand from 256 to 1024 tiles as needed
- **Multiple File Formats** - Support for NES, CHR, BIN, and ZIP files
- **Tile Tools** - Flip horizontal/vertical, rotate 90°, copy/paste
- **Real-time Preview** - 16x16 metatile preview while editing
- **Undo/Redo System** - Up to 50 undo steps
- **Multiple Export Formats** - CHR, BIN, PNG, or Hex dump
- **Responsive Design** - Works on desktop and tablet devices
- **Bilingual UI** - Available in Japanese (index.html) and English (index-en.html)

## Getting Started

### Installation

Simply open the HTML file in a modern web browser:

```bash
# Japanese version
open index.html

# English version
open index-en.html
```

Or access directly:
- Japanese: `pixel-chr-studio/index.html`
- English: `pixel-chr-studio/index-en.html`

### Usage

1. **Load a File**
   - Click the file input to select a NES, CHR, BIN, or ZIP file
   - The editor will automatically detect the file format and expand as needed

2. **Select a Tile**
   - Click on the grid (left panel) to select an 8x8 tile
   - The editor displays the tile magnified in the right panel

3. **Edit Pixels**
   - Click on tiles in the editor to paint with the selected color
   - Use keyboard shortcuts 0-3 to quickly change colors

4. **Transform Tiles**
   - **Flip H** - Flip horizontally
   - **Flip V** - Flip vertically
   - **Rotate** - Rotate 90° clockwise
   - **Copy/Paste** - Duplicate tiles

5. **Export**
   - Choose export format (CHR, BIN, PNG, or Hex)
   - Click "Export" to download the file

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Z` | Undo |
| `Ctrl+Shift+Z` | Redo |
| `Ctrl+C` | Copy tile |
| `Ctrl+V` | Paste tile |
| `0-3` | Select color palette |

## File Formats

- **NES** - Complete NES ROM file (CHR data auto-extracted)
- **CHR** - NES Character ROM (standard 8KB)
- **BIN** - Binary file (up to 16KB supported)
- **ZIP** - Archive containing NES/CHR/BIN file

## Color Palette

The editor uses a simple 4-color palette:

- **0 (Black)** - Background / Transparent
- **1 (Dark Gray)** - Shadow / Outline
- **2 (Light Gray)** - Midtone / Highlight
- **3 (White)** - Brightest highlight

## Technical Details

### Tile Storage

- Each tile is 16 bytes (2 bitplanes × 8 bytes)
- 256 tiles = 4 KB (minimum size)
- 512 tiles = 8 KB (standard NES)
- 1024 tiles = 16 KB (maximum size)

### Data Format

NES CHR data uses 2-bit planar format:
- Plane 1 (low bit) - bytes 0-7
- Plane 2 (high bit) - bytes 8-15

### Browser Requirements

- Chrome/Chromium 60+
- Firefox 55+
- Safari 11+
- Edge 79+

## Tips

- Tiles automatically expand in 256-tile blocks (4KB each)
- Undo history is maintained separately from saved data
- Metatile preview helps visualize tile arrangements
- Use PNG export for sharing artwork or documentation

## Limitations

- Maximum 1024 tiles (16KB)
- 4-color palette only (NES standard)
- Web-based (no offline save feature)
- Limited to modern browsers with Canvas support

## Future Enhancements

Potential features for future versions:
- Palette customization
- Animation preview
- Tile search and find/replace
- Batch operations
- Grid overlay options
- Import from PNG images

## Credits

Created by **skt001**

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For issues, questions, or suggestions:
- Check the Help (?) button in the application for usage documentation
- Review the Tips section for best practices

---

**Pixel CHR Studio** - Making NES sprite editing easy! 🎮
