# Model-Compression-and-Pruning-Project

This repository contains the code, report, and model weights for our **10-605 Mini Project** at Carnegie Mellon University. The goal was to explore and compare three neural network pruning techniques for compressing deep learning models while preserving accuracy. In this project, we implemented and compared three neural network pruning methods: Wanda (Weight and Activation Pruning), L1-norm filter pruning, and Network Slimming.

## 🧠 Project Summary

We implemented and evaluated three distinct pruning methods:

1. **L1-norm Based Filter Pruning**  
   Structured pruning by ranking filters based on L1 norm and removing the least important ones progressively.

2. **WANDA (Weight and Activation-aware Pruning)**  
   Unstructured pruning method that combines weight magnitude with the strength of corresponding activation channels to score importance.

3. **Network Slimming**  
   Channel pruning technique based on BatchNorm γ scaling factors, combined with L1 regularization and post-pruning fine-tuning.

## 📊 Results

We compared all methods in terms of:
- **Sparsity vs. Validation Accuracy Trade-offs**
- **Implementation Complexity**
- **Fine-tuning effectiveness**

Key insights:
- **WANDA** achieved the best overall sparsity-accuracy balance.
- **L1-norm** is the simplest to implement.
- **Network Slimming** requires more training and tuning effort but performs well under moderate sparsity.

Refer to `10605_Report.pdf` for full methodology, figures, and analysis.

## 📁 File Structure

├── 10605_Report.pdf # Full report with methodology, figures, and comparisons
├── README.md # This file
├── my_model_weights_1.pt # Pretrained model (baseline or L1 pruned)
├── my_model_weights_2.pt # Model after WANDA pruning
├── my_model_weights_3.pt # Model after Network Slimming and fine-tuning

## 👥 Authors

- HsiangYu Lee (hsiangyl@andrew.cmu.edu)  
- Leyla Li (leylal@andrew.cmu.edu)  
- Shizhuo Li (shizhuol@andrew.cmu.edu)  

## 📄 References

- Li et al., *Pruning Filters for Efficient ConvNets*, 2017 [arXiv:1608.08710](http://arxiv.org/abs/1608.08710)  
- Liu et al., *Learning Efficient Convolutional Networks through Network Slimming*, 2017 [arXiv:1708.06519](http://arxiv.org/abs/1708.06519)

