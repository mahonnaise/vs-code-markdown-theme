# VS Code Markdown Theme

This is an official-looking Markdown CSS theme for VS Code with support for dark and high-contrast color themes. Compared to the standard theme, it uses larger fonts which are closer to what you might see in a blog. Block quotes and tables are a bit more polished. Code blocks scroll if necessary.

*theme.css* contains the bare-bones light version of the theme. It's container-filling. It has a 100% width and there aren't any margins at either side, top, or bottom. Margins only exist between block elements which means Markdown snippets will look great in dialogs and similar containers. If you want a max-width or some margins, just add them to your container.

*vs-code.css* contains VS Code specific tweaks and the color overrides for dark (`.vs-dark`) and high-contrast (`.hc-black`) color themes. It uses transparent shades of gray for things like borders and background colors. So, if you use a dark theme with a blue-ish background, you get shades of blue instead of completely unrelated grays.

## Installation

Clone this repo (or just grab those two CSS files) and then go to *File -> Preferences -> User Settings* and merge the JSON object you see there with this one:

```json
{
	"markdown.styles": [
		"file:///X:/foo/vs-code-markdown-theme/theme.css",
		"file:///X:/foo/vs-code-markdown-theme/vs-code.css",
		"file:///C:/Program%20Files%20(x86)/Microsoft%20VS%20Code/resources/app/out/vs/languages/markdown/common/tokens.css"
	]
}
```

Change the first two paths accordingly and adjust the last one if necessary. The last one is required for making syntax highlighting in fenced code blocks work.

If you use VS Code primarily for writing Markdown, you might as well also set `editor.wrappingColumn` to 0 while you're at it. Setting this to 0 enables viewport-width-wrapping which is more convenient for running text.

## Screenshots

### Light

![Light](screenshots/light.png?raw=true)

### Abyss (dark mode + background from theme)

![Abyss](screenshots/abyss.png?raw=true)

### Monokai (dark mode + background from theme)

![Monokai](screenshots/monokai.png?raw=true)

### High Contrast

![High Contrast](screenshots/high-contrast.png?raw=true)