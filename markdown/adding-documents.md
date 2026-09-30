# Adding Documents to the Markdown Viewer

The [Markdown Viewer](markdown-viewer.html) shows documents stored in the `markdown/` folder. A web page can't look inside a folder on the server by itself, so the viewer gets its list of documents from a file called `markdown/files.json`. **A document only appears in the viewer after it has been added to that list.**

## Step 1: Create the Markdown File

Write your document as a markdown (`.md`) file and save it in the `markdown/` folder.

When naming the file:

- Use lowercase letters, numbers, and hyphens, for example `network-basics.md`.
- Don't use spaces or special characters.
- End the name with `.md`.

## Step 2: Add the File to `files.json`

Open `markdown/files.json`. It holds a list of entries, one for each document:

```json
[
    {
        "file": "ethernet-cables-intro.md",
        "title": "An Introduction to Ethernet Cables"
    },
    {
        "file": "adding-documents.md",
        "title": "Adding Documents to the Markdown Viewer"
    }
]
```

Each entry has two parts:

| Key     | Meaning                                                   | Required? |
|---------|-----------------------------------------------------------|-----------|
| `file`  | The exact file name inside the `markdown/` folder.        | Yes       |
| `title` | The name shown in the viewer's dropdown menu.             | No. If it's left out, the file name is shown. |

To add a document, put a **comma** after the last entry's closing `}`, then add a new entry before the closing `]`:

```json
[
    {
        "file": "ethernet-cables-intro.md",
        "title": "An Introduction to Ethernet Cables"
    },
    {
        "file": "adding-documents.md",
        "title": "Adding Documents to the Markdown Viewer"
    },
    {
        "file": "network-basics.md",
        "title": "Network Basics"
    }
]
```

Documents appear in the dropdown in the same order as they are listed in this file, so you can reorder the entries to change the menu order.

## Common JSON Mistakes

JSON is strict. A single mistake stops the **whole** list from loading, and the viewer shows "File list unavailable." Check for these:

- **Missing comma between entries.** Every `}` except the last one needs a comma after it.
- **Extra comma after the last entry.** The final `}` must **not** have a comma after it.
- **Single quotes.** JSON only accepts double quotes: `"file"`, not `'file'`.
- **Mismatched file name.** The `file` value must match the real file name exactly, including capital letters and the `.md` extension.
- **Comments.** JSON doesn't allow comments, so don't add `//` or `/* */` notes to `files.json`.

To check the file, paste its contents into a JSON validator such as [jsonlint.com](https://jsonlint.com), or open it in VS Code, which underlines errors in red.

## Step 3: Test It Locally

The viewer loads files over the web, so it **doesn't work** if you double-click `markdown-viewer.html` to open it from your computer. Start a local web server from the `website` folder instead:

```
python -m http.server
```

(On some systems, the command is `python3` instead of `python`.)

Then open <http://localhost:8000/markdown-viewer.html> in your browser and choose your document from the dropdown. Press **Ctrl+C** in the terminal to stop the server when you're done.

## Step 4: Commit Your Changes

Commit **both** files to GitHub:

- the new `.md` file in `markdown/`
- the updated `markdown/files.json`

Use a descriptive commit message, such as `Add network basics document to markdown viewer`.

## Extra Tips

- **Linking directly to a document:** add `?file=` and the file name to the viewer's address, for example `markdown-viewer.html?file=network-basics.md`.
- **Images and links inside a document:** paths are read from the `website` folder, not from `markdown/`. If an image is saved at `markdown/images/diagram.png`, refer to it as `markdown/images/diagram.png` in your markdown.
- **Supported formatting:** headings, bold and italic text, lists, links, images, tables, block quotes, and code blocks all display correctly. For HTML safety, the viewer removes scripts and other unsafe HTML.
