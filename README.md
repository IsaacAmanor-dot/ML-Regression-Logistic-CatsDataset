# ML-Regression-Logistic-CatsDataset

This project explores gradient descent, linear regression, and logistic regression using both synthetic datasets and the real **cats vs. non-cats** image dataset. The goal is to understand optimization behavior, model fitting, generalization performance, and overfitting under different training–testing configurations.

---

## 📌 Project Summary

The repository contains five major tasks:

1. **Gradient Descent on a Smooth Function**  
   - Implemented gradient descent on  
     $f(x)=\sqrt{x^2+5}.$
   - Tested multiple step sizes and visualized convergence behavior.

2. **Linear Regression with Two-Dimensional Data**  
   - Generated synthetic data  
     $y = 4 + 4x_1 + 0.5x_2 + \varepsilon.$
   - Solved using the normal equation and plotted the regression plane.

3. **Logistic Regression on Gaussian Clusters**  
   - Generated two 2D Gaussian classes and trained logistic regression.  
   - Achieved:  
     - **Training accuracy:** 0.98  
     - **Testing accuracy:** 1.0  
   - Visualized the learned decision boundary.

4. **Logistic Regression on Cats vs. Non-Cats (Original Split)**  
   - Used provided HDF5 datasets (`train_catvnoncat.h5`, `test_catvnoncat.h5`).  
   - Flattened and normalized 64×64×3 images.  
   - Achieved:  
     - **Training accuracy:** 0.9952  
     - **Testing accuracy:** 0.70  
   - Reported all misclassified test indices and displayed 4 failure cases.

5. **Logistic Regression with Modified Training–Testing Split**  
   - Reconstructed the dataset using only the original 209 training images.  
   - New training size:  
     $160 + 6 = 166$
     based on the last digit of the student ID.  
   - Remaining 43 images used as the new test set.  
   - Achieved:  
     - **Training accuracy:** 1.0  
     - **Testing accuracy:** 0.5349  
   - Listed all misclassified indices and displayed 4 misclassified images.  
   - Demonstrated severe **overfitting**.

---

## 🧠 Key Takeaways

### 💡 Optimization  
- Gradient descent is highly sensitive to the learning rate.  
- Moderate learning rates converge; large ones diverge or oscillate.

### 📈 Regression  
- Linear regression successfully recovers model parameters when the underlying model is linear.  
- Visualization of the regression plane confirms good model fit.

### 🧩 Classification  
- Logistic regression performs well when classes are linearly separable (Gaussian task).  
- Performance drops significantly on high-dimensional image data (cat dataset).  
- Modified training split (Task 5B) clearly shows **overfitting** due to reduced data diversity.

---


