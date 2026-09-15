# catalystech.solutions

Static site. No build step. Edit `index.html`, push, done.

## Publish on GitHub Pages (first time)
1. Create a new empty repo on GitHub named `catalystech-site` (public or private both work for Pages).
2. In this folder:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin git@github.com:YOUR_GITHUB_USER/catalystech-site.git
   git push -u origin main
   ```
3. GitHub repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`. Save.
4. Same page, "Custom domain": enter `catalystech.solutions` and save (the CNAME file here already matches). Tick "Enforce HTTPS" once it's available (can take up to an hour).

## DNS at your domain registrar
Add these records for `catalystech.solutions`:

| Type  | Name | Value                |
|-------|------|----------------------|
| A     | @    | 185.199.108.153      |
| A     | @    | 185.199.109.153      |
| A     | @    | 185.199.110.153      |
| A     | @    | 185.199.111.153      |
| CNAME | www  | YOUR_GITHUB_USER.github.io |

Remove any existing A/CNAME records pointing at Carrd first.

## Later edits
Change the file, then `git commit -am "update" && git push`. Live in about a minute.
