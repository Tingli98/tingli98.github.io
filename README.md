# Ting Li — Academic Homepage

Based on [Minimal-Academic-Website](https://github.com/yuhui-zh15/Minimal-Academic-Website) by Yuhui Zhang.

## Publish on GitHub Pages

1. Create a public GitHub repository named **`<your-username>.github.io`**.
2. Upload every file in this folder to it (drag-and-drop in the GitHub web page works).
3. Go to **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
4. In a minute or two the site is live at `https://<your-username>.github.io`.

## Editing

| What | Where |
|---|---|
| Name, intro, research, experience, education, awards | `index.html` |
| Advisor, GitHub, LinkedIn, News | `index.html`: uncomment the marked lines |
| Profile photo | save as `images/profile.jpg` (it's hidden until the file exists) |
| Publications | `publications.json` (format below) |
| Colors and fonts | `styles.css` (`:root` at the top) |

### Adding a paper to `publications.json`

```json
{
  "publications": [
    {
      "title": "Paper Title",
      "authors": ["Ting Li", "Coauthor One", "Advisor Name"],
      "venue": "ACM/IEEE HRI 2026",
      "thumbnail": "images/thumbs/paper1.jpg",
      "selected": 1,
      "award": "",
      "links": { "pdf": "https://...", "doi": "https://...", "code": "https://...", "video": "https://...", "project": "https://..." }
    }
  ]
}
```

- "Ting Li" is highlighted automatically (an asterisk or dagger after it is fine).
- `selected: 1` shows the paper by default; `0` shows it only under "Show All".
- `thumbnail`, `award` and each link are optional; leave out any you don't have.

## Preview locally

```bash
python3 -m http.server
# open http://localhost:8000
```
