# Dijkstra's Algorithm Implementation

## Overview

This repository contains an implementation of Dijkstra's algorithm in Python, designed to find the shortest paths from a starting node to all other nodes in a weighted graph. The graph is represented as an adjacency list, where each key is a node, and its value is a dictionary of neighboring nodes and their corresponding edge weights.

## How It Works

Dijkstra's algorithm is a well-known shortest path algorithm used in graph theory. The main idea is to continuously select the node with the smallest known distance, update its neighbors with the computed distances, and iterate until all nodes have been processed. This implementation uses a priority queue to efficiently select the next node with the smallest distance.

## Graph Representation

The graph is represented as a Python dictionary. Each key represents a node, and its value is another dictionary that contains its neighbors and the weights of the edges connecting to those neighbors. Here's a brief description of the provided graph:

- Node 'A' is connected to 'B' (weight 20), 'D' (weight 80), and 'G' (weight 90).
- Node 'B' is connected to 'F' (weight 10).
- Node 'C' is connected to 'F' (weight 50), 'H' (weight 20), and 'D' (weight 10).
- Node 'D' is connected to 'G' (weight 20) and 'C' (weight 10).
- Node 'E' is connected to 'B' (weight 50) and 'G' (weight 30).
- Node 'F' is connected to 'C' (weight 10) and 'D' (weight 40).
- Node 'G' is connected to 'A' (weight 20).
- Node 'H' has no outgoing edges.

## Algorithm Steps

1. **Initialization**: Set the distance to the start node to 0 and all other nodes to infinity. Use a priority queue to manage the nodes to be processed, initially containing only the start node.
2. **Processing Nodes**: Continuously extract the node with the smallest known distance from the priority queue.
3. **Updating Distances**: For the current node, calculate the distance to each neighbor. If the calculated distance is less than the known distance, update the distance and record the path.
4. **Repeat**: Continue the process until the priority queue is empty.
5. **Result**: The algorithm outputs the shortest distances from the start node to all other nodes and the paths taken to achieve these distances.

## Output

The program prints the shortest paths from the start node to all other nodes along with their distances. If a node is not reachable from the start node, it indicates that the node is not reachable.

