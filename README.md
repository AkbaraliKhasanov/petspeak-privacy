# PetSpeak — Privacy &amp; Terms

GitHub Pages site for PetSpeak legal docs.

**Live URL:** `https://akbaralikhasanov.github.io/petspeak-privacy/`

## Files

- `index.html` — landing page
- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Service
- `support.html` — Support / FAQ
- `_style.css` — shared cream + sage theme styles

## Deploy

```bash
cd /Users/akbaralikhasanov/Public/AppStore/petspeak-privacy
git init && git add . && git commit -m "Initial site"
git branch -M main
gh repo create petspeak-privacy --public --source=. --remote=origin --push
gh api -X POST repos/AkbaraliKhasanov/petspeak-privacy/pages \
  --input - <<EOF
{"source": {"branch": "main", "path": "/"}}
EOF
```

Then in App Store Connect:

| Field | URL |
|-------|-----|
| Privacy Policy URL | `https://akbaralikhasanov.github.io/petspeak-privacy/privacy.html` |
| Support URL | `https://akbaralikhasanov.github.io/petspeak-privacy/support.html` |
| Marketing URL (optional) | `https://akbaralikhasanov.github.io/petspeak-privacy/` |
