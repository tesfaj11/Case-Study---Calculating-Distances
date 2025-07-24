# Case-Study---Calculating-Distances
# Case Study: Euclidean and Manhattan Distances

## Overview

This project explores and compares two common distance metrics used in data science and machine learning — **Euclidean distance** and **Manhattan distance**. The goal is to understand how these metrics differ when applied to the same dataset and to visualize their behaviors.

## Objectives

- Calculate all pairwise distances using both Euclidean and Manhattan metrics.
- Visualize the distribution of each distance type.
- Observe how distance varies from a central point (5, 5, 5) in the dataset.
- Explore how each distance metric represents space differently in 2D projections.

## Dataset

The dataset used (`distance_dataset.csv`) contains 3D points with columns: `X`, `Y`, and `Z`. These points are centered around (5, 5, 5) to allow for meaningful comparison of distances from this reference point.

## Key Steps

1. **Data Preparation**
   - Loaded the dataset and extracted only the coordinate columns (`X`, `Y`, `Z`).
   - Defined a reference point: (5, 5, 5) to calculate distance from.

2. **Distance Calculations**
   - Used `scipy.spatial.distance.pdist` to compute all pairwise distances between points using:
     - Euclidean Distance (straight-line)
     - Manhattan Distance (grid-like steps)

3. **Visualization**
   - Plotted histograms showing the distribution of Euclidean and Manhattan distances.
   - Colored scatter plots showing how distance from the center varies in 2D projections:
     - Y-Z plane for Euclidean
     - X-Z plane for Manhattan

## Results

- The Euclidean distance distribution is more compact, while the Manhattan distance shows a wider spread due to its additive nature.
- Visualizations confirmed that the shapes formed by equal distances are different:
  - Euclidean distances form circles.
  - Manhattan distances form diamonds/squares due to the stepped nature of the calculation.

## Conclusion

This case study clearly demonstrates the geometric differences between Euclidean and Manhattan distances. These visual and quantitative comparisons help clarify when one metric might be preferred over the other, depending on the structure and goals of the analysis.
