# Bir Group — Geo-Intelligence Explorer (Module 1)
**Retail Visit & Territory Coverage Intelligence System**

---

### 📌 System Overview
This is a standalone, ultra-high performance Geospatial Intelligence application designed for field sales, territory penetration, and retail coverage tracking without requiring sales/order data.

- **Total Retail Universe:** 32,671 geocoded outlets
- **Field Visits:** 89,679 audited visits
- **Active Field Reps:** 101 representatives
- **Coverage Reach:** 31.6% (10,324 visited outlets)
- **Zero-Visit Blindspots:** 68.4% (22,347 untapped outlets)

---

### 🎨 Visual & Map Architecture
1. **Micro Dot Color Coding (No Green Dots):**
   - 🟡 **Yellow Dots:** Visited Outlets (Visits > 0)
   - 🔴 **Red Dots:** Untapped Outlets (Visits = 0 / Blindspots)
2. **3D Visit Height:**
   - 3D bars rise in real-time proportional to the visit volume received by each outlet.
3. **Hierarchical Filtering:**
   - Bangladesh National -> 8 Divisions -> 64 Districts -> 490+ Thanas -> Unions / Wards.
   - Point-in-Polygon (PIP) boundaries ensure 100% of outlets are bounded inside their respective territorial polygon.

---

### 🚀 How to Run Locally
Open a terminal in this folder and start any local HTTP server:
`ash
python -m http.server 8080
`
Then visit:
http://localhost:8080/index.html

---

### 🔄 How to Reuse for Any Other Client in Future
To feed in data for another company:
1. Place their outlet/department CSV with id, 
ame, lat, long.
2. Place their field visit CSV with department_id, user_id, created_at.
3. Run the generator script to re-build ceo_national.js and ceo_outlets_D0.js - D7.js.
