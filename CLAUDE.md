# Claude Code Instructions

## Platform
This site is used on both desktop and mobile. Always consider both when implementing UI features (e.g. hover-only interactions don't work on touch screens).

## Logo Processing
- rembg venv is at ~/rembg-venv (`~/rembg-venv/bin/rembg i input.png output.png`)
- For simple white backgrounds: replace near-white pixels (r,g,b > 240) with transparency via PIL
- Dark/light variants: `name.png` = dark mode (default), `name-light.png` = light mode
- For black logos: invert colors for the dark variant, keep original as light
- For colored logos on dark backgrounds: add subtle white outline using PIL MaxFilter(5) on alpha channel
- Always check results visually before and after processing
