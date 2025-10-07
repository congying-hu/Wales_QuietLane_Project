
# 🚲 Quiet Lane Identification – Rural NCN On-road Sections

### Overview
This project identifies **rural NCN on-road sections** that are suitable for **Quiet Lane interventions**, following approximately **90%** of the *Wales Quiet Lane Guidance* methodology.  
It combines **Ordnance Survey road classifications** and **Agilysis traffic data** (AADT and speed) with **Urban–Rural classification polygons** to extract and visualize candidate sections.

---

### Methodology
| Step | Description | Data Source |
|------|--------------|--------------|
| 1 | Select rural areas (`Accessible Rural` and `Remote Rural`) | Urban–Rural Classification |
| 2 | Clip NCN/Agilysis roads within rural areas | Agilysis Roads + Rural Polygons |
| 3 | Keep only road types: `Classified Unnumbered`, `Unclassified`, `Unknown`, `Not Classified` | Ordnance Survey |
| 4 | Filter out high-traffic segments (`Modelled AADT` > 1000) | Agilysis |
| 5 | Save results to GeoPackage and visualize | GeoPandas / Folium |

> ⚠️ *Van percentage data are currently unavailable, so the script achieves ~90% compliance with the Wales Quiet Lane Guidance.*

---
