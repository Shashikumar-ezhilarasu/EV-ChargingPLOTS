 EV Charging Stations Mappings
<img width="1470" alt="Screenshot 2024-08-03 at 4 37 55 PM" src="https://github.com/user-attachments/assets/b640e096-3d87-4cd4-a86d-93c3d9af8c40">


---

# EV Charging Stations Mapping

This project visualizes Electric Vehicle (EV) charging stations on an interactive map using Python and Folium. The data is sourced from a CSV file containing information about each charging station, such as its name, address, latitude, longitude, and other relevant details. By hovering over each marker on the map, users can view specific details about the charging station.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Example Output](#example-output)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

With the rise in popularity of electric vehicles, the availability of charging stations has become crucial. This project aims to provide a visual representation of EV charging station locations to help EV users find convenient charging points.

Using a dataset of charging stations, the project plots these locations on an interactive map, providing users with detailed information about each station when they hover over the map markers.

## Features

- **Interactive Map:** Displays all EV charging stations on a map.
- **Hover Information:** Detailed information is displayed when hovering over each charging station marker.
- **Customizable Map:** Change the map style, marker icons, and other settings.
- **Easy Integration:** Import new datasets easily and update the map with new locations.

## Dataset

The dataset is stored in a CSV file containing the following columns:

- `Station Name`: Name of the EV charging station
- `Address`: Address of the charging station
- `Latitude`: Latitude of the charging station location
- `Longitude`: Longitude of the charging station location
- `Other Details`: Additional information (e.g., charging speed, available ports)

**Example CSV File:**

| Station Name     | Address                 | Latitude | Longitude | Other Details          |
|------------------|-------------------------|----------|-----------|------------------------|
| Station A        | 123 Main St, City A     | 40.7128  | -74.0060  | 50 kW, 2 ports         |
| Station B        | 456 Elm St, City B      | 34.0522  | -118.2437 | 150 kW, 4 ports        |
| ...              | ...                     | ...      | ...       | ...                    |

## Installation

To run this project, you'll need to have Python installed along with the necessary libraries. Follow these steps to set up your environment:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/EV_Charging_Stations_Mapping.git
   cd EV_Charging_Stations_Mapping
   ```

2. **Install Required Libraries**

   Install the required Python libraries using pip:

   ```bash
   pip install folium pandas
   ```

## Usage

1. **Prepare Your Dataset**

   Ensure your dataset is in a CSV file format with the columns mentioned above. Update the file path in the script to point to your CSV file.

2. **Run the Script**

   Use the following command to run the script and generate the map:

   ```bash
   python map_charging_stations.py
   ```

3. **View the Map**

   The script will generate an HTML file containing the map. Open this file in your web browser to explore the EV charging stations.

   ```bash
   open my_map.html
   ```

## Example Output

Here's an example of what the map will look like:

![Example Map]<img width="918" alt="image" src="https://github.com/user-attachments/assets/bf90caaa-75dc-4657-9b82-29e65d185997">


Each marker on the map represents a charging station. Hover over a marker to see details about the station, such as its name, address, and charging capabilities.

## Script Explanation

Here's a brief explanation of the Python script used to generate the map:

```python
import folium 
from folium.plugins import FastMarkerCluster
map = folium.Map(location =[41.5025,-72.69997], zoom_start=9)
latitudes = [a['latitude'] for a in records]
longitudes = [a['longitude']for a in records]
for record in records:
    coords =(record['latitude'], record['longitude'])
    folium.Marker(coords, popup=record['Station Name']).add_to(map)

FastMarkerCluster(data=list(zip(latitudes, longitudes))).add_to(map)
map
```

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push your branch to your fork.
5. Create a pull request.

Please ensure your code follows the project's coding guidelines and includes appropriate documentation and tests.



## Contact

For any questions or suggestions, feel free to reach out to me at shashikumar-ezhilarasu@gmail.com.

---



