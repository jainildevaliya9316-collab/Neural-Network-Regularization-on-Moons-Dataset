# Moons Dataset & Regularization

Generate Make-Moons dataset without using sklearn make_moons. Use default noise 0.2, also create two extra test sets with noise 0.1 and 0.3 for robustness reporting. Make training set and test set with 500 points each. Standardize x after the split using train statistics only. Create a validation split of the train set with 20 percent for model selection. Use random seed 1337.
Train the following models:
1. MLP with hidden layer - early stopping (patience=50)
2. MLP with L1 regularization . L1 gird λ ∈ {1e−6, 3e−6, 1e−5, 3e−5, 1e−4, 3e−4}. Report layerwise sparsity and validation AUROC vs.  λ
3. MLP with L2 regularization (you may vary the penalty coefficient by choose the best one using a validation dataset)
4. Logistic regression with polynomial features (x₁x₂, x₁², etc.)
## Evaluation and Analysis 
• Evaluate test accuracy on noise = 0.20, and robustness accuracy on 0.10 & 0.30.

• Create a table with test accuracy for the four models on the three test noise levels. Include parameter count.

• Plot decision boundaries side by side for all 4 models with default noise 0.2.

• Discuss:

	- Effect of L1 on sparsity and boundary jaggedness
    
	- Effect of L2 on smoothness and margin
    
• Add class imbalance (70:30) in the trainset while keeping the testset balanced. Report accuracy and AUROC and discuss the effect of imbalance.
