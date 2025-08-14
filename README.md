# Delivery Route Optimization with EDA (Los Angeles TSP)

## Overview
This project demonstrates a practical solution to the **Traveling Salesman Problem (TSP)** using synthetic delivery data for Los Angeles. It applies the Nearest Neighbor heuristic followed by 2-opt optimization to minimize total travel distance, saving time, fuel, and emissions. The project includes an exploratory data analysis (EDA) stage and interactive mapping for route visualization.

## Key Features
- **Synthetic Data Generation**: Creates delivery stops around a central depot in Los Angeles.
- **Exploratory Data Analysis (EDA)**:
  - Maps delivery stops on an interactive Folium map.
  - Displays distance distribution between stops.
- **Route Optimization**:
  - Baseline route via Nearest Neighbor heuristic.
  - Route improvement using 2-opt algorithm.
- **Performance Metrics**:
  - Travel distance reduction.
  - Estimated time, fuel, and CO₂ savings.

## Results Summary
- **Number of stops (including depot)**: 12  
- **Nearest Neighbor distance**: 66.16 km (~2.21 h @ 30 km/h)  
- **Optimized (NN + 2-opt) distance**: 58.91 km (~1.96 h @ 30 km/h)  
- **Improvement over NN**: **10.96%** (7.25 km saved)  

**Estimated daily impact (per vehicle)**:
- Fuel saved: 0.60 L/day  
- Cost saved: $0.76/day  
- CO₂ reduction: 1.40 kg/day  

Assumptions: average speed = 30 km/h, fuel efficiency = 12 km/L, fuel price = $1.27/L, CO₂ = 2.31 kg/L.

## Installation
### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab

### Install dependencies
```bash
pip install pandas numpy folium matplotlib geopy
```

## Usage
1. Clone this repository or download the notebook file.
2. Open `TSP_with_EDA.ipynb` in Jupyter.
3. Run all cells to:
   - Generate synthetic delivery locations
   - Perform exploratory data analysis
   - Optimize the route
   - Visualize and save the results
4. View the interactive HTML map in the `out/` directory.


## Future Improvements
- Incorporate real-world traffic data via APIs (Google Maps, OpenStreetMap)
- Extend to Vehicle Routing Problem (VRP) with multiple vehicles
- Add delivery time windows and service durations
- Integrate with live tracking systems for dynamic re-optimization

## License
This project is provided for educational and portfolio purposes.  
You are free to use and modify it with attribution.
