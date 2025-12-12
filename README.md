# Diamond Aircraft Authorized Centers Content Pack for ForeFlight

This repository provides **source code** to generate KML files and a **ForeFlight content pack** featuring detailed maps, waypoints, and information for Diamond Aircraft's authorized service centers, distributors, and training centers worldwide. These waypoints and overlays help pilots quickly locate official Diamond support locations for maintenance, sales, and training, enhancing situational awareness during flight planning.

The content pack displays centers as custom map layers in ForeFlight, categorized by type (Service Centers, Distributors/Sales Partners, Training Centers), and integrates seamlessly with terrain, hazard advisor, profile view, and sectional charts for better route planning.

## Content Overview

This content pack includes waypoints for all official Diamond Aircraft locations, sourced directly from Diamond's map data API. It generates separate KML files for each category and a unified ForeFlight content pack for easy import.

**Current version: 2025.12.12**  
**Number of locations: Approximately 192 (varies based on Diamond's updates)**

Locations are grouped into categories:
- **Sales / Distributors** (Green target icons)
- **Service Centers** (Blue airport icons)
- **Training / Flight Schools** (Red school icons)

The Python script automates fetching and parsing data from Diamond's endpoint, ensuring the content stays up-to-date with minimal effort. Generated KML files can be viewed in Google Earth or imported into ForeFlight.

## Inspiration and Credits

This content pack is inspired by and builds upon community efforts to make Diamond Aircraft location data more accessible:

- **[Diamond Aircraft](https://www.diamondaircraft.com/en/service-and-support/service-center-locations/)** – Primary source for all authorized center data, fetched via their public map API. All location information is credited to Diamond Aircraft Industries.
- **[Diamond Aviators Forum Thread](https://www.diamondaviators.net/forum/viewtopic.php?p=103010&hilit=kml#p103010)** – Special thanks to Marlon for the original exhaustive work in compiling and sharing KML data for Diamond centers. This repository automates Marlon's foundational efforts to keep the data current and converts it into a distributable ForeFlight content pack.
- **[Premier Aircraft Sales (Fort Lauderdale)](https://www.premieraircraftsales.com)** – Grateful acknowledgment for their assistance with instruction, purchasing, and maintenance of my Diamond DA40NG.
- **[MyFlight (Patrick Abel)](https://myflight.com)** – Thanks to Patrick Abel for expert guidance on Diamond aircraft ownership, training, and upkeep.

This automation script was developed to simplify updates and distribution, ensuring pilots have the latest information without manual recreation.

## Included Locations

The pack includes worldwide Diamond Aircraft authorized locations, categorized and with detailed info windows. Here's a summary of categories (full list generated dynamically via script):

| Category                  | Icon Style | Example Locations | Notes |
|---------------------------|------------|-------------------|-------|
| Sales / Distributors     | Green Target | Premier Aircraft Sales (USA), Aeropole Denmark (Denmark) | Handles sales and partnerships; often includes demo flights and purchasing support. |
| Service Centers          | Blue Airport | Diamond Aircraft Industries (Austria), Various global ASCs | Authorized maintenance and repairs; certified for DA20, DA40, DA42, DA62 models. |
| Training / Flight Schools| Red School  | Flight schools affiliated with Diamond | Simulator and flight training centers for type ratings and recurrent training. |

*Fly safe: Always verify center details directly with Diamond or the location before planning visits. Data is fetched from official sources but may change.*

## How to Generate and Use

1. **Download Pre-Generated Files:**
   - Check the [DiamondCenters.zip](https://github.com/ingramleedy/Diamond-Aircraft-Service-Centers/blob/main/DiamondCenters.zip?raw=true) section for ready-to-use ForeFlight content pack.

2. **Import into ForeFlight:**
   - Transfer files to your iPad/iPhone via AirDrop, email, or cloud storage.
   - In ForeFlight: More > Custom Content > Add > Select the pack.
   - Enable the layer in Maps > Layers.

## How to Generate new KML files
1. **Run the Script:**
   - Clone this repository.
   - Install dependencies: `pip install requests beautifulsoup4`.
   - Run `python generate_kml.py` (or similar script name) to fetch data and create KML files.
   - For ForeFlight pack: Use tools like [ForeFlight Content Pack Creator](https://foreflight.com/support/custom-content) to bundle KMLs`.

## Contributing

Contributions welcome! If you spot outdated data or have enhancements (e.g., better icons, additional filters), submit a pull request. Ensure any changes respect Diamond's data usage terms.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. All Diamond Aircraft data remains property of Diamond Aircraft Industries.
