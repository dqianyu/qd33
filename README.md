===================================

This is a quick reference for how to update Hugo site (qd33) and deploy changes to GitHub Pages.

Project assumptions
-------------------
- Site repo folder: qd33
- Hugo outputs built site into: docs/
- GitHub Pages serves from: main branch / docs folder
- You have this in config.toml:
    publishDir = "docs"

--------------------------------------------------
1. Where to change things
--------------------------------------------------

1.1. Change text / add content
------------------------------

Edit files under the content/ directory:

- Home page:
    content/_index.md

- Research page:
    content/research/_index.md

- Teaching page:
    content/teaching/_index.md

- Publications:
    content/publication/*.md

Example front matter for a publication:

    ---
    title: "Paper title"
    authors: "First Last, Second Author, Qianyu Dong"
    periodical: "Journal Name"
    status: "submitted"    # or "accepted", "published"
    link: "https://..."
    code: "https://github.com/..."  # optional
    date: 2025-12-01
    type: "publications"
    ---

1.2. Change layout / structure
------------------------------

Edit files under layouts/:

- Publications list page:
    layouts/publications/list.html

- Header and footer:
    layouts/partials/header.html
    layouts/partials/footer.html

Use these when you want to change HOW things are displayed
(order, labels, sections, etc.), not the actual text content.

1.3. Change styles (colors, fonts, sizes)
-----------------------------------------

Edit CSS under static/css/:

- Main theme styles (includes dark/light mode):
    static/css/style.css

- Personal overrides and tweaks:
    static/css/theme-override.css

Important:
- NEVER edit docs/css/*.css by hand. docs/ is generated output
  and will be overwritten by Hugo.

--------------------------------------------------
2. How to check changes locally
--------------------------------------------------

From the repo root:

    cd qd33
    hugo server --disableFastRender

Then open the local URL printed in the terminal, usually:

    http://localhost:1313/

Check:

- Home:          /               (or /qd33/ depending on baseURL)
- Publications:  /publications/
- Research:      /research/
- Teaching:      /teaching/

When you are happy with how everything looks, stop the server with:

    Ctrl + C

--------------------------------------------------
3. How to regenerate docs/ for deployment
--------------------------------------------------

Make sure config.toml contains:

    publishDir = "docs"

Then from the repo root:

    cd qd33
    hugo --cleanDestinationDir

This will:

- Clean old files in docs/ that no longer correspond to any page.
- Rebuild the entire site into docs/.

You can verify:

    ls docs
    ls docs/teaching
    ls docs/research
    ls docs/css

You should see index.html in the relevant folders and updated CSS files.

--------------------------------------------------
4. How to update GitHub (deploy)
--------------------------------------------------

After rebuilding docs/, commit and push the changes:

    cd qd33
    git status          # should show modified files under docs/
    git add docs
    git commit -m "Update site"
    git push origin main

GitHub Pages will then serve whatever is currently inside docs/.

If you don’t see changes immediately on the live site, do a hard refresh
in your browser:

- Mac (Chrome): Cmd + Shift + R
- Or open the site in an Incognito / Private window.

--------------------------------------------------
5. Minimal cheat sheet
--------------------------------------------------

You can keep this tiny version handy:

    # Update qd33 website

    1. Edit source files:
       - content/_index.md
       - content/research/_index.md
       - content/teaching/_index.md
       - content/publication/*.md
       - layouts/publications/list.html
       - static/css/style.css
       - static/css/theme-override.css

    2. Preview locally:
       cd qd33
       hugo server --disableFastRender

    3. Rebuild docs:
       cd qd33
       hugo --cleanDestinationDir

    4. Commit and push:
       cd qd33
       git add docs
       git commit -m "Update site"
       git push origin main

    5. Check live:
       Visit https://dqianyu.github.io/qd33/
       Hard refresh if needed (Cmd+Shift+R).

End of file.
"""