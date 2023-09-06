Code for the Transformer AIDA Workshop
===================================================

This repository contains the practical material for the AIDA Workshop on Transformers. It's a minimal example of how we can implement basic image Transformers in pytorch, as well as how we can use the pre-trained Transformer models for vision tasks from the Huggingface library.

Learning outcomes
=================
The goal is to become familiar with building a Transformer neural network using the building blocks in Pytorch and Huggingface. 

After going  through the material, the student should:
 - Be able to use the TransformerEncoder and TransformerDecoder modules in Pytorch
 - Be able to use existing Transformer models for vision from Huggingface and apply them to their own data.


Workshop material
=================

The learning material is centered around notebooks, it is a suitable platform for code-along style workshops, but for real reproducible experiments you should convert these steps to batch processing scripts.

The notebooks are designed to either 1) be run from your own computer, in which case you need to perform the installation steps below, or 2) From Google Colab in which case you need to follow the "colab" link after the link to the notebook below.

Workshop notebooks:
 - [Transformers for images](notebooks/transformsers_for_images.ipynb) ([colab](https://colab.research.google.com/github/eryl/aida-transformers-workshop-code/blob/main/notebooks/graph_basics.ipynb))
 
Installing dependencies for local use
=====================================
First clone this repository using git:

```shell
#Download the workshop material (this repository)
> git clone git@github.com:eryl/aida-transformers-workshop-code.git
```
This workshop assumes you are using [Anaconda](https://www.anaconda.com/) (or a variant like [miniforge](https://github.com/conda-forge/miniforge)), so install one if you don't have it. 

It is highly suggested that you use the `libmamba` dependency solver, the default conda solver is extremely slow for this relatively complex environment file:

```shell
# Create workshop environment "aida_workshop_gnn"
> conda install -n base conda-libmamba-solver # install the libmamba solver to the base environment
> conda env create -f environment.yml --solver=libmamba  # Create the environemnt
```

Which will install all necessary requirements. Activate the environment by running:
```shell
# Create workshop environment "aida_workshop_gnn"
> conda activate aida_workshop_gnn
```

Start the local jupyter server by running
```shell
# Start the jupyter notebook server
> jupyter notebooks
```

As an alternative to using `conda` above, we recommend that you install [`mamba`](https://github.com/mamba-org/mamba) instead, which makes all these installations much faster:

```shell
# Install the free mamba tool
> conda install -n base mamba -c conda-forge
# Create workshop environment "aida_workshop_gnn"
> mamba env create -f environment.yml
```
