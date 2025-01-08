# Python Setup
The following steps guide you through the requirements to run Python with PyTorch as required for this course.

When working with Python and especially with running your code on remote machines, it is convenient to know about basic commands for Linux and to be aware of the computing resources at the IMS.

Therefore, we have collected basic instructions for [Bash](bash.md), [SSH](ssh.md), [Git](git.md) and [IDEs](ide.md) in the [Setup](.) folder of our GitHub repository https://github.com/DigitalPhonetics/deep-learning-course (where all information and instructions to be able to participate in the Introduction to DL course at the IMS are collected in).

Most of you probably already have worked with Linux, and feel free to consult other information online if you want to learn more!

Although you can run Python directly from the command-line (e.g., in a Linux terminal), for this course, we use Jupyter Notebooks where Python runs interactively in separate steps (so called cells).

For setting up these Jupyter Notebooks, check out our [instructions](run_jupyter_notebook.md).
Then you can continue with setting up PyTorch as described in [this](pytorch_setup.ipynb) Jupyter Notebook.

# Troubleshooting

**Q: Python cannot import Numpy**

**A:** Make sure that NumPy is installed. See installation commands in [pytorch_setup.ipynb](pytorch_setup.ipynb) or [run_jupyter_notebook.md](run_jupyter_notebook.md); the Python package is called numpy.

**Q: I cannot install Python packages when using pip**

**A:** Make sure that you have activated your virtual environment where you can write to!

**Q: I cannot install PyTorch**

**A:** Make sure that your version of Python is supported for the version of PyTorch you are going to install.

**Q: Python cannot import module X**

**A:** Make sure that the corresponding Python package is installed to your currently activated environment (if used).

For further help, see [here](../#help-feedback--other-questions).