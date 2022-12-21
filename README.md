# tldr-bash-framework
Framework for handling errors gracefully, colorize text and parse options in a readable manner.

## Functions

### Coloring

All color functions accept the following color values: `none`, `black`, `red`, `green`, `yellow`, `blue`, `magenta`, `cyan`, `light-gray`, `gray`, `light-red`, `light-green`, `light-yellow`, `light-blue`, `light-magenta`, `light-cyan`, `white`.

- `raw_foreground {{color_name}}` - obtain ANSI color sequence for a specific foreground color
- `raw_background {{color_name}}` - obtain ANSI color sequence for a specific background color
- `foreground {{color_name}}` - obtain interpreted ANSI color sequence for a specific foreground color
- `background {{color_name}}` - obtain interpreted ANSI color sequence for a specific background color
