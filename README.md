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
