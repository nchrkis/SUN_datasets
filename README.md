
# SUN Datasets: Mickey Mouse & Particles

This repository contains two 2D datasets used in the paper:

**Christakis, N., & Drikakis, D. (2025).  
_SUN: Stochastic UNsupervised learning for data noise and uncertainty reduction._  
Applied Sciences (MDPI).**  


Both datasets were created to evaluate the **SUN algorithm**, an unsupervised clustering framework combining the RUN-ICON method with Gaussian Mixture Models (GMM) to reduce data noise and uncertainty.

---

## 📘 1. Mickey Mouse Dataset

### Description
The **Mickey Mouse dataset** consists of **7,500 points** in 2D space (`x`, `y`).  
It represents a stylized **Mickey Mouse head**, with:
- One large circular cluster (the “face”)
- Two smaller circular clusters (the “ears”), symmetrically attached to the main circle

This dataset tests the algorithm’s ability to identify **distinct geometric shapes** and separate overlapping clusters.

### Columns

| Column | Description |
|:-------|:-------------|
| `x` | x-coordinate of a point in the 2D plane |
| `y` | y-coordinate of a point in the 2D plane |

### Structure
- **Total points:** 6,648 
- **True clusters:** 3  
- **Expected cluster names:** `ear_left`, `ear_right`, `face`

### Example Usage
This dataset is suitable for:
- Demonstrating clustering performance on structured shapes  
- Comparing deterministic (K-means) vs. probabilistic (GMM, SUN) clustering  
- Visualization and educational purposes  



## 💨 2. Particles Dataset

### Description
The **Particles dataset** consists of **146,400 two-dimensional points** derived from **computational fluid dynamics (CFD)** simulations of a **coughing event in an enclosed room**.  
It models the **lateral dispersion of airborne particles** at **0.12 seconds** after emission, under **turbulent flow conditions**.

Each data point represents a single particle, defined by its **diameter** and **lateral displacement** from the main flow axis.  
This dataset captures realistic aerosol behavior relevant to **public health**, **environmental studies**, and **fluid dynamics** research.

---

### Columns

| Column | Description |
|:-------|:-------------|
| `x` | Particle diameter in metres (m) |
| `y` | Lateral distance from the mouth (metres); `y = 0` denotes the central airflow axis |

---

### Structure

- **Total points:** 146,400  
- **True clusters (a priori):** 5  

**Physical meaning of clusters:**
1. **Cluster 1, 2 & 3:** High-velocity core (main airflow trajectory)  
2. **Clusters 4 & 5:** Particles displaced *upward* and *downward* due to inertial effects  
  

These clusters reflect **flow-induced segregation** and **turbulence-driven dispersion patterns**.

---

### 🧠 Use Cases

- Benchmark probabilistic and noise-robust clustering (e.g., **GMM**, **SUN**)  
- Study **aerosol dispersion** and **uncertainty quantification**  
- Demonstrate **data-driven detection of flow regions** in CFD simulations  

