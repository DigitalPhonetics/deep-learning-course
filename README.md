# Deep Learning Course at the IMS (University of Stuttgart)

This repository collects the tutorials for the deep learning course and accompanying material.

## Structure

* [Setup](Setup): Basics for getting started with PyTorch on Linux
* [PyTorch 1](PyTorch_1): Basics
  * [Tensor operations](PyTorch_1/1_tensors.ipynb)
  * [Gradient computation](PyTorch_1/2_gradients.ipynb)
  * [Simple data handling](PyTorch_1/3_data_handling.ipynb)
  * [Simple neural network](PyTorch_1/4_create_nn.ipynb)
* [PyTorch 2](PyTorch_2): Data Loading & Processing and Model Development for NLP
  * Example Task: Sentiment Analysis
  * Example Task: Part-Of-Speech Tagging
* [PyTorch 3](PyTorch_3): Training, Inference, Checkpoint Handling
* [PyTorch 4](PyTorch_4): Language Models

## How To Start
1. Open a terminal.
2. Change to the directory where you want to download this repository to, e.g., `cd ~/` to change to your home directory (create directories using `mkdir`).
3. Clone this repository to the current directory using `git`:
```bash
git clone https://github.com/DigitalPhonetics/deep-learning-course.git
```
4. Check out our [instructions](run_jupyter_notebook.md) for setting up Jupyter Notebooks.
5. Set up PyTorch as described in [this](pytorch_setup.ipynb) Jupyter Notebook.
6. Now you should be ready to use PyTorch in Python, and to be able to run all Jupyter Notebooks of this course.

## Help, Feedback & Other Questions
Many commands provide a help if you call them with the `-h` or `--help` argument, or appear in the manual with `man command` where *command* is the name of the command.

You can also contact us via ILIAS (e.g., in the forum), or [open an issue](https://github.com/DigitalPhonetics/deep-learning-course/issues/new/choose) in the GitHub repository!