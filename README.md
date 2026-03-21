# LW4_Improving-CNN-Performance

**Google Colab Link: https://colab.research.google.com/drive/1saLA4yauIrr2V7tt4vlgavwMPf5hd2ce?usp=sharing**

## A. Model Evaluation Analysis

**1. What were the weakest-performing classes based on the confusion matrix?**  

The confusion matrix highlights which classes the model misclassified most often. Typically, these are classes with overlapping visual features or fewer training samples.

**2. How did Precision, Recall, and F1-score vary across classes?**  

- Precision was higher in classes with distinct features (fewer false positives).
- Recall was lower in classes where the model missed many true samples (more false negatives).
- F1-score balanced both, showing which classes had consistent performance versus those with trade-offs.

**3. What does a low recall indicate in your model?**  

A low recall indicates that the model failed to correctly identify many actual instances of a class. This means there are many false negatives, and the model is missing important data points that belong to that class.

**4. How does AUC score reflect model performance compared to accuracy?**  

The AUC score reflects the model’s ability to distinguish between classes across all classification thresholds, while accuracy only measures overall correctness at a fixed threshold. AUC is a more reliable metric, especially when dealing with imbalanced datasets, because it evaluates the model’s discrimination capability rather than just correct predictions.

---

## B. Model Improvement

**5. How did data augmentation affect validation accuracy?**  

Data augmentation improved validation accuracy by increasing the diversity of the training dataset. It helped the model generalize better to unseen data by introducing variations such as rotation, flipping, and scaling, which reduced overfitting.

**6. Why is Batch Normalization important in CNNs?**  

Batch Normalization is important because it normalizes the inputs of each layer, which stabilizes and speeds up the training process. It also helps reduce internal covariate shift and allows the use of higher learning rates, improving overall performance.

**7. What role did Dropout play in improving your model?**  

Dropout helped prevent overfitting by randomly disabling a fraction of neurons during training. This forced the model to learn more robust and generalized features instead of relying too heavily on specific neurons.

**8. How did Early Stopping prevent overfitting?**  

Early Stopping prevented overfitting by stopping the training process once the validation performance stopped improving. This ensured that the model did not continue learning noise from the training data.

---

## C. Performance Comparison

**9. What improvements were observed after modifying the model?**   

After modifying the model, there was an increase in validation accuracy and a decrease in validation loss. The model also showed better performance in terms of precision, recall, and F1-score, indicating improved generalization.

**10. Which enhancement contributed the most to performance improvement? Why?**  

Data augmentation contributed the most to performance improvement because it effectively increased the size and diversity of the dataset. This allowed the model to learn more robust features and reduced overfitting significantly.

**11. Did the gap between training and validation accuracy decrease? Explain.**  

Yes, the gap between training and validation accuracy decreased. This indicates that the model became less overfitted and more capable of generalizing to new, unseen data.

---

## D. Explainability (Grad-CAM Integration)

**12. How did Grad-CAM help in understanding model predictions?**  

Grad-CAM helped by visualizing the regions of the image that the model focused on when making predictions. This provided insight into how the model made decisions.

**13. Did the improved model focus on more relevant regions? Provide evidence.**  

Yes, the improved model focused more on relevant regions. The Grad-CAM heatmaps showed stronger and more concentrated activations on important features of the object, while reducing attention to irrelevant background areas.

**14. Why is explainability important in real-world AI applications?**  

Explainability is important because it builds trust in AI systems, helps identify errors or biases, and ensures transparency. In real-world applications such as healthcare and security, understanding how a model makes decisions is critical for reliability and accountability.
