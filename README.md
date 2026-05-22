# PostGIS to REST API to GIS Clients
## Overview
This laboratory implements a complete geospatial data pipeline by integrating a spatial database (PostGIS), a web service layer (Flask REST API), and GIS clients (QGIS).

Unlike previous exercises where spatial data was created directly in Python, this lab retrieves real-world spatial data from a PostGIS database and serves it through REST API endpoints in GeoJSON format.

The workflow is:

PostGIS Database → Flask REST API → GeoJSON → QGIS Client

This architecture demonstrates how spatial data can be distributed, accessed, and visualized dynamically without manual file exports.

## Environment Setup
- Python 3.x 
- `PostgreSQL` with `PostGIS` 
- `Flask`, `flask-cors`, `psycopg2-binary`, and `python-dotenv`   
- QGIS  

---
## How to Run

1. Activate the virtual environment  
2. Navigate to the backend folder
3. Test database connection
4. Run the Flask server
5. Open in browser

---

## Reflection
PostGIS plays the role of the core spatial database in this architecture, serving as the authoritative source of geographic data by storing, managing, and processing spatial features such as parcels and roads using specialized geometry types and spatial functions. Flask, on the other hand, acts as the backend service layer that connects to the PostGIS database, executes SQL queries, and exposes the retrieved spatial data through REST API endpoints that can be accessed over HTTP. GeoJSON is useful for spatial web services because it provides a lightweight, standardized, and web-friendly format for encoding geographic data, making it easy to transmit, visualize, and integrate across different systems and platforms.

The function `ST_AsGeoJSON()` supports distributed GIS by converting spatial geometries stored in PostGIS into GeoJSON format, allowing the data to be shared and consumed by remote applications such as QGIS and web-based clients. QGIS is considered a heavy client because it performs advanced spatial analysis, rendering, and data processing locally while still being capable of consuming data from remote services. A REST API is better than manually exporting shapefiles because it enables real-time access to up-to-date spatial data, eliminates repetitive manual processes, and ensures consistency across users and applications.

This laboratory demonstrates distributed geospatial computing by separating the system into different components `database`, `server`, and `client` that communicate over a network, rather than relying on a single local environment. Service-based GIS architecture provides advantages such as centralized data management, real-time data sharing, interoperability between systems, and easier integration with various clients. Finally, this architecture supports scalability in spatial systems because each component `database`, `API server`, and `client` can be scaled independently to handle increasing data volume, user demand, and system complexity efficiently.