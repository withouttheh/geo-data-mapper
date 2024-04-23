**GeoDataMapper: Integrating Google Places API for Location Visualization**

---

### Overview
GeoDataMapper is a project designed to utilize the Google Places API along with a database to clean up, manage, and visualize geographic location data on a Google Map. This README provides a comprehensive guide on setting up and executing the project, along with explanations of key components and instructions for user interaction.

### Features
- **Data Loading and Cleaning:**
  - Reads input data from a file (`where.data`).
  - Checks if the data is already present in the database (`geodata.sqlite`).
  - Calls the Google geocoding API to retrieve missing data and stores it in the database.

- **API Key and Rate Limiting:**
  - Explains the rate limitation of the Google Geocoding API and provides alternative sources for data retrieval without API keys.

- **Visualization:**
  - Visualizes the data on a Google Map using JavaScript.
  - Generates a JavaScript file (`where.js`) with location, latitude, and longitude information.

- **Execution:**
  - Runs `geoload.py` to load data into the database.
  - Runs `geodump.py` to generate JavaScript code for visualization.

- **User Interaction:**
  - Opens `where.html` in a browser to view the locations on the map.
  - Interacts with the map to explore the locations.

### Setup Instructions
1. **Clone the Repository:**
   ```
   git clone <repository_url>
   cd GeoDataMapper
   ```

2. **Install Dependencies:**
   - Ensure Python 3.x is installed on your system.
   - Install required Python packages:
     ```
     pip install -r requirements.txt
     ```

3. **Obtain Google API Key (Optional):**
   - If you have a Google API Key, follow the instructions [here](https://developers.google.com/maps/documentation/geocoding/intro) to obtain one.
   - If not, you can use a subset of data available [here](http://py4e-data.dr-chuck.net/geojson) by setting `api_key` to `False` in `geoload.py`.

4. **Run `geoload.py`:**
   - Execute the following command:
     ```
     python3 geoload.py
     ```
   - This script will load data into the database (`geodata.sqlite`).

5. **Run `geodump.py`:**
   - Execute the following command:
     ```
     python3 geodump.py
     ```
   - This script will generate JavaScript code for visualization.

6. **View Visualization:**
   - Open `where.html` in a web browser.
   - Explore the locations on the map.

### File Structure
- `geoload.py`: Script to load data into the database.
- `geodump.py`: Script to generate JavaScript code for visualization.
- `where.data`: Input data file containing geographic locations.
- `geodata.sqlite`: SQLite database for storing location data.
- `where.html`: HTML file for visualizing locations on a Google Map.
- `where.js`: JavaScript file generated for visualization.

### Notes
- Ensure UTF-8 support in the command line interface (CLI) by running `chcp 65001` in Windows.
- For detailed information on how the project works and its components, refer to the provided documentation within each script.

### Credits
- Developed by [Your Name]

### License
This project is licensed under the [MIT License](LICENSE).

---

Feel free to reach out if you have any questions, encounter issues, or want to contribute to the project!
