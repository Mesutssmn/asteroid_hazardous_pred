# Asteroid Hazard Classification
This project aims to classify potentially hazardous asteroids (PHA) using a neural network model trained on a dataset provided by NASA’s Jet Propulsion Laboratory (JPL). The dataset includes physical and orbital characteristics of asteroids, and the task focuses on addressing class imbalance by applying SMOTE to improve detection of hazardous asteroids.

---

## About the Dataset

The dataset is officially maintained by NASA’s Jet Propulsion Laboratory (JPL), California Institute of Technology. JPL provides up-to-date information on small bodies in the solar system, including asteroids, their orbits, and physical properties.

- Dataset source: [Asteroid Dataset on Kaggle](https://www.kaggle.com/datasets/sakhawat18/asteroid-dataset/data)  
- Contents: Physical features (diameter, albedo, mass, etc.), orbital parameters (eccentricity, semi-major axis, inclination, etc.), and hazard classification (PHA flag).

### Key Columns

| Column Name | Description                                     |
|-------------|------------------------------------------------|
| `pha`       | Potentially Hazardous Asteroid flag (1 or 0)  |
| `H`         | Absolute magnitude                             |
| `diameter`  | Diameter in kilometers                         |
| `albedo`    | Geometric albedo                              |
| `a`, `e`, `i` | Orbital elements: semi-major axis, eccentricity, inclination |
| Others      | Various orbital and physical parameters        |

---

## Project Workflow

1. **Data Cleaning:** Removed rows with missing critical values due to a high number of nulls in features like diameter and albedo.  
2. **Feature Scaling:** Applied `StandardScaler` to normalize features for better model convergence.  
3. **Handling Class Imbalance:** Used SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic samples for the minority class (hazardous asteroids).  
4. **Model Architecture:** Built a simple feedforward neural network with sigmoid output for binary classification.  
5. **Training & Evaluation:** Trained with early stopping and evaluated performance metrics including precision, recall, and F1-score.

---

## Results Summary

- The model achieves around **91% recall** on the hazardous asteroid class, improving detection of rare but critical samples.  
- Overall accuracy exceeds 99%, but accuracy alone is misleading due to class imbalance.  
- F1-score for the minority class is about 0.49, indicating room for improvement.

---

## Acknowledgements

This dataset and its maintenance by NASA and the Jet Propulsion Laboratory (JPL) are invaluable to the scientific community. Their commitment to openly sharing data enables research and applications in astronomy and astrophysics. Special thanks to NASA and JPL for providing this comprehensive dataset.

---

## Citation

If you use this dataset in your research, please cite:

**Hossain, M.S., Zabed, M.A. (2023).** *Machine Learning Approaches for Classification and Diameter Prediction of Asteroids.*  
In: Ahmad, M., Uddin, M.S., Jang, Y.M. (eds) Proceedings of International Conference on Information and Communication Technology for Development. Springer, Singapore.  
DOI: [10.1007/978-981-19-7528-8_4](https://doi.org/10.1007/978-981-19-7528-8_4)

---

## Future Work

- Experiment with more advanced models (e.g., XGBoost, LightGBM).  
- Perform feature engineering and dimensionality reduction (PCA, feature selection).  
- Test other data balancing techniques and ensemble methods.  
- Interpret model decisions to better understand characteristics of hazardous asteroids.

---

📫 Feel free to reach out for questions or collaborations.

> **Note:** This project contributes towards better understanding and early warning of asteroids that pose potential threats to Earth.

