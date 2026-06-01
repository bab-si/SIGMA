# SIGMA Project

This repository brings together the code used for SIGMA: A Versatile Streaming Graph Partitioner for Vertex- and
Edge-Balanced Distributed GNN Training. 

## Repository Structure

- [SIGMA-Implementation](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/SIGMA-Implementation) contains the main SIGMA streaming graph partitioner in C++.
- [Partitioners](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/Partitioners) contains additional partitioning baselines used for comparison.
- [GraphTools](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/GraphTools) contains dataset download and format conversion scripts.
- [DistGNN](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/DistGNN) is the distributed GNN training stack used for edge-partition experiments.
- [DistDGL](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/DistDGL) is the distributed DGL-based training stack used for vertex-partition experiments.

## Typical Workflow

1. Prepare a dataset with the tools in [GraphTools](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/GraphTools).
2. Generate partitions with [SIGMA-Implementation](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/SIGMA-Implementation) or one of the baselines in [Partitioners](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/Partitioners).
3. Train and evaluate distributed GNN workloads with [DistGNN](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/DistGNN) or [DistDGL](/Users/bt309356/Forschung/GraphPartitioniererHeidelberg/SIGMA/DistDGL).

## Notes

- This is a multi-component research repository rather than a single buildable application.
- The subprojects have their own dependencies, build steps, and experiment scripts.
- The most important project-specific component is SIGMA itself; the training stacks and many baselines are included to support benchmarking and end-to-end evaluation.
