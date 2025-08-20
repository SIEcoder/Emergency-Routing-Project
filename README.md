# Emergency Routing Project

## Overview
The **Emergency Routing Project** focuses on optimizing medical emergency response in **Obio-Akpor, Rivers State**.  
The goal is to identify the **closest hospital** for any emergency, taking into account:
- Distance  
- Travel time  
- Hospital capacity  
- Service rating  

---

## Tools and Libraries
- **Python**: main programming environment  
- **Pandas / NumPy**: data handling and computation  
- **GeoPandas / Shapely / Fiona**: geospatial manipulation  
- **OSMNx / NetworkX**: road networks, graph modeling, shortest paths  
- **SciPy**: optimization routines 
- **Kepler.gl / Matplotlib / Plotly**: geospatial visualization  
- **Google Colab**: coding & collaboration  
- **Git / GitHub**: version control  

---

## Data Notes
- **Hospitals dataset** manually collected into CSV: Name, coordinates, service rating.  
  - Reason: OpenStreetMaps does not have a lot of hospitals plotted onto its maps.  
- **Road network** extracted via OSMNx for Obio-Akpor polygon.  
- Data integrity maintained: no missing values, clean and ready for modeling.  

---

## Project Phases

### Phase 1  Completed
- Extract Obio-Akpor boundaries.  
- Load hospital CSV and road network.  
- Convert road network to GeoDataFrame.  
- Prepare graph base for routing.  
- Integrate hospitals with the road network graph.  
- Hospitals plotted on map with lon/lat.  

### Phase 2  In Progress
- Emergency Route Optimization.  
- Compute one-to-many shortest paths using **Dijkstra’s algorithm**.  
- Compute route metrics: distance, travel time (road-type speeds), hospital capacity, service rating.  
- Visualization: highlight closest hospital, color-code alternatives.  

### Phase 3  Planned
- Simulation of emergency scenarios.  
- Interactive dashboards (Tableau).  
- Documentation and reporting of results.  

---

## Special Considerations
- Travel time calculated using average speeds by road type:  
  - Highway → 80 km/h  
  - Primary → 60 km/h  
  - Minor → 40 km/h  
- Multi-criteria cost function considers **distance, travel time, hospital capacity, and rating**.  
- Workflow maintained in **Google Colab**.  
- GitHub used for version snapshots (token-based authentication).  

---

## Collaboration & Version Control
- Shared Google Drive folder for Colab notebooks & resources.  
- **Folder structure**:  
/Project Code, Resources and Implementation/
  - Route_Optimization_Project.ipynb (primary code-space)
  - Resources, containing (hospital CSV and other static data)
  - Scripts, containing python files
- GitHub repository used for storing snapshots, while live coding collaboration happens in Colab.  

---

## Current Status
-  Phase 1 complete: hospitals integrated.  
-  Starting Phase 2: route optimization using Dijkstra’s algorithm.  

