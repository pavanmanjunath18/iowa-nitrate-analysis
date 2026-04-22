# Data Sources

Two files are too large to store in this repository and must be downloaded manually before running the notebook.

---

## Files included in this repo

| File | Size | Source |
|------|------|--------|
| `raw/corn_oats_soyabeans.csv` | 512 KB | USDA NASS Quick Stats |
| `raw/groundwater_nitrate.csv` | 4.3 MB | EPA Water Quality Portal |

---

## Files you must download

### 1. `raw/water_nitrate.csv` (~133 MB)
Surface water nitrate measurements from the EPA Water Quality Portal.

**Download:**
1. Go to https://www.waterqualitydata.us/
2. Set filters:
   - **State:** Iowa
   - **Characteristic Name:** Nitrate
   - **Sample Media:** Water
   - **Date Range:** 01-01-2010 to 12-31-2017
3. Click **Download** → select CSV format
4. Rename the downloaded file to `water_nitrate.csv` and place it in `data/raw/`

### 2. `shapefiles/tl_2024_us_county.*` (~127 MB unzipped)
US Census TIGER/Line county boundaries shapefile (2024).

**Download:**
1. Go to https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html
2. Select **2024** → **Counties (and equivalent)**
3. Download the national shapefile zip
4. Unzip and place all files (`tl_2024_us_county.shp`, `.dbf`, `.prj`, `.shx`, `.cpg`) into `data/shapefiles/`

---

## Final expected structure

```
data/
├── raw/
│   ├── corn_oats_soyabeans.csv   ✓ included
│   ├── groundwater_nitrate.csv   ✓ included
│   └── water_nitrate.csv         ← download required
└── shapefiles/
    ├── tl_2024_us_county.shp     ← download required
    ├── tl_2024_us_county.dbf
    ├── tl_2024_us_county.prj
    ├── tl_2024_us_county.shx
    └── tl_2024_us_county.cpg
```
