A plugin for Obsidian that aims to make typesetting LaTeX math as fast as handwriting.

Inspired by [Gilles Castel's setup using UltiSnips](https://castel.dev/post/lecture-notes-1/).

![[8a80652f7df5c66c0bbf6ffca0410d5a_MD5.gif]]

The plugin's main feature is **snippets**, which help you write LaTeX quicker through shortcuts and text expansion! For example, type

- "sqx" instead of "\sqrt{x}"
- "a/b" instead of "\frac{a}{b}"
- "par x	y	" instead of "\frac{\partial x}{\partial y}"

See [Gilles Castel's writeup](https://castel.dev/post/lecture-notes-1/) for more information.


The plugin comes with a [set of default snippets](https://github.com/artisticat1/obsidian-latex-suite/blob/main/src/default_snippets.ts), loosely based on [Gilles Castel's](https://castel.dev/post/lecture-notes-1/#other-snippets). You can modify them, remove them, and write your own.


## Usage
To get started, type "dm" to enter display math mode. Try typing the following:

- "xsr" → "x^{2}".

- "x/y <kbd>Tab</kbd>" → "\\frac{x}{y}".

- "sin @t" → "\\sin \\theta".

**Have a look at the [cheatsheet](#cheatsheet)** for a list of commonly used default snippets.


Once these feel familiar, you can check out the [default snippets](https://github.com/artisticat1/obsidian-latex-suite/blob/main/src/default_snippets.ts) for more commands. e.g.

- "par <kbd>Tab</kbd> f <kbd>Tab</kbd> x <kbd>Tab</kbd>" → "\\frac{\\partial f}{\\partial x}".

- "dint <kbd>Tab</kbd> 2pi <kbd>Tab</kbd> sin @t <kbd>Tab</kbd> @t <kbd>Tab</kbd>" → "\\int_{0}^{2\pi} \\sin \\theta \\, d\\theta".


You can also add your own snippets! [See here for more info on writing snippets](#snippets). You can [view snippets written by others and share your own snippets here](https://github.com/artisticat1/obsidian-latex-suite/discussions/50).


## Features
### Auto-fraction
Lets you type "1/x" instead of "\frac{1}{x}".

For example, it makes the following expansions:

- `x/` → `\frac{x}{}`
- `(a + b(c + d))/` → `\frac{a + b(c + d)}{}`

and moves the cursor inside the brackets.

Once done typing the denominator, press <kbd>Tab</kbd> to exit the fraction.

![[d3a9a923138b9f578dcf6ff11e12ff5a_MD5.gif]]


### Matrix shortcuts
While inside a matrix, array, align, or cases environment,

- Pressing <kbd>Tab</kbd> will insert the "&" symbol
- Pressing <kbd>Enter</kbd> will insert "\\\\" and move to a new line
- Pressing <kbd>Shift + Enter</kbd> will move to the end of the next line (can be used to exit the matrix)

![[5440fe2a725d7a18bfbf9a452948a5ad_MD5.gif]]


### Conceal
*This feature must be enabled in settings!*

Make your equations more readable by hiding LaTeX code, instead rendering it in a pretty format.

For example, "\dot{x}^{2} + \dot{y}^{2}" will be displayed as "ẋ² + ẏ²".

To reveal the LaTeX code, move the cursor over it.

![[c4eeafe97ce8551730cda02adb4155a7_MD5.png]]
![[6837dc07b30c50d4d901ecb18d76378e_MD5.gif]]


### Tabout
- Pressing <kbd>Tab</kbd> while the cursor is at the end of an equation will move the cursor outside the $ symbols.
- Otherwise, pressing <kbd>Tab</kbd> will advance the cursor to the next closing bracket: ), ], }, >, or |.


### Preview inline math
When the cursor is inside inline math, a popup window showing the rendered math will be displayed.

<img width=500 src="https://raw.githubusercontent.com/artisticat1/obsidian-latex-suite/main/gifs/inline_math_preview_1.png">
<img width=650 src="https://raw.githubusercontent.com/artisticat1/obsidian-latex-suite/main/gifs/inline_math_preview_2.png">


### Color & highlight matching brackets
- Matching brackets are rendered in the same color, to help with readability.
- When the cursor is adjacent to a bracket, that bracket and its pair will be highlighted.
- When the cursor is inside brackets, the enclosing brackets will be highlighted.

![[e5bbda949ab8b38d48fae84d8b5ff2a5_MD5.gif]]


### Visual snippets
Sometimes you want to annotate math, or cancel or cross out terms. Selecting some math with the cursor and typing

- "U" will surround it with "\\underbrace".
- "C" will surround it with "\\cancel".
- "K" will surround it with "\\cancelto".
- "B" will surround it with "\\underset".

![[8a5d6117efebc911811ec166d462793d_MD5.gif]]


### Auto-enlarge brackets
When a snippet containing "\\sum", "\\int" or "\\frac" is triggered, any enclosing brackets will be enlarged with "\\left" and "\\right".

![[91bd781e6ac8733cdb728c91e6754abb_MD5.gif]]


### Editor commands
- Box current equation – surround the equation the cursor is currently in with a box.
- Select current equation – select the equation the cursor is currently in.


### Snippets
Snippets are formatted as follows:

```typescript
{trigger: string | RegExp, replacement: string, options: string, priority?: number, description?: string, flags?: string}
```

- `trigger` : The text that triggers this snippet.
- `replacement` : The text to replace the `trigger` with.
- `options` : See below.
- `priority` (optional): This snippet's priority. Snippets with higher priority are run first. Can be negative. Defaults to 0.
- `description` (optional): A description for this snippet.
- `flags` (optional): Flags for regex snippets.


#### Options
- `t` : Text mode. Only run this snippet outside math
- `m` : Math mode. Only run this snippet inside math. Shorthand for both `M` and `n`
- `M` : Block math mode. Only run this snippet inside a `$$ ... $$` block
- `n` : Inline math mode. Only run this snippet inside a `$ ... $` block
- `A` : Auto. Expand this snippet as soon as the trigger is typed. If omitted, the <kbd>Tab</kbd> key must be pressed to expand the snippet
- `r` : Regex. The `trigger` will be treated as a regular expression
- `w` : Word boundary. Only run this snippet when the trigger is preceded (and followed by) a word delimiter, such as `.`, `,`, or `-`.
- `c` : Code mode. Only run this snippet inside a ```` ``` ... ``` ```` block

Insert **tabstops** for the cursor to jump to by writing "$0", "$1", etc. in the `replacement`.

For more details on writing snippets, including **regex** snippets, [see the documentation here](DOCS.md). You can [view snippets written by others and share your own snippets here](https://github.com/artisticat1/obsidian-latex-suite/discussions/50).

> [!WARNING]
> Snippet files are interpreted as JavaScript and can execute arbitrary code.
> Always be careful with snippets shared from others to avoid running malicious code.


## Cheatsheet

| Trigger            | Replacement      |
| ------------------ | ---------------- |
| mk                 | \$ \$            |
| dm                 | \$\$<br><br>\$\$ |
| sr                 | ^{2}             |
| cb                 | ^{3}             |
| rd                 | ^{ }             |
| \_                 | \_{ }            |
| sq                 | \\sqrt{ }        |
| x/y <kbd>Tab</kbd> | \\frac{x}{y}     |
| //                 | \\frac{ }{ }     |
| te <kbd>Tab</kbd>  | \\text{ }        |
| x1                 | x_{1}            |
| x,.                | \\mathbf{x}      |
| x.,                | \\mathbf{x}      |
| xdot               | \\dot{x}         |
| xhat               | \\hat{x}         |
| xbar               | \\bar{x}         |
| xvec               | \\vec{x}         |
| xtilde             | \\tilde{x}       |
| xund               | \\underline{x}   |
| ee                 | e^{ }            |

When running a snippet that **moves the cursor inside brackets {}, press <kbd>Tab</kbd> to exit the brackets**.


### Greek letters

| Trigger | Replacement  | Trigger | Replacement | Why|
| ------- | ------------ | ------- | ----------- | - |
| @a      | \\alpha      | eta     | \\eta       | Because |
| @b      | \\beta       | mu      | \\mu        | Because |
| @g      | \\gamma      | nu      | \\nu        | Because |
| @G      | \\Gamma      | xi      | \\xi        | Because |
| @d      | \\delta      | Xi      | \\Xi        | Because |
| @D      | \\Delta      | pi      | \\pi        | Because |
| @e      | \\epsilon    | Pi      | \\Pi        | Because |
| :e      | \\varepsilon | rho     | \\rho       | Because |
| @z      | \\zeta       | tau     | \\tau       | Because |
| @t      | \\theta      | phi     | \\phi       | Because |
| @T      | \\Theta      | Phi     | \\Phi       | Because |
| @k      | \\kappa      | chi     | \\chi       | Because |
| @l      | \\lambda     | psi     | \\psi       | Because |
| @L      | \\Lambda     | Psi     | \\Psi       | Because |
| @s      | \\sigma      |         |             | Because |
| @S      | \\Sigma      |         |             | Because |
| @o      | \\omega      |         |             | Because |
| ome     | \\omega      |         |             | Because |


For greek letters with short names (2-3 characters), just type their name,
e.g. "pi" → "\\pi"



## Contributing
Any contributions and PRs are welcome!



## Acknowledgements
- [@tth05](https://github.com/tth05)'s [Obsidian Completr](https://github.com/tth05/obsidian-completr) for the basis of the tabstop code
- [Dynamic Highlights](https://github.com/nothingislost/obsidian-dynamic-highlights/blob/master/src/settings/ui.ts) for reference
- [Quick Latex for Obsidian](https://github.com/joeyuping/quick_latex_obsidian) for inspiration



## Support
If you like this plugin and want to say thanks, you can buy me a coffee here!