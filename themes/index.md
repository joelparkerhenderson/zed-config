# Zed themes

This repository has my personal favorite Zed themes.

Key sections:

- Metadata: Theme name, author, and appearance (dark/light)
- UI Colors: Background, borders, panels, status bar, tabs, scrollbars
- Editor Colors: Text, line numbers, selection, highlights
- Terminal Colors: Full ANSI color palette (16 colors with normal, bright, and dim variants)
- Status Colors: Error, warning, success, info, hint states
- Git Colors: Created, modified, deleted, conflict states
- Syntax Highlighting: Colors for keywords, strings, functions, comments, types, etc.
- Multiplayer: Cursor and selection colors for collaborative editing

To use this theme:

1. Place the JSON file in your Zed themes directory (usually ~/.config/zed/themes/)

2. Restart Zed or reload themes

3. Open the Zed theme picker: Cmd/Ctrl + K, then Cmd/Ctrl + T.

4. Select "joelparkerhenderson-dark".

## Goals

- background: black

- text: white

- text-muted: off white

- comment: green

- selection background: gray translucent

## Top-Level Structure

**`$schema`** - Points to Zed's JSON schema for validation and autocomplete in editors

**`name`** - The theme family name (can contain multiple theme variants)

**`author`** - Creator of the theme

**`themes`** - Array containing one or more theme variants (e.g., dark and light versions)

## Theme Variant Properties

**`name`** - Individual theme variant name shown in the theme picker

**`appearance`** - Either "dark" or "light", tells Zed which mode this theme is for

**`style`** - Contains all color definitions

## UI Element Colors

**Border Colors:**
- `border` - Default border color for panels and UI elements
- `border.variant` - Alternative border color for visual hierarchy
- `border.focused` - Border color when an element has focus
- `border.selected` - Border color for selected items
- `border.transparent` - Fully transparent border (useful for borderless designs)
- `border.disabled` - Border color for disabled elements

**Surface Colors:**
- `elevated_surface.background` - Background for floating panels and dialogs
- `surface.background` - Standard surface background
- `background` - Main editor/window background color
- `element.background` - Background for interactive elements like buttons
- `element.hover` - Background when hovering over elements
- `element.active` - Background when clicking/activating elements
- `element.selected` - Background for selected elements
- `element.disabled` - Background for disabled elements

**Drop Target:**
- `drop_target.background` - Highlight color when dragging files over a drop zone

**Ghost Elements** (transparent/subtle UI elements):
- `ghost_element.background` - Base background for ghost buttons
- `ghost_element.hover` - Ghost element hover state
- `ghost_element.active` - Ghost element active/pressed state
- `ghost_element.selected` - Ghost element selected state
- `ghost_element.disabled` - Ghost element disabled state

**Text Colors:**
- `text` - Primary text color
- `text.muted` - Secondary/less important text
- `text.placeholder` - Placeholder text in inputs
- `text.disabled` - Text for disabled elements
- `text.accent` - Accent color for highlighted text

**Icon Colors:**
- `icon` - Default icon color
- `icon.muted` - Muted/secondary icons
- `icon.disabled` - Disabled icon state
- `icon.placeholder` - Placeholder icons
- `icon.accent` - Accent color for important icons

**Specific UI Components:**
- `status_bar.background` - Bottom status bar background
- `title_bar.background` - Top window title bar background
- `toolbar.background` - Toolbar background color
- `tab_bar.background` - Tab bar background
- `tab.inactive_background` - Inactive tab background
- `tab.active_background` - Active tab background
- `search.match_background` - Highlight color for search results
- `panel.background` - Side panels background (file tree, terminal, etc.)
- `panel.focused_border` - Border for the currently focused panel
- `pane.focused_border` - Border for the focused editor pane

**Scrollbar:**
- `scrollbar.thumb.background` - The draggable scrollbar handle
- `scrollbar.thumb.hover_background` - Scrollbar handle when hovering
- `scrollbar.thumb.border` - Border around scrollbar handle
- `scrollbar.track.background` - Background of the scrollbar track
- `scrollbar.track.border` - Border of the scrollbar track

## Editor-Specific Colors

- `editor.foreground` - Default text color in the editor
- `editor.background` - Editor pane background
- `editor.gutter.background` - Line number gutter background
- `editor.subheader.background` - Breadcrumb/navigation header background
- `editor.active_line.background` - Highlight for the current line
- `editor.highlighted_line.background` - Background for specifically highlighted lines
- `editor.line_number` - Inactive line numbers color
- `editor.active_line_number` - Current line number color
- `editor.invisible` - Color for invisible characters (spaces, tabs)
- `editor.wrap_guide` - Vertical line showing wrap/margin column
- `editor.active_wrap_guide` - Wrap guide for the active line
- `editor.document_highlight.read_background` - Highlight for read occurrences of symbol under cursor
- `editor.document_highlight.write_background` - Highlight for write occurrences of symbol under cursor

