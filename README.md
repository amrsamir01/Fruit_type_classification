# Cross-Species Fruit Quality Grading via Few-Shot Metric Learning

**Author:** Amr Samir  
**Master's Thesis - 2026**

## 📌 Research Gap

> *"While models can classify fruit species with high accuracy, they fail to generalize quality grading (Good/Bad) to unseen fruit types without retraining."*

This research addresses **intra-class quality grading** using **few-shot metric learning**, proving that models can learn "class-agnostic defect representations" that transfer across fruit species.

## 🎯 Key Contribution

- **Train on:** Apple, Banana, Grape  
- **Test on:** Mango, Orange *(never seen during training!)*  
- **Method:** Prototypical Networks + Supervised Contrastive Loss

## 📊 Results Summary

| Method | Seen Fruits | Unseen Fruits |
|--------|-------------|---------------|
| Supervised CNN | 98% | ~60% |
| Zero-Shot CLIP | 70% | 70% |
| **Our Method (5-shot)** | **95%** | **85%** |

## 🗂️ Project Structure

```
├── FewShot.ipynb           # Main implementation (Prototypical Network)
├── DenseNet121.ipynb       # Baseline: Supervised DenseNet
├── VGG16.ipynb             # Baseline: Supervised VGG16
├── dataset/                # Organize your data here
│   ├── apple/
│   │   ├── good/
│   │   └── bad/
│   ├── banana/
│   │   ├── good/
│   │   └── bad/
│   └── ...
├── checkpoints/            # Saved models
└── results/                # Figures and metrics
```

## 📥 Datasets

1. **Fruits Fresh and Rotten** (Primary):  
   [Kaggle Link](https://www.kaggle.com/datasets/sriramr/fruits-fresh-and-rotten-for-classification)

2. **Fruit Quality Good/Bad** (Zenodo):  
   [Zenodo Link](https://zenodo.org/records/1310165)

## 🚀 Quick Start

```python
# 1. Install dependencies
pip install torch torchvision tqdm scikit-learn matplotlib seaborn

# 2. Download dataset and organize as shown above

# 3. Update config.DATA_ROOT in FewShot.ipynb

# 4. Run the notebook cells sequentially
```

## 📝 Paper Structure

1. **Introduction** - The generalization problem in fruit grading
2. **Related Work** - CNN grading, Few-shot learning, CLIP in agriculture
3. **Methodology** - Prototypical Networks + SupCon Loss
4. **Experiments**
   - Cross-species generalization (KEY)
   - N-shot ablation
   - Baseline comparisons
5. **Results & Discussion**
6. **Conclusion**

## 📚 Key References

- Snell et al., "Prototypical Networks for Few-shot Learning" (NeurIPS 2017)
- Khosla et al., "Supervised Contrastive Learning" (NeurIPS 2020)
- AgriCLIP (COLING 2025)
- MFLI for Pomelo Quality (Computers and Electronics in Agriculture, 2024)

## 📧 Contact

**Amr Samir** - Master's Student  
Research Focus: Computer Vision, Few-Shot Learning, Agricultural AI
