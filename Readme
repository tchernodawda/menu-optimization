
# Menu Optimization using Graph Coloring

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![NetworkX](https://img.shields.io/badge/NetworkX-graph%20theory-1F77B4?style=flat-square)
![Matplotlib](https://img.shields.io/badge/Matplotlib-visualisation-11557C?style=flat-square)
![Jupyter](https://img.shields.io/badge/Jupyter-notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Applying graph coloring to find the minimum number of dishes required to satisfy all dietary requirements simultaneously, with no incompatible pairings.**

</div>

## Problem Statement

Hotels and high-traffic venues must accommodate a wide variety of dietary requirements: gluten-free, vegan, lactose-free, nut-free, egg-free, fish-free, red-meat-free, and more.

The central question: what is the minimum number of distinct dishes needed to cover all dietary regimes, given that some combinations are incompatible?

This is a direct application of the **graph coloring problem**, a classic NP-hard combinatorial optimisation problem where:

- Each **node** represents a dietary regime.
- Each **edge** connects two regimes that **cannot be served by the same dish** (incompatibility).
- The **minimum number of colours** needed to colour the graph = the **minimum number of dishes** required.

## Approach

### Modelling

8 dietary regimes are modelled as nodes in an undirected graph:

- Sans gluten
- Végétalien
- Sans lactose
- Sans fruits à coque
- Sans produits laitiers
- Sans œufs
- Sans poisson
- Sans viande rouge

Edges are added between regimes that are **mutually incompatible** (cannot be served by the same dish). Incompatible pairs are connected by an edge and therefore require different colours.

### Algorithm

`nx.greedy_color()` from NetworkX applies a **greedy graph coloring algorithm** that assigns colours to nodes such that no two adjacent nodes share the same colour.

```python
# Core of the solution
colors = nx.greedy_color(G)
num_dishes = max(colors.values()) + 1

print(f"Minimum number of dishes required: {num_dishes}")
```

Each colour represents one dish category that satisfies a group of compatible dietary regimes.

**Note:** The greedy coloring algorithm provides a valid coloring but does not guarantee the optimal minimum number of colours (chromatic number).

### Visualisation

The graph is rendered with Matplotlib at two stages:

1. **Before coloring**: plain graph showing dietary regime nodes and incompatibility edges.
2. **After coloring**: colour-coded graph where each colour group identifies regimes that can be covered by a single dish.

## Setup & Usage

**Prerequisites:** Python 3.x, Jupyter.

```bash
# Install dependencies
pip install networkx matplotlib jupyter

# Launch the notebook
jupyter notebook "notebooks/notebook menu_optimization_using_graphs.ipynb"
```

Run all cells in order; the notebook walks through problem modelling, graph construction, coloring, and result interpretation.

## Key Concepts Demonstrated

| Concept | Application |
|---|---|
| Graph modelling | Dietary regimes as nodes, incompatibilities as edges |
| Graph coloring problem | Minimum dish count = chromatic number |
| Greedy coloring algorithm | `nx.greedy_color()` — heuristic coloring algorithm |
| Combinatorial optimisation | Real-world resource minimisation problem |
| Graph visualisation | Matplotlib rendering of coloured compatibility graphs |

## License

See [LICENSE](LICENSE) for details.
