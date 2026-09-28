# Hollow Knight Route Search

This project uses a genetic algorithm to search for high-scoring routes through Hollow Knight. Fitness is based on Geo changes between areas and the route constraints.

The default run creates a new matrix without a fixed seed, so results can vary.

The default settings use tournament selection, order crossover, swap mutation, elitism, fitness sharing, and a two-opt improvement step. The dashboard shows the route and fitness over the generations.

## Run

Install the dependencies and start the program from the repository root:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python main.py
```

The run opens a route visualization and starts the dashboard at `http://127.0.0.1:8050`. Stop the dashboard with `Ctrl+C` in the terminal.

To use a saved Geo matrix, load it as a list of lists and pass it as `matrix_to_use` in `main.py`. The project also includes `Geo_Matrix_Dataset.csv`, grid-search results, and the final report.

## Files

- `ga/`, `operators/`, `pop/`, and `utils/` contain the genetic algorithm and route-scoring code.
- `visualizations/` contains the route plots and dashboard.
- `gridsearch.py` runs parameter searches; `tests/` contains a crossover test.
