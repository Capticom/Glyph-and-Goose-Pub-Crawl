# 🍺 GLYPH & GOOSE Pub Crawl Planner

Plan the ultimate London pub crawl spelling out "GLYPH & GOOSE"!

## 🌐 Live Demo

👉 **[Open Pub Crawl Planner](https://your-username.github.io/pub-crawl-planner)**

*(Replace `your-username` with your actual GitHub username)*

## 📖 How to Use

### 1. Get Your Pub Data

You need a GeoJSON file of London pubs. Here's how to get it:

1. Go to [Overpass Turbo](https://overpass-turbo.eu/)
2. Copy and paste this query:
```
[out:json][timeout:25];
(
  node["amenity"="pub"]["name"~"^(The )?(G|L|Y|P|H|O|S|E)",i]({{bbox}});
  way["amenity"="pub"]["name"~"^(The )?(G|L|Y|P|H|O|S|E)",i]({{bbox}});
  relation["amenity"="pub"]["name"~"^(The )?(G|L|Y|P|H|O|S|E)",i]({{bbox}});
);
out body;
>;
out skel qt;
```

3. Zoom/pan to central London (include areas like Soho, Covent Garden, Shoreditch)
4. Click **"Run"**
5. Click **"Export"** → **"GeoJSON"**
6. Save the file

### 2. Upload to the Planner

1. Open the [Pub Crawl Planner](https://your-username.github.io/pub-crawl-planner)
2. Click **"Upload GeoJSON File"**
3. Select your downloaded file
4. Wait for it to load (you'll see pub counts)

### 3. Choose Your Starting Point

**Option A: Pick a Starting Area**
- Choose from Soho, Covent Garden, Shoreditch, Camden, or South Bank
- Routes will start from that area and head towards Oval

**Option B: Pick a Specific Pub**
- Select any pub starting with "G" from the dropdown
- Get 10 different route variations from that exact pub

**Option C: Any Location**
- Let the planner find the best starting points automatically

### 4. Generate Routes

1. Click **"Generate Optimal Routes"**
2. Wait a few seconds (it's calculating optimal paths!)
3. View your top 10 routes

### 5. Use Your Route

For each route, you can:
- **📍 Open in Maps** - Opens Google Maps with turn-by-turn directions
- **💾 Download CSV** - Get a spreadsheet with all pub details

## 🎯 Features

- ✅ Spells out "GLYPH & GOOSE" with pub names
- ✅ Always ends near Oval station (easy journey home!)
- ✅ Smart routing that moves progressively towards Oval (no backtracking)
- ✅ Balanced distances between pubs
- ✅ Choose your starting location (area or specific pub)
- ✅ Export to Google Maps for navigation
- ✅ Download routes as CSV

## 🗺️ How It Works

1. **Finds the closest E pub to Oval** - This is always your final destination
2. **Works backwards** - Plans routes that progressively move towards that ending pub
3. **Smart pathfinding** - Balances between nearest pubs and making progress towards Oval
4. **No huge jumps** - Ensures the 9th→10th pub distance isn't excessive

## 📊 Sample GeoJSON

Want to try it out quickly? Download the sample London pubs data:
- [Download london-pubs.geojson](london-pubs.geojson) *(if you uploaded it)*

## 🛠️ Technical Details

- Built with React
- Uses Haversine formula for distance calculations
- Nearest-neighbor algorithm with directional weighting
- Client-side processing (your data never leaves your browser)

## 📝 Tips for Best Results

- **Include a wide area** when exporting from Overpass Turbo (Soho to Oval)
- **Check letter coverage** - Make sure you have enough of each letter (especially Y!)
- **Try different starting points** - Routes can vary significantly
- **Consider time** - Shorter routes aren't always better if pubs are far apart

## 🍻 Have Fun!

Remember to drink responsibly and pace yourself. That's 10 pubs! 🎉

---

Made with 🍺 and ❤️ for London pub crawlers
