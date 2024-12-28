# A-Cascaded-Dilated-Convolution-Approach-for-Mpox-Lesion-Classification

[Link to pre-print](https://www.researchgate.net/publication/387032588_A_Cascaded_Dilated_Convolution_Approach_for_Mpox_Lesion_Classification)

## Project Overview

The global outbreak of the Mpox virus, classified as a Public Health Emergency of International Concern (PHEIC) by the World Health Organization, presents significant diagnostic challenges due to its visual similarity to other skin lesion diseases. Traditional diagnostic methods for Mpox, which rely on clinical symptoms and laboratory tests, are slow and labor intensive. Deep learning-based approaches for skin lesion classification offer a promising alternative. However, developing a model that balances efficiency with accuracy is crucial to ensure reliable and timely diagnosis without compromising performance. This study introduces the Cascaded Atrous Group Attention (CAGA) framework to address these challenges, combining the Cascaded Atrous Attention module and the Cascaded Group Attention mechanism. The Cascaded Atrous Attention module utilizes dilated convolutions and cascades the outputs to enhance multi-scale representation. This is integrated into the Cascaded Group Attention mechanism, which reduces redundancy in Multi-Head Self-Attention. By integrating the Cascaded Atrous Group Attention module with EfficientViT-L1 as the backbone architecture, this approach achieves state-of-the-art performance, reaching an accuracy of 98% on the Mpox Close Skin Image (MCSI) dataset while reducing model parameters by 37.5% compared to the original EfficientViT-L1. The model's robustness is demonstrated through extensive validation on two additional benchmark datasets, where it consistently outperforms existing approaches.

## Dataset Information

This repository works with three datasets:
1. [Mpox Close Skin Image Dataset (MCSI)](https://arxiv.org/abs/2305.18489)
2. [Monkeypox Skin Images Dataset (MSID)](https://www.kaggle.com/datasets/dipuiucse/monkeypoxskinimagedataset)
3. [Monkeypox Skin Lesion Dataset (MSLD))](https://www.kaggle.com/datasets/joydippaul/mpox-skin-lesion-dataset-version-20-msld-v20)

### Dataset Access
All datasets and the trained model (for Grad-CAM visualization) are available in this shared Google Drive:
[[Drive Link Placeholder](https://drive.google.com/drive/folders/1KqQTi6mrUHuA3Oaf8G-PdpX90yNXXcgY?usp=sharing)]

## Project Structure
```
.
├── main.ipynb                    # Main notebook for running all experiments
├── requirements.txt              # Project dependencies
├── README.md                     # This file
├── MSID/
│   └── Scores and Hyperparams/  
│       ├── model_name1/
│       │   └── model_params.csv
│       └── model_name2/
│           └── model_params.csv
├── MSLD/
│   └── Scores and Hyperparams/  
│       ├── model_name1/
│       │   └── model_params.csv
│       └── model_name2/
│           └── model_params.csv
├── MCSI/
│   └── Scores and Hyperparams/  
│       ├── model_name1/
│       │   └── model_params.csv
│       └── model_name2/
│           └── model_params.csv
├── MCSI_Implementation.ipynb     # MCSI model implementation
├── MSID_Implementation.ipynb     # MSID model implementation
└── MSLD_Implementation.ipynb     # MSLD model implementation
├── Ablation Study/
    └── Scores and Hyperparams/  
        ├── model_name1/
        │   └── model_params.csv
        └── model_name2/
            └── model_params.csv
```

## Installation

```bash
# Clone the repository
git clone https://github.com/TheUndercover01/A-Cascaded-Dilated-Convolution-Approach-for-Mpox-Lesion-Classification.git
cd A-Cascaded-Dilated-Convolution-Approach-for-Mpox-Lesion-Classification

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```


## Running the Code

### Main Execution
All experiments can be run through the main notebook:
```bash
jupyter notebook main.ipynb #change the model_name and dataset in the file while reproducing results
```

### Individual Model Implementations
You can also run individual model implementations:
- MCSI: `MCSI_Implementation.ipynb`
- MSID: `MSID_Implementation.ipynb`
- MSLD: `MSLD_Implementation.ipynb`

## Hyperparameter Configuration

For reproducibility, each dataset has its own hyperparameters stored in CSV format:
```
dataset[1/2/3]/Scores and Hyperparams/model_name[1/2]/model_params.csv
```


## Contact

For questions or issues, please:
1. Open an issue in this repository
2. Contact: [[email](aayush.m.deshmukh@gmail.com)]