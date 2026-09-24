# Prod Is Down

A 30-second browser FPS that ends with a referral link to Coralogix's Senior Software Engineer role (remote, Europe).
Single static file, no build step. Three.js r128 loads from cdnjs.

## Deploy to GitHub Pages

```bash
cd ~/work/prod-is-down
git init -b main && git add . && git commit -m "Prod Is Down"
gh repo create prod-is-down --public --source=. --push
gh api -X POST repos/{owner}/prod-is-down/pages -f 'source[branch]=main' -f 'source[path]=/'
```

The site goes live at `https://<your-github-username>.github.io/prod-is-down/` within about a minute.

## Local preview

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```
