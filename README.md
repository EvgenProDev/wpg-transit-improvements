# Winnipeg Transit and Parking Analysis Datathon Project

A comprehensive web application for analyzing Winnipeg's transit data and parking violations using machine learning clustering algorithms and interactive visualizations.

## 🚀 Overview

This project analyzes Winnipeg's public transit system and parking violations data to identify patterns, clusters, and insights that can help improve urban planning and transportation efficiency. The application combines multiple datasets to create interactive maps showing high-demand bus stops, parking violation hotspots, and areas where buses frequently pass up passengers.

## 🛠️ Technologies Used

### Backend
- **Django 5.1** - Python web framework for the backend API and server
- **Python 3.x** - Core programming language
- **SQLite** - Lightweight database for data storage
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **scikit-learn** - Machine learning library (DBSCAN clustering)

### Frontend
- **HTML5/CSS3** - Web markup and styling
- **Bootstrap 5.2.2** - CSS framework for responsive design
- **JavaScript (ES6+)** - Client-side interactivity
- **Three.js** - 3D graphics library for interactive visualizations
- **Leaflet** - Interactive maps library
- **Folium** - Python library for creating interactive maps

### Data Visualization
- **Folium** - Interactive map generation
- **HeatMap** - Geographic heatmap visualization
- **MarkerCluster** - Clustered map markers
- **DBSCAN** - Density-based clustering algorithm

### Development Tools
- **Django Management Commands** - Project administration
- **CSV Processing** - Data cleaning and transformation
- **Regex** - Pattern matching for data extraction

## 📊 Features

### Data Analysis
- **Transit Demand Analysis** - Identifies high-demand bus stops
- **Parking Violation Mapping** - Visualizes parking violation hotspots
- **Passenger Pass-up Analysis** - Tracks locations where buses are too full
- **Geographic Clustering** - Uses DBSCAN algorithm to find spatial patterns

### Interactive Visualizations
- **Interactive Maps** - Clickable markers with detailed information
- **Heat Maps** - Visual representation of data density
- **Cluster Analysis** - Groups related data points geographically
- **3D Visualizations** - Three.js powered interactive elements

### Data Processing
- **CSV Data Cleaning** - Automated data preprocessing
- **Coordinate Extraction** - Parses location data from various formats
- **Date Filtering** - Filters data by time periods (2019 onwards)
- **Weekday Analysis** - Focuses on weekday transit patterns

## 📁 Project Structure

```
Datathon/
├── manage.py                 # Django management script
├── daily_passenger.csv       # Transit passenger data
├── Datathon/                 # Django project settings
│   ├── __init__.py
│   ├── settings.py          # Django configuration
│   ├── urls.py              # Main URL routing
│   ├── wsgi.py              # WSGI configuration
│   └── asgi.py              # ASGI configuration
├── Website/                  # Main Django app
│   ├── views.py             # View functions
│   ├── urls.py              # App URL routing
│   ├── clusters.py          # Clustering analysis
│   ├── filter.py            # Data filtering utilities
│   ├── visualize_heatmap.py # Heatmap generation
│   ├── parking_violations.csv
│   ├── bus_demand_clusters.html
│   ├── static/
│   │   └── js/
│   │       └── exoplanets.js # 3D visualization script
│   └── templates/
│       └── website/
│           ├── base.html     # Base template
│           └── home.html     # Home page template
└── utility/
    └── weekday_transit_filters.py # Data filtering utilities
```

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher
- pip (Python package installer)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Datathon-main
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required packages**
   ```bash
   pip install django==5.1
   pip install pandas
   pip install numpy
   pip install scikit-learn
   pip install folium
   ```

4. **Run database migrations**
   ```bash
   python manage.py migrate
   ```

5. **Start the development server**
   ```bash
   python manage.py runserver
   ```

6. **Access the application**
   Open your browser and navigate to `http://127.0.0.1:8000/`

## 📈 Data Sources

The project analyzes several datasets:

- **Daily Passenger Activity** - Transit ridership data with location coordinates
- **Parking Violations** - Parking infraction data with geographic information
- **Bus Stops** - Location data for transit stops
- **Pass-ups** - Data on when buses pass up passengers due to capacity

## 🔍 Key Analysis Features

### Clustering Analysis
- Uses DBSCAN (Density-Based Spatial Clustering) algorithm
- Identifies geographic clusters of high-demand areas
- Configurable distance parameters (500m default)

### Interactive Mapping
- Real-time map generation with Folium
- Clickable markers with detailed information
- Responsive design for mobile and desktop

### Data Visualization
- Heat maps for parking violations
- Cluster visualization for transit demand
- Statistical summaries and analysis results

## 🛠️ Customization

### Modifying Clustering Parameters
Edit the clustering parameters in `views.py` or `clusters.py`:
```python
eps_meters = 500  # Distance threshold for clustering
min_samples = 3   # Minimum points required for a cluster
```

### Adding New Data Sources
1. Add CSV files to the project directory
2. Update the data loading code in `views.py`
3. Modify the clustering logic as needed

### Styling and UI
- Modify templates in `Website/templates/website/`
- Update CSS in the base template
- Customize Bootstrap components

## 📊 Sample Output

The application generates:
- Interactive maps with cluster markers
- Statistical tables showing cluster information
- Heat maps of parking violations
- Analysis summaries and insights

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is part of a datathon competition. Please check with the organizers for specific licensing terms.

## 🆘 Support

For questions or issues:
1. Check the Django documentation for framework-specific questions
2. Review the scikit-learn documentation for clustering algorithms
3. Consult the Folium documentation for mapping features

## 🔮 Future Enhancements

- Real-time data integration
- Advanced machine learning models
- Mobile app development
- API endpoints for external access
- Enhanced data filtering options
- Performance optimization for large datasets
