# 🍺 GLYPH & GOOSE Pub Crawl Planner

Plan the ultimate London pub crawl spelling out "GLYPH & GOOSE"!

## 🌐 Live Demo

👉 **[Open Pub Crawl Planner](https://capticom.github.io/Glyph-and-Goose-Pub-Crawl/)**

## 🚀 Quick Start

1. **[Open the Planner](https://capticom.github.io/Glyph-and-Goose-Pub-Crawl/)**
2. **Download the pub data**: [export.geojson](export.geojson)
3. **Upload it** to the planner
4. **Choose your starting point** (Soho, Covent Garden, or any specific pub)
5. **Click "Generate Optimal Routes"**
6. **Open in Google Maps** or download as CSV!

## 🎯 What It Does

Creates pub crawl routes that:
- ✅ Spell out "GLYPH & GOOSE" using pub names (e.g., **G**reyhound, **L**amb, **Y**e Olde...)
- ✅ Always end near **Oval station** (easy journey home!)
- ✅ Move progressively towards Oval (no backtracking)
- ✅ Have balanced distances between pubs
- ✅ Can start from your chosen area or specific pub

## 📖 How to Use

### Step 1: Upload Pub Data
- Click **"Upload GeoJSON File"**
- Select the `export.geojson` file from this repo
- Wait for pubs to load

### Step 2: Choose Starting Point

**Option A - Pick an Area:**
- Soho
- Covent Garden  
- Shoreditch
- Camden
- South Bank

**Option B - Pick a Specific Pub:**
- Choose any pub starting with "G" from the dropdown
- Get 10 different route variations from that pub

**Option C - Let It Decide:**
- Select "Any Location" to see the overall best routes

### Step 3: Generate & Navigate

1. Click **"Generate Optimal Routes"**
2. Browse the top 10 routes
3. For each route:
   - **📍 Open in Maps** - Get Google Maps directions
   - **💾 Download CSV** - Export pub details

## 🗺️ Route Logic

- **Always ends at the closest E pub to Oval** for easy journey home
- **Works progressively** - Each pub is closer to Oval than the last
- **No huge jumps** - Balanced distances (typically 0.3-0.8 km between pubs)
- **Smart scoring** - Balances nearest pub vs. progress towards destination

## 📊 Understanding the Results

Each route shows:
- **Total distance** in km and miles
- **Start → End pubs** clearly marked
- **Distance from previous pub** for each stop
- **Final distance to Oval** so you know your journey home

## 💡 Tips

- **Include more area** in your data for more route options
- **Check letter availability** - You need: G(2), L(1), Y(1), P(1), H(1), O(2), S(1), E(1)
- **Y is rare!** - Make sure your area includes pubs starting with Y
- **Try different starting points** - Routes vary significantly
- **10 pubs is a lot** - Consider splitting into two sessions! 🍻

## 🛠️ Technical Details

- Built with React + Tailwind CSS
- Client-side processing (data never leaves your browser)
- Uses Haversine formula for GPS distance calculations
- Nearest-neighbor algorithm with directional bias
- Hosted on GitHub Pages

## 🍻 Drink Responsibly

This is 10 pubs across several kilometers. Pace yourself, stay hydrated, and know your limits!

---

Made with 🍺 and ❤️ for London pub crawlers
