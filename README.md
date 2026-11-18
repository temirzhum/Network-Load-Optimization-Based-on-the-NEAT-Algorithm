# Network Load Optimization Using NeuroEvolution of Augmenting Topologies (NEAT)

A simulation-based implementation of an adaptive load balancing algorithm for heterogeneous LTE/5G cellular networks using NeuroEvolution of Augmenting Topologies (NEAT).

The project explores the application of neuroevolution to dynamic network optimization by evolving neural network architectures, weights, and biases to optimize Cell Individual Offset (CIO) parameters and improve user distribution across base stations.

## Key Features

- **NEAT-based Optimization:** Evolves neural network topology, connection weights, and biases simultaneously using evolutionary mechanisms.
- **Heterogeneous Network Simulation:** Models LTE macro cells and 5G small cells with different coverage areas, transmission powers, bandwidths, and resource capacities.
- **Dynamic Load Balancing:** Adjusts CIO values to influence handover decisions and distribute users between overloaded and underutilized cells.
- **Radio Environment Modeling:** Implements RSRP, SINR, path loss, thermal noise, and signal propagation calculations.
- **User Mobility Simulation:** Simulates mobile users with varying positions, movement speeds, directions, and traffic demands.
- **Resource Allocation:** Models Physical Resource Block (PRB) distribution and evaluates user satisfaction based on allocated resources.
- **NEAT Improvements:** Implements connection pruning, population-wide elitism, weight blending during crossover, and probabilistic inheritance of genes from less-fit parents.
- **Algorithm Comparison:** Evaluates the proposed approach against Reinforcement Learning (Q-learning) and Automatic Weight Function (AWF) algorithms.

## Simulation Environment

The simulated network consists of:

- 7 LTE base stations
- 21 5G base stations
- 100 mobile users
- An 1800 × 1800 m simulation area
- User speeds ranging from 1 to 160 km/h
- Traffic demands ranging from 1 to 8 Mbps

Each simulation step represents 0.5 seconds and includes user movement, radio parameter calculations, handover decisions, resource allocation, and performance evaluation.

## Performance Evaluation

The proposed NEAT-based approach was compared with Reinforcement Learning and Automatic Weight Function methods under identical simulation conditions.

| Metric | NEAT | Reinforcement Learning | AWF |
|---|---:|---:|---:|
| Average traffic (Mbps) | 3.155 | 0.786 | 2.200 |
| User satisfaction | 0.695 | 0.132 | 0.412 |
| Disconnected users | 99.6 | 98.0 | 89.65 |
| Execution time (s) | 2.36 | 12.24 | 5.76 |
| Ping-pong handovers | 0 | 0 | 324.5 |

*Results obtained under random simulation conditions.*

The NEAT-based approach achieved higher traffic throughput and user satisfaction while requiring substantially less execution time than the two alternative implementations.

## Limitations and Future Work

The simulation uses a simplified radio propagation model based on free-space path loss and standard thermal noise. It does not account for physical obstacles, realistic base station deployment patterns, or structured user mobility.

An analysis of evolved neural network topologies also revealed that the resulting models relied predominantly on station type while making limited use of other input features. This suggests that the evolved solution may behave more like a simplified heuristic than a fully adaptive controller.

Future work could investigate more realistic radio environments, additional network configurations, and improved generalization across different deployment scenarios.

## Technologies and Concepts

- Python
- Neuroevolution
- Genetic Algorithms
- Neural Networks
- NEAT
- Reinforcement Learning
- LTE / 5G Networks
- Network Load Balancing
- Radio Resource Management
- Simulation and Performance Evaluation
