# California Wildfire Dashboard

Live link: https://ashwinjain99.github.io/Project-3/

## Project Proposal
Design an interactive JavaScript dashboard webpage containing an interactive leaflet map, time lapse visualization, and data table for the 2019 California Wildfires where the user can filter the data by month. Dashboard will be initialized with flask application that will store all data into a PostgreSQL database and create an API.

## Tools Used:
- Python
  - Pandas
- JavaScript
  - Leaflet
  - D3 Library
  - Plotly Library
- Flask
- HTML/CSS
- PostgreSQL
- Excel


## Data Used:
- [California Wildfire Incidents](https://www.kaggle.com/datasets/ananthu017/california-wildfire-incidents-20132020)
- This [website](https://www.convertcsv.com/csv-to-geojson.htm) is used to convert the csv files into GeoJSON.

## Extract, Transform, Load (ETL) Phase

### Part I - Data Extraction and Munging
- Utilized Pandas to clean the California Fire Incidents csv to filter for 2019 data and remove unwanted columns.
- Convert csv files into GeoJSON.
- Used Excel to prepare the Wildfires and Temps csv for import into PostgreSQL.

### Part II - PostgreSQL Database
- Created a wildfires_db with the following tables:
- Temps (primary key = county_id and month_number)
- Wildfires (primary key = fire_id)

## API and Interactive Dashboard Phase

### Part III - Flask App
- Utilized SQLAlchemy to connect app to our postgreSQL database tables.
- Provided 3 API routes for homepage, wildfire_names, wildfire_data.
- Wrote query to join Wildfires and Temps tables to build API route.
- Added "app.config['JSON_SORT_KEYS'] = False" to prevent JSON from alphabetically ordering the Jsonified data.

### Part IV - Interactive JavaScript
- Leaflet Interactive Map
- Leaflet Time Lapse Map
- Interactive JavaScript Table
- plotly charts
