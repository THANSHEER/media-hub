# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a **media asset repository** storing demonstration videos, animations, and images for various Obsidian plugins and browser extensions. It serves as a CDN source for documentation, marketing materials, and README files across related projects.

**Public repo:** https://github.com/THANSHEER/media

### Projects Covered
- **detube**: Browser extension demo videos
- **obsidian-mermaid-flow**: Mermaid diagram plugin for Obsidian
- **obsidian-omnichat**: Omnifunctional chat plugin for Obsidian
- **obsidian-noteflare**: Note enhancement plugin for Obsidian
- **mdsite**: Markdown documentation site

## Media Organization

Each project directory follows a standardized structure with four format subdirectories:

```
project-name/
├── raw/              # Original source files (.mov, .png, etc.)
├── webm/             # WebM video format (web-optimized for video)
├── animated-webp/    # Animated WebP (optimized animations, ~30-50% smaller than WebM)
└── webp/             # Static WebP images
```

### Format Guidelines

- **raw/**: Store original high-quality source files. Use meaningful names with descriptors (e.g., `obsidian-meramaid-create-mermaid-daigram.mov`)
- **webm/**: Generated web video format. Use same base name as source but with `.webm` extension
- **animated-webp/**: Generated animated WebP for GIF-like content. Better compression than WebM for animations
- **webp/**: Static screenshots/images converted to WebP format

### File Naming Convention

Use descriptive kebab-case names that clearly indicate what the media demonstrates:
```
[product-name]-[feature-description].[extension]
```

Examples:
- `detube-quick-enable:disable-extension.webm`
- `obsidian-meramaid-ai-mermadi-generater.webp`
- `obsidian-omnichat-chat-interface.animated.webp`

## Working with Media Assets

### Adding New Media

1. **Place raw files** in the `raw/` subdirectory of the relevant project
2. **Convert to web formats**:
   - Use FFmpeg for video → WebM conversion
   - Use ImageMagick or similar for image → WebP conversion
   - Use appropriate tools for animated content → animated WebP
3. **File size expectations**: Individual media files typically range 50-100MB for the entire project; aim for optimized file sizes in web formats (WebM should be < 5MB per video, WebP < 1MB per image)

### Referencing Media in External Repos

Media files in this repo can be referenced via raw GitHub URLs:
```
https://raw.githubusercontent.com/THANSHEER/media/main/project-name/format/filename.ext
```

Example:
```
https://raw.githubusercontent.com/THANSHEER/media/main/detube/webm/detube-videpage.webm
```

### Storage Considerations

- Repository is public; all media is visible to the world
- Keep media organized and consistently named for easy reference
- Remove unused or outdated media to maintain repository cleanliness
- Total repo size is anticipated at 50-100MB+

## Git Workflow

1. **Adding media**: `git add project-name/format/filename`
2. **Committing**: Use descriptive messages like `Add demo videos for mermaid flow plugin`
3. **Pushing**: Standard `git push origin main` (repository is public)

## File Format Recommendations

| Use Case | Format | Characteristics |
|----------|--------|-----------------|
| Video demos | WebM | Good compression, broad browser support, streaming-friendly |
| Animated GIFs | Animated WebP | Superior compression vs GIF, smooth animations |
| Static screenshots | WebP | Modern format, ~25% smaller than PNG, lossless/lossy options |
| Archival | MOV/Original | Keep source for future re-encoding if needed |

## No Build/Test Commands

This is a media repository with no build, test, or lint steps. All work involves managing media files directly via git.

## Important Notes

- **License**: MIT License (see LICENSE file) — all media is freely usable
- **Copyright**: Copyright (c) 2026 MOHAMMED THANSEER
- **Public visibility**: Repository is public; ensure media content is appropriate for public distribution
