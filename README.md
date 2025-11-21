# DS4002-Project-3
## Contents
This repository contains all files, code, and documentation for our image-classification analysis of apple leaf diseases, using multiple machine-learning and deep-learning models. It includes Jupyter notebooks for data preprocessing, image augmentation, model training, and evaluation across traditional machine-learning baselines and convolutional neural networks (CNNs). All raw images, cleaned datasets, intermediate outputs, and trained model artifacts are organized into dedicated folders to support clarity, reproducibility, and transparent experimentation. Visualizations, performance metrics, and exported predictions are stored in the Output directory, while all workflow scripts—including data ingestion, modeling pipelines, and evaluation routines—are contained in the Scripts directory.

## Software and Platform
This project was developed in Python 3 using Jupyter Notebooks run primarily on the University of Virginia’s Rivanna High-Performance Computing (HPC) cluster. Rivanna provided the CPU/GPU resources necessary for training convolutional neural networks and running image-processing pipelines at scale.

Core libraries include:

- TensorFlow / Keras for CNN model development and training
- scikit-learn for baseline machine-learning models and evaluation
- pandas and numpy for dataset preparation and manipulation
- matplotlib and seaborn for visualization
- opencv-python and Pillow for image loading, preprocessing, and augmentation

All work was conducted through JupyterLab on Rivanna, ensuring a consistent computing environment, reproducible package versions, and stable access to GPU resources. The workflow is compatible with any Linux-based HPC environment or local Python installation using the same dependencies.

## Documentation Map
```text
DS4002-Project-3/
├── Data/
│   ├── Metadata.md
│   └── AppleData/
│       ├── Apple___Apple_scab/
│       ├── Apple___Black_rot/
│       ├── Apple___Cedar_apple_rust/
│       ├── Apple___healthy/
│       └── Background_without_leaves/
├── Output/
│   ├── .ipynb_checkpoints/
│   │   └── image_distribution-checkpoint.png
│   ├── Category_examples.png
│   ├── cnnAccuracy.png
│   ├── cnnConfMatrix.png
│   └── image_distribution.png
├── Scripts/
│   ├── .ipynb_checkpoints/
│   │   ├── AnotherCNN-checkpoint.ipynb
│   │   ├── Decision_Tree-checkpoint.ipynb
│   │   ├── NicksCNN-Copy1-checkpoint.ipynb
│   │   ├── NicksCNN-checkpoint.ipynb
│   │   ├── Untitled-checkpoint.ipynb
│   │   ├── decsion_tree-checkpoint.ipynb
│   │   ├── eda-checkpoint.ipynb
│   │   ├── knn-checkpoint.ipynb
│   │   └── test-checkpoint.ipynb
│   ├── AnotherCNN.ipynb
│   ├── Decision_Tree.ipynb
│   ├── decsion_tree.ipynb
│   ├── eda.ipynb
│   ├── knn.ipynb
├── LICENSE
└── README.md
```

## Instructions for Reproducibility 
1. **Clone or Access the Repository**  
   Create a local copy of this repository on your machine, or open it directly through Rivanna’s JupyterLab interface.

2. **Verify Dataset Location**  
   The full Apple disease image dataset is included in `Data/AppleData/`. **Do not change the folder structure**, as scripts depend on the original class subfolders.

3. **Run Notebooks in Logical Order**  
   Navigate to the `Scripts/` folder and execute the notebooks sequentially:  
   **EDA → Preprocessing → Baseline Models → CNN Models → Evaluation**.  
   - Each notebook regenerates plots, metrics, and artifacts in the `Output/` directory.  
   - Deep learning notebooks require substantial memory; use an environment with **≥24 GB RAM** (e.g., Rivanna compute nodes) to avoid runtime failures.

4. **Reproduce All Figures and Outputs**  
   All figures and model outputs are automatically recreated when notebooks are run.  
   - To start completely from scratch, optionally delete the contents of `Output/` before re-executing the notebooks in order.
