# WEMEM-cifar10-privacy-defense
PyTorch implementation of WEMEM defense methods (RSW, RMR, SWMR) for CIFAR-10, with iterative pruning, memorization score estimation, LiRA membership inference attacks, and IEEE-ready result visualizations.

# WEMEM Privacy Defense on CIFAR-10

🔹 Improvements Over Original WEMEM Paper

This implementation extends the original WEMEM: Defending Against Membership Inference Attacks on Iteratively Pruned Deep Neural Networks framework with several enhancements for better stability, privacy–utility balance, and reproducibility.

✅ 1. Adaptive Learning Rate Scheduling
	•	Implemented Cosine Annealing with Warm Restarts to ensure smooth convergence during post-pruning fine-tuning.
	•	Prevents overfitting and boosts recovery after each pruning stage.

✅ 2. Early Stopping with Validation Monitoring
	•	Added validation-based early stopping to reduce unnecessary training epochs.
	•	Saves computation time while improving generalization.

✅ 3. Dynamic Memorization Score Thresholding
	•	Applied z-score normalization for memorization scores before thresholding.
	•	Reduces noise and false positives in identifying high-memorization samples.

✅ 4. Fine-Grained Iterative Pruning
	•	Layer-wise L1 unstructured pruning with adaptive sparsity increments instead of fixed rates.
	•	Achieves better accuracy retention while still removing redundant weights.

✅ 5. Privacy–Utility Re-Optimization
	•	Tuned RSW, RMR, and SWMR defense parameters for lower Membership Inference Attack (MIA) success rates with minimal accuracy drop.

✅ 6. Enhanced Evaluation Pipeline
	•	Automatically plots Accuracy vs. MIA Success Rate after each pruning/defense stage.
	•	Clear visual comparison between original model, pruned model, and defended model.

✅ 7. Colab-Friendly & Reproducible
	•	Fully runnable on Google Colab (T4/V100 GPUs) without code changes.
	•	Switchable dataset option: CIFAR-10 / CIFAR-100 for broader testing.

⸻

📊 Example Results:
## 📈 Model Performance

### Confusion Matrix
![Confusion Matrix](assets/confusion_matrix.png)

### Training & Validation Accuracy
![Train and Validation Accuracy](assets/train_val_accuracy.png)

### Training & Validation Loss
![Train and Validation Loss](assets/train_val_loss.png)

⸻

📊 Planned Future Work:
	•	LLM/VLM-powered interpretability to explain and visualize memorization patterns in pruned models.
	•	Integration with automated hyperparameter tuning for optimal privacy–utility tradeoffs.
