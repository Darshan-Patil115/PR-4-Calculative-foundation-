# Calculative Foundation: Linear Algebra on Student Performance Data

A hands-on project that uses **Linear Algebra** to understand the exam scores of students in five subjects.
It covers vectors, matrices, geometry (line, plane, hyperplane) and eigenvalues / eigenvectors.

---

## Project Goal
A research institute shared the scores of students across several subjects. As a data analyst, the task is to:

1. Represent the data with **vectors and matrices**.
2. Use **norms, dot product, cross product and projection** on the data.
3. Understand **line, plane and hyperplane** in the data dimensions.
4. Use **eigenvalues and eigenvectors** to understand the variance in the data.

## Dataset
File: `data/student_scores.csv`

| Column | Meaning |
|---|---|
| Student_ID | Student name or ID (S01 to S30) |
| Maths, Physics, Chemistry, English, Computer | Score of the student in each subject (out of 100) |

- 30 students and 5 subjects, so the data matrix has size **30 x 5**.
- This is a **sample dataset** made for this project. You can replace it with your own CSV file if it has the same column names.

## Project Structure
```
calculative_foundation/
|-- README.md                      <- this file
|-- Calculative_Foundation.ipynb   <- main notebook (code, results, interpretations)
|-- Linear_Algebra_Theory.pdf      <- theory notes with definitions and formulas
|-- requirements.txt               <- Python libraries needed
|-- data/
|   `-- student_scores.csv         <- dataset
`-- images/                        <- charts saved by the notebook
    |-- norms_bar.png
    |-- cross_product_3d.png
    |-- vector_projection.png
    |-- line_plane_fit.png
    |-- linear_transformation.png
    |-- covariance_heatmap.png
    |-- scree_plot.png
    `-- pca_scatter.png
```

## What Is Covered

### Part A: Vector and Matrix Fundamentals
- Each student is a **5D vector**.
- **Norm-1** (total marks) and **Norm-2** (vector length).
- **Dot product** and the **angle** between two students.
- **Cross product** for 3 subjects (Maths, Physics, Chemistry).
- **Projection** of one student vector on another.

### Part B: Matrix Operations
- Students x subjects matrix (30 x 5).
- Matrix **addition** (bonus marks) and **multiplication** (weighted final score, Gram matrix).
- **Transpose**, **determinant** and **inverse** (only for square matrices).

### Part C: Linear Transformations and Geometry
- **Line** (2 subjects), **plane** (3 subjects) and **hyperplane** (5 subjects) fitted to the data.
- How dimensions grow from 2D to 3D to higher dimensions.
- A simple **linear transformation** applied to the data points.

### Part D: Eigenvalues and Decomposition
- **Covariance matrix** of the subjects.
- **Eigenvalues and eigenvectors** and a check that `C v = lambda v`.
- Variance explained by each eigenvector (scree plot).
- Dimensionality reduction from 5D to 2D (PCA).

## Key Results
| Topic | Result |
|---|---|
| Angle between S01 and S02 | 6.74 degrees (very similar score pattern) |
| Cross product of S01 and S02 (3 subjects) | [676, -848, 181], perpendicular to both vectors |
| Line fit | Physics = 0.918 x Maths + 1.238 |
| Eigenvalues of covariance matrix | 237.47, 45.63, 28.49, 21.81, 10.76 |
| Variance explained by PC1 | 69.0 % |
| Variance explained by PC1 + PC2 | 82.3 % |

**Main insight:** The first eigenvector has positive weights for all subjects. It shows *overall academic strength*:
a student who is good in one subject is usually good in the others. This one direction explains about 69 % of all variation in the scores.

## Sample Charts
| | |
|---|---|
| ![Projection](images/vector_projection.png) | ![Line and plane](images/line_plane_fit.png) |
| ![Covariance](images/covariance_heatmap.png) | ![Scree](images/scree_plot.png) |

## How to Run
1. Install Python 3.9 or newer.
2. Install the libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:
   ```bash
   jupyter notebook Calculative_Foundation.ipynb
   ```
4. Click **Run All**. The charts are saved in the `images/` folder.

> Run the notebook from the project folder so that the paths `data/` and `images/` work.

## Tools Used
- Python, NumPy, Pandas, Matplotlib
- Jupyter Notebook

## Theory Notes
Read `Linear_Algebra_Theory.pdf` for simple definitions, formulas and examples of every concept used in this project.

## Author
Add your name here.
