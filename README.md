# K-means Excel: Iris Clustering

K-means clustering on the classic Iris dataset implemented **entirely in Excel** (no code).  
The goal is to show a complete unsupervised learning workflow using only spreadsheet formulas.

---

## Dataset and workbook

- Dataset: Iris flowers (150 samples, 4 numeric features, 3 species).  
- Main file: [`data/iris-kmeans-excel.xlsx`](./data/iris-kmeans-excel.xlsx)  

Open the workbook to explore the data, formulas and results.

---

## K-means in Excel

The workbook implements K-means with \(K = 3\) clusters:

- Uses all four features (sepal length/width, petal length/width) in a 4D Euclidean distance.  
- Assigns each flower to the nearest centroid.  
- Recomputes centroids as cluster means until assignments stop changing (convergence in 2 iterations).

All calculations are visible as standard Excel formulas, making each step of the algorithm transparent.

---

## Results

**Final cluster sizes**

- Cluster K1: 51 flowers  
- Cluster K2: 64 flowers  
- Cluster K3: 35 flowers  
- Total: 150 flowers

**Species vs. clusters (confusion matrix)**

| Species         | Cluster 1 | Cluster 2 | Cluster 3 |
|-----------------|-----------|-----------|-----------|
| Iris-setosa     | 50        | 0         | 0         |
| Iris-versicolor | 1         | 49        | 0         |
| Iris-virginica  | 0         | 15        | 35        |

Setosa is perfectly separated; versicolor and virginica show the expected partial overlap for this dataset.

---

## How to use

1. Download or clone this repository.  
2. Open `data/iris-kmeans-excel.xlsx` in Excel or LibreOffice.  
3. Inspect the distance, cluster and centroid formulas.  
4. (Optional) Change the initial centroids and see how the final clustering changes.
