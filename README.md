# Modular Debiasing of Latent User Representations in Prototype-based Recommender Systems @ ECML-PKDD'24

This repository hosts the code and and the settings for the paper ["Modular Debiasing of Latent User Representations in Prototype-based Recommender Systems"](https://karapostk.github.io/assets/pdf/melchiorre2024modular.pdf) by [Alessandro B. Melchiorre](https://karapostk.github.io/), Shahed Masoudian, Deepak Kumar, and Markus Schedl at ECML-PKDD'24.
![MMD_Debiasing](./results/plots/gender_lfm2bdemobias_mmd_bacc_ndcg_lams.png "MMD Gender Debiasing")

## CV
Ending my PhD in October, looking for Applied Scientist/Data Scientist positions.
[CV is here](https://github.com/hcai-mms/modprotodebias/blob/main/AlessandroBMelchiorreCV.pdf)
## Installation

### Environment

- Install the environment with
  `conda env create -f modprotodebias.yml`
- Activate the environment with `conda activate modprotodebias`


### Data

- move into the folder with `cd data/<dataset_folder>`
- run `python <dataset_name>_processor.py`

If you have problems with the LFM2b data, ping me and I'll be happy to help

### Pre-Trained Models

- download the pre-trained ProtoMF models from [here](https://drive.jku.at/filr/public-link/file-download/0cce88f0905932a10190c68ce5731feb/62214/-7633188943201829349/pre_trained_models.zip)
- place the two folders inside `pre_trained_models` folder (default)
- (optional) adjust the path files in the `conf.yml` if you have issues

## Usage

Adjust the configuration of your experiment in `run_full_debiasing.py`.

The experiments can be started with

`python start.py run_full_debiasing`

or define sweep configurations to use with the wandb sweep command

`wandb sweep sweep_config.yaml`


## Cite

```latex
@inproceedings{melchiorre2024modular,
  title = {Modular Debiasing of Latent User Representations in Prototype-based Recommender Systems},
  author = {Melchiorre, Alessandro B. and Masoudian, Shahed and Kumar, Deepak and Schedl, Markus},
  booktitle = {Proceedings of 2024 Joint European Conference on Machine Learning and Knowledge Discovery in Databases (ECML PKDD)},
  year = {2024},
}
```
## License
The code in this repository is licensed under the MIT License. For details, please see the LICENSE file.

## Acknowledgments
This research was funded in whole or in part by the Austrian Science Fund (FWF): P36413, P33526, and DFH-23, and by the State of Upper Austria and the Federal Ministry of Education, Science, and Research, through grant LIT-2021-YOU-215.
