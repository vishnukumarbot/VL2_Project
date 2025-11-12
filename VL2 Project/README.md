# VL2 Load Balancing Performance Visualizer

## Project Overview

This project simulates and visualizes the VL2 (Virtual Layer 2) data center network architecture proposed by Microsoft Research in their SIGCOMM 2009 paper.
The focus is on demonstrating how Valiant Load Balancing (VLB) achieves uniform link utilization, fairness, and high throughput compared to deterministic (shortest-path) routing.

It is implemented entirely in Python using graph-based topology modeling and basic traffic simulation.

## Key Features
Builds a multi-layer VL2-style network topology (Servers → ToR → Aggregation → Core).

Implements two routing methods:
• Deterministic (shortest-path)
• Valiant Load Balancing (random intermediate routing)

Generates random flows (mice and elephant traffic).

# Calculates
Link utilization
Maximum congestion
Jain’s fairness index
Flow completion statistics
Provides clear visualizations of load distribution across links.

# Background

VL2 is a server-to-server scalable network design that separates addressing from location and uses Clos topology built from commodity switches.
The key innovation — Valiant Load Balancing (VLB) — routes each flow through a randomly selected intermediate switch, ensuring balanced utilization and resilience to traffic hotspots.

# Technologies Used
| Component | Tool/Library |
|------------|--------------|
| **Language** | Python 3.x |
| **Network Topology** | NetworkX |
| **Data Handling** | NumPy |
| **Visualization** | Matplotlib |
| **Notebook** | VS Code (.ipynb) |


# Metrics Measured
Metric	                    Description
Average Link Load	        Mean number of flows per link
Max Link Load	            Peak utilization (identifies hotspots)
Fairness (Jain’s Index) 	Measures load distribution balance
Flow Completion Time (FCT)	Flow duration under varying traffic patterns

# Expected Results
Deterministic routing: uneven link utilization and possible congestion hotspots.

Valiant Load Balancing: smoother utilization curve, higher fairness, and stable performance even under random traffic.


# How to Run
Open the notebook:
Run all cells to generate:
•VL2 topology graph
•Load distribution comparison
•Visualization plots

# Output Visuals
Graph 1: Determinstic link utilization
Graph 2:  VLB link utilization
(Figures generated dynamically by Matplotlib in the notebook.)

# References
A. Greenberg, J. R. Hamilton, N. Jain, S. Kandula, et al.
“VL2: A Scalable and Flexible Data Center Network,”

SIGCOMM, 2009.
