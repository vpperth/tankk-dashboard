# Tankk Dashboard - Live Deploy Instructions

## Quick Deploy (GitHub Pages)

1. Create a GitHub repo: `tankk-dashboard`
2. Push contents of `/tmp/tankk-deploy/` to `main` branch
3. Enable GitHub Pages in Settings → deploy from `main`
4. Live URL: `https://<username>.github.io/tankk-dashboard`

## Alternative: Vercel (1-click)

1. Connect repo to Vercel
2. Deploy → instant live URL
3. Auto-updates on push

## Alternative: Simple HTTP server (temporary)
```
cd /tmp/tankk-deploy
python3 -m http.server 8765
# Open: http://localhost:8765
```

---

**Dashboard Features:**
- Network + Store-specific KPI views
- Staff portal (checklists, stock takes, adjustments)
- Manager compliance tracking
- Sales trend chart
- Real-time submission logging (via API endpoint `/api/submit`)

**Next Steps:**
- Wire backend storage (`/api/submit` → database)
- Add this week's sales data (Mar 30 - Apr 6)
- Test staff submissions with real staff
- Enable email alerts on missed compliance items
