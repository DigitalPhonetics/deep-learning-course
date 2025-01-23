# Using GPUs with PyTorch

PyTorch provides strong support for GPU acceleration using CUDA. To leverage GPUs in your PyTorch code, you need to ensure that your system has a compatible NVIDIA GPU and the necessary CUDA libraries installed.

## Checking for GPU Availability

To check if PyTorch can access a GPU, you can use the following code snippet:

```python
import torch

if torch.cuda.is_available():
    print("CUDA is available. You can use GPU.")
else:
    print("CUDA is not available. Using CPU instead.")
```

## Moving Tensors to GPU

To perform computations on a GPU, you need to move your tensors and models to the GPU. This can be done using the `.to()` or `.cuda()` methods. Here is an example:

```python
# Assuming you have a tensor `x` and a model `model`
device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
x = x.to(device)
model = model.to(device)
```

## Restricting GPU Usage with `CUDA_VISIBLE_DEVICES`

In some cases, you might want to restrict your PyTorch code to use specific GPUs. This can be done using the `CUDA_VISIBLE_DEVICES` environment variable. For example, to restrict PyTorch to use only the first and third GPUs, you can set the environment variable as follows:

```bash
export CUDA_VISIBLE_DEVICES=0,2
```

You can set this variable in your terminal before running your PyTorch script:

```bash
CUDA_VISIBLE_DEVICES=0,2 python your_script.py
```

Alternatively, you can set this variable within your Python script:

```python
import os
os.environ["CUDA_VISIBLE_DEVICES"] = "0,2"
```

By setting `CUDA_VISIBLE_DEVICES`, you can control which GPUs are visible to your PyTorch code, allowing you to manage GPU resources more effectively.
