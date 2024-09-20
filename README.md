# Advanced Assignment: Monte Carlo Simulation for Race Performance

## Overview
This project is part of the **Advanced Assignment** for a training offered by the **University of Bristol**. The focus of this assignment is to implement a **Monte Carlo Simulation** to analyze race outcomes, specifically determining how often the 7th car wins in a simulated racing environment. The task simulates multiple car races with a probabilistic model to predict the likelihood of the 7th car winning under various race conditions.

### Purpose
The purpose of this project is to apply advanced statistical and simulation techniques (specifically Monte Carlo methods) to analyze real-world-like scenarios and gain insights into the likelihood of certain events (e.g., winning conditions) occurring under random variations.

---

## Project Structure

### Files
- **`Advanced_assignment.ipynb`**: Jupyter notebook containing the full implementation of the Monte Carlo Simulation. This notebook details the simulation setup, implementation, and results analysis.
- **`README.md`**: This file, providing an overview of the project.

---

## Monte Carlo Simulation: Detailed Description

The project simulates a **10,000-lap car race** between multiple cars. The simulation is designed to replicate real-world uncertainties like varying lap times, overtakes, and crashes. It counts how often the 7th car (starting from position 7) wins the race.

### Key Aspects of the Simulation:
1. **Lap Times**: Each car has a normally distributed lap time (`mean_lap_time` and `std_dev_lap_time` are parameters).
2. **Starting Time**: Each car starts at different times (`start_times`), affecting the overall race time.
3. **Penalties**: During the race, overtaking results in penalties, which are added to a car's total time.
4. **Crashes**: There's a probabilistic chance of a car crashing during overtaking. Crashed cars do not continue in the race.
5. **Race Outcome**: The race runs for multiple laps, and the car with the lowest total race time, out of those that are still in the race, is declared the winner.

### Simulation Breakdown:
- The race is repeated **10,000** times to gather sufficient statistical data.
- After each race, the model checks if the **7th car** won the race and records the result.

---

## Key Results

The simulation output gives the number of times the 7th car wins the race, providing insight into how starting position and race dynamics affect the likelihood of winning.

For example, after running the simulation, the result was:

This result suggests that the 7th car won 20 out of 10,000 races under the specific conditions modeled in this simulation.

---

## How to Run the Simulation

### Requirements:
- Python 3.x
- Jupyter Notebook
- Required Libraries:
  - `numpy`
  - `matplotlib`

### Instructions:
1. Clone this repository.
2. Open the **`Advanced_assignment.ipynb`** file in Jupyter Notebook.
3. Run all cells in the notebook to execute the Monte Carlo Simulation.
4. The final output will display the number of times the 7th car wins the race.

---

## Acknowledgements
This project is part of a training program offered by the **University of Bristol**. Special thanks to the instructors and course facilitators for providing the guidance and resources needed for this advanced simulation assignment.
