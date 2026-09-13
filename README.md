# 🌎 Shared Earth

**Shared Earth** is an educational web project designed to raise awareness about endangered species and help users learn about the animals with whom we share our planet.

The website combines an **interactive world map**, individual species information pages, and **population trend visualizations** to make information about endangered animals more accessible and engaging.

This project was created during one of our first hackathons as freshman developers and served as an opportunity to explore web development, interactive mapping, data visualization, and Python beyond our previous programming experience.

## Features

### 🗺️ Interactive Species Map

Explore endangered species around the world through an interactive map built with **Mapbox GL JS**.

Markers represent locations associated with different endangered species. Selecting a marker displays information about the species and provides a link to its dedicated information page.

### 🐾 Endangered Species Profiles

The website contains individual pages for several endangered species, including:

* African Forest Elephant
* Amur Leopard
* Bornean Orangutan
* Black Rhino
* Hawksbill Turtle
* Javan Rhino
* Mountain Gorilla
* Sunda Island Tiger
* Yangtze Finless Porpoise

Each page provides information and population-related data for the selected species.

### 📈 Population Trend Visualization

Python is used to analyze historical population data and generate population trend graphs.

The data-processing script uses:

* **SciPy** for linear regression
* **Matplotlib** for graph generation
* Historical population observations for each species

The generated visualizations provide another way to understand how endangered animal populations have changed over time.

## Tech Stack

### Frontend

* HTML5
* CSS3
* JavaScript
* Mapbox GL JS

### Data & Visualization

* Python
* Matplotlib
* SciPy

### Backend Experimentation

* Flask

## Project Structure

```text
quocgiahuydo.github.io/
│
├── graphs/                 # Generated population graphs
├── images/                 # Images and website assets
├── pages/                  # Individual endangered species pages
│
├── animal.html             # Species directory
├── globe.html              # Interactive Mapbox species map
├── info.html               # Main information/home page
├── main.py                 # Population analysis and graph generation
├── style.css               # Shared website styling
├── note.txt
└── README.md
```

## How It Works

### Interactive Map

`globe.html` uses **Mapbox GL JS** to display a world map containing geographic markers for endangered species.

Each location is represented as a GeoJSON feature containing:

* Species name
* Geographic coordinates
* Short description
* Link to the species information page

Clicking a marker opens a popup where users can learn more about that species.

### Population Analysis

`main.py` contains the Python logic used to process historical population data.

For each species, historical population observations are provided as a series of years and population values. The program applies linear regression using SciPy and generates a visualization of the resulting trend using Matplotlib.

Generated graphs are stored in:

```text
graphs/
```

## Running the Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/quocgiahuydo/quocgiahuydo.github.io.git
cd quocgiahuydo.github.io
```

### 2. Run the Website

Because most of the website is static HTML/CSS/JavaScript, you can run it using a simple local web server.

Using Python:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/info.html
```

### 3. Generate Population Graphs

Install the Python dependencies:

```bash
pip install matplotlib scipy flask
```

Then run:

```bash
python3 main.py
```

The script generates population graphs for the species defined in `main.py`.

## What We Learned

This project was an early opportunity for us to move beyond basic Python programming and explore several new technologies at once.

Some of the concepts we practiced included:

* Building multi-page websites with HTML and CSS
* Using JavaScript libraries in a web application
* Working with geographic coordinates and GeoJSON
* Integrating Mapbox into a website
* Visualizing data with Matplotlib
* Performing basic statistical analysis with SciPy
* Connecting data analysis with a user-facing website
* Learning new technologies quickly during a hackathon environment

One of the largest challenges was creating the interactive map while simultaneously learning unfamiliar web technologies. Completing a working website during our first hackathon was itself one of the biggest accomplishments of the project.

## Motivation

There are thousands of species facing threats from habitat loss, climate change, poaching, and other environmental pressures.

Shared Earth was created with a simple goal:

> Help people learn more about endangered animals and the species with whom we share the Earth.

By combining geographic exploration, species information, and population data, the project aims to make learning about endangered wildlife more interactive.

## Future Improvements

Possible improvements to the project include:

* Add additional endangered species
* Retrieve current conservation data from public APIs
* Improve mobile responsiveness
* Add filtering and searching by species or conservation status
* Replace static population datasets with dynamically retrieved data
* Improve population forecasting models
* Add conservation resources and organizations for each species
* Improve accessibility and UI/UX
* Refactor the JavaScript and Python components into a more structured application

## Authors

Created as a hackathon project by a team of freshman developers.

**Harry Do**
GitHub: [@quocgiahuydo](https://github.com/quocgiahuydo)

## Disclaimer

This project was created for educational and hackathon purposes. Population estimates and trend projections should not be interpreted as authoritative conservation forecasts. For current species population and conservation information, consult organizations such as the IUCN or WWF.

---

⭐ If you found this project interesting, feel free to explore the repository and learn more about the s
