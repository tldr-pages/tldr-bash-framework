# tldr-bash-framework

Framework for handling errors gracefully, colorize text and parse options in a readable manner.

No dependencies exist for this script: it's self-contained.

## Functions

### Coloring

All color functions accept the following color values: `none`, `black`, `red`, `green`, `yellow`, `blue`, `magenta`, `cyan`, `light-gray`, `gray`, `light-red`, `light-green`, `light-yellow`, `light-blue`, `light-magenta`, `light-cyan`, `white`.

- `raw_foreground {{color_name}}` - obtain ANSI color sequence for a specific foreground color
- `raw_background {{color_name}}` - obtain ANSI color sequence for a specific background color
- `foreground {{color_name}}` - obtain interpreted ANSI color sequence for a specific foreground color
- `background {{color_name}}` - obtain interpreted ANSI color sequence for a specific background color

### Error reporting

All error reporting functions without `user_` prefix must not be used to display messages for user - they are for developers.
`main` is shown instead of function name when internal error reporting function was called outside another function.

- `info {{description}}` - display internal info note in the following format: `{{function_caused_this_message_to_appear|main}}: info: {{description}}`
- `warn {{description}}` - display internal warning note in the following format: `{{function_caused_this_message_to_appear|main}}: warn: {{description}}`
- `error {{description}}` - display internal error note in the following format: `{{function_caused_this_message_to_appear|main}}: error: {{description}}`

- `user_info {{description}}` - display user info note in the following format: `info: {{description}}`
- `user_warn {{description}}` - display user warning note in the following format: `warn: {{description}}`
- `user_error {{description}}` - display user error note in the following format: `error: {{description}}`
