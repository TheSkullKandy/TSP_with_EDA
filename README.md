# Delivery Route Optimizer – Traveling Salesman Problem (Los Angeles)

## Overview
This project demonstrates how to optimize delivery routes for a set of locations in Los Angeles using the Traveling Salesman Problem (TSP) framework.  
By minimizing total travel distance, the solution aims to reduce operational costs, improve delivery efficiency, and lower environmental impact.

The optimization is performed using:
- Haversine distance for geographic calculations
- Nearest Neighbor heuristic for initial route generation
- 2-opt local search for route refinement
- Interactive mapping using Folium

## Problem Statement
Last-mile delivery is one of the most resource-intensive parts of logistics.  
Given a central depot and multiple delivery locations:
1. Start at the depot
2. Visit each location exactly once
3. Return to the depot
4. Minimize the total travel distance

## Features
- Synthetic Data Generation: Creates delivery points within a specified radius of Los Angeles.
- Distance Calculation: Uses the Haversine formula to compute great-circle distances.
- Route Optimization: Nearest Neighbor + 2-opt improvement.
- Visualization:
  - Scatter map of delivery points
  - Histogram of pairwise distances
  - Interactive optimized route map (Folium)
- Impact Estimation:
  - Percentage distance improvement
  - Fuel, cost, and CO₂ savings estimation

## Project Structure
.
├── tsp_los_angeles_notebook.ipynb   # Main Jupyter notebook  
├── out/  
│   ├── tsp_map_LA.html              # Interactive route map output  
│   └── tsp_results_summary.csv      # Summary metrics (optional)  
└── README.md                        # Project documentation  

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
2. Open `tsp_los_angeles_notebook.ipynb` in Jupyter.
3. Run all cells to:
   - Generate synthetic delivery locations
   - Perform exploratory data analysis
   - Optimize the route
   - Visualize and save the results
4. View the interactive HTML map in the `out/` directory.

## Example Output
- Optimized Distance: ~XX km  
- Improvement over Nearest Neighbor: ~YY% shorter route  
- Estimated Fuel Savings: ~Z liters/day  
- Estimated CO₂ Reduction: ~W kg/day

## Future Improvements
- Incorporate real-world traffic data via APIs (Google Maps, OpenStreetMap)
- Extend to Vehicle Routing Problem (VRP) with multiple vehicles
- Add delivery time windows and service durations
- Integrate with live tracking systems for dynamic re-optimization

## License
This project is provided for educational and portfolio purposes.  
You are free to use and modify it with attribution.
