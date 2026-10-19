# rohittir.github.io

Personal portfolio. One file, `index.html`, plain HTML and CSS, no build step.

## Deploy (first time)

Run from inside this `site/` folder:

```bash
git init -b main
git add .
git commit -m "Portfolio site"
gh repo create rohittir.github.io --public --source=. --push
```

GitHub Pages turns on automatically for a repo named `<username>.github.io`. The site is live at https://rohittir.github.io within a couple of minutes. If it is not, enable it once:

```bash
gh api -X POST repos/rohittir/rohittir.github.io/pages -f "source[branch]=main" -f "source[path]=/"
```

## Update

Edit `index.html`, then:

```bash
git commit -am "Update" && git push
```

## Preview locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765.

## To do

- Add `headshot.jpg` and uncomment the `<img>` in `index.html`.
- Add `resume.pdf` and uncomment the Resume button.