## Terminal Colors

**Basic Terminal:**
- `terminal.background` - Terminal pane background
- `terminal.foreground` - Default terminal text color
- `terminal.bright_foreground` - Bright text variant
- `terminal.dim_foreground` - Dimmed text variant

**ANSI Color Palette** (each has three variants):
For each color (black, red, green, yellow, blue, magenta, cyan, white):
- `terminal.ansi.[color]` - Standard color
- `terminal.ansi.bright_[color]` - Bright variant (used for bold text)
- `terminal.ansi.dim_[color]` - Dimmed variant (used for faint text)

These follow the standard 16-color ANSI terminal color scheme.

## Link Colors

- `link_text.hover` - Color for links when hovering

## Diagnostic/Status Colors

Each status type has three properties (background, border, and foreground):

**Conflict** (merge conflicts):
- `conflict` - Foreground color
- `conflict.background` - Background highlight
- `conflict.border` - Border color

**Created** (new files in git):
- `created`, `created.background`, `created.border`

**Deleted** (removed content):
- `deleted`, `deleted.background`, `deleted.border`

**Error** (syntax errors, problems):
- `error`, `error.background`, `error.border`

**Hidden** (hidden files/elements):
- `hidden`, `hidden.background`, `hidden.border`

**Hint** (subtle suggestions):
- `hint`, `hint.background`, `hint.border`

**Ignored** (gitignored files):
- `ignored`, `ignored.background`, `ignored.border`

**Info** (informational messages):
- `info`, `info.background`, `info.border`

**Modified** (changed files):
- `modified`, `modified.background`, `modified.border`

**Predictive** (AI code suggestions):
- `predictive`, `predictive.background`, `predictive.border`

**Renamed** (renamed files):
- `renamed`, `renamed.background`, `renamed.border`

**Success** (successful operations):
- `success`, `success.background`, `success.border`

**Unreachable** (unreachable code):
- `unreachable`, `unreachable.background`, `unreachable.border`

**Warning** (warnings):
- `warning`, `warning.background`, `warning.border`

## Multiplayer/Collaboration

**`players`** - Array of color schemes for different users in collaborative editing. Each player object has:
- `cursor` - Cursor color for that user
- `background` - Background color for that user's presence
- `selection` - Selection highlight color for that user

## Syntax Highlighting

The `syntax` object defines colors for code tokens. Each can have:
- `color` - The text color
- `font_style` - Optional: "normal", "italic", "oblique"
- `font_weight` - Optional: 100-900 (700 = bold)

**Common syntax tokens:**

- `attribute` - HTML/XML attributes, decorators, annotations
- `boolean` - true/false literals
- `comment` - Regular comments
- `comment.doc` - Documentation comments
- `constant` - Constants and constant values
- `constructor` - Constructor functions/methods
- `embedded` - Embedded language code (like JavaScript in HTML)
- `emphasis` - Markdown emphasis
- `emphasis.strong` - Bold/strong emphasis
- `enum` - Enumeration types
- `function` - Function names
- `hint` - Inline hints from the editor
- `keyword` - Language keywords (if, else, for, etc.)
- `label` - Labels for goto/break statements
- `link_text` - Markdown link text
- `link_uri` - URLs and URIs
- `number` - Numeric literals
- `operator` - Operators (+, -, *, ==, etc.)
- `predictive` - AI-predicted code
- `preproc` - Preprocessor directives
- `primary` - Default/primary syntax color
- `property` - Object properties and fields
- `punctuation` - General punctuation
- `punctuation.bracket` - Brackets [], {}, ()
- `punctuation.delimiter` - Delimiters like commas, semicolons
- `punctuation.list_marker` - Markdown list markers
- `punctuation.special` - Special punctuation characters
- `string` - String literals
- `string.escape` - Escape sequences in strings (\n, \t)
- `string.regex` - Regular expressions
- `string.special` - Special strings (template literals, etc.)
- `string.special.symbol` - Symbols in strings
- `tag` - HTML/XML tags
- `text.literal` - Literal text in markup
- `title` - Headings and titles
- `type` - Type names and type annotations
- `variable` - Variable names
- `variable.special` - Special variables (self, this, etc.)
- `variant` - Enum variants
