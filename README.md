# PyTorch-Trilinear-Interpolation

Example Usage

```python
import torch
from interpolation import TrilinearIntepolation
batch_size, width, height, depth = 1, 128, 128, 32
num_channels = 32
# Input data
input_data = torch.rand(batch_size, num_channels, depth, height, width).float()
sampling_grid = (torch.rand(batch_size, height, width, 3) - 0.5)*2.0

# create interpolation layer
trilinear_interpolation = TrilinearIntepolation()
# apply_interpolation
interpolated_data = trilinear_interpolation(input_data, sampling_grid)
print(interpolated_data.shape)

```
