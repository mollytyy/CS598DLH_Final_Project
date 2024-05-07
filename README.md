# CS 598 DLH Final Project
This repository is the final project for CS 598 Deep Learning for Healthcare course taught by Professor Jimeng Sun at University of Illinois Urbana-Champaign Spring 2024. We are reproducing the Drug-Drug Interaction experiment from the paper [Conditional Graph Information Bottleneck for Molecular Relational Learning](https://arxiv.org/pdf/2305.01520), which the original github repository can be found [here](https://github.com/Namkyeong/CGIB). 


## Requirements

Create a virtual environment and install jupyter notebook. Navigate to the directory. 

To install requirements:

```setup
pip install -r requirements.txt
pip install torch==1.8.1+cu111 torchvision==0.9.1+cu111 torchaudio==0.8.1 -f https://download.pytorch.org/whl/torch_stable.html
```
*OR*

Start the notebook and proceed to run the code blocks under `Methodology - Environment`

## Data
(For running the code for the first time)
  1. Create a `processed` folder under `DrugDrugInteraction\data`
  2. Run the code blocks under `Data` to clean and create .pt files
 
 **Note:** This might take a while, once the files are created, skip this step for future runs

## Training

To train the model in the paper:

Continue to run the [notebook](DL4LH_Team122.ipynb) to load the datasets, define hyperparameters, and define the CGIB model.

## Evaluation

Continue to run the notebook to evaluate the model. This step could take hours depending on the number of epochs. Screenshots and text files of previously obtained results are attached.  

## Results

Our reproduced model achieved the following performance on Drug-Drug Interaction using CGIB model:

| Metric             | Original Paper  | Replicated Results |
| ------------------ |---------------- | ------------------ |
| AUROC              |     94.74       |        93.55       |
| Accuracy (%)       |     86.88       |        86.32       |


## Citation

Namkyeong Lee, Dongmin Hyun, Gyoung S. Na, Sungwon Kim, Junseok Lee, and Chanyoung Park. "Conditional Graph Information Bottleneck for Molecular Relational Learning." ICML 2023.
```
@article{lee2023conditional,
  title={Conditional Graph Information Bottleneck for Molecular Relational Learning},
  author={Lee, Namkyeong and Hyun, Dongmin and Na, Gyoung S and Kim, Sungwon and Lee, Junseok and Park, Chanyoung},
  journal={arXiv preprint arXiv:2305.01520},
  year={2023}
}
```
