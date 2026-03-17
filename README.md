# EBMissions

This repository contains an R script that generates a directed graph of hiding spots for an Easter egg hunt (or scavenger hunt).

## Usage

Run the script using `Rscript`:

```bash
Rscript main.R [--data=path/to/input.csv] [--output=output_dir] [--seed=<number>]
```

- `--data`: Optional path to a CSV input file. If omitted, the script uses built-in example data.
- `--output`: Optional output directory (default: `output`).
- `--seed`: Optional random seed to make graph generation reproducible.

## Outputs

The script generates:

- `output/graph.dot` — Graphviz DOT representation of the directed graph
- `output/graph.svg` — SVG rendering of the graph (requires Graphviz `dot` executable)
- `output/clue_graph.csv` — A CSV table mapping each hiding spot to the clues it provides.
