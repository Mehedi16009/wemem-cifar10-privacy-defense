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
<img width="707" height="701" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/bbc7d3c2-fec7-4806-9039-333d550ddd52" />


### Training & Validation Accuracy
<img width="781" height="694" alt="Train and Validation Accuracy" src="https://github.com/user-attachments/assets/afa6bad3-3d64-41f0-88a6-964efcb66327" />


### Training & Validation Loss
<img width="781" height="693" alt="Train and Validation Loss" src="https://github.com/user-attachments/assets/8af78623-6ae4-4173-a796-374b48344aa4" />


⸻

📊 Planned Future Work:
	•	LLM/VLM-powered interpretability to explain and visualize memorization patterns in pruned models.
	•	Integration with automated hyperparameter tuning for optimal privacy–utility tradeoffs.
 📬 Contact
Sincerely,
Md. Mehedi Hasan
Prospective Ph.D. Student
Lecturer, Dept. of Computer Science & Engineering
Global Institute of Information Technology (GIIT), Bangladesh
📧 Email: mehedi.hasan.ict@mbstu.ac.bd | mehedi.hasan.ict13@gmail.com
📞 Phone: +880 1789 113 669 | +880 1334 110 929
🌐 Portfolio: [Link](https://md-mehedi-hasan-resume.vercel.app/)
