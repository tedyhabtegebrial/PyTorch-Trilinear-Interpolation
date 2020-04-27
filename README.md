# PyTorch-Trilinear-Interpolation
Pytorch Trilinear Interpolation
```python
import torch
from interpolation import TrilinearIntepolation
batch_size, width, height, depth = 1, 128, 128, 32
num_channels = 32
# Input data
interpolated_data = torch.rand(batch_size, num_channels, depth, height, width).float()
sampling_grid = (torch.rand(batch_size, height, width, 3) - 0.5)*2.0

# create interpolation layer
trilinear_interpolation = TrilinearIntepolation()
# apply_interpolation
interpolated_data = trilinear_interpolation(interpolated_data, sampling_grid)
print(interpolated_data.shape)

```
