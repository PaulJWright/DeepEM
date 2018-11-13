DeepEM: A Deep <i>Neural Network</i> for DEM Inversion
============================================
*Paul Wright*

**This is a working directory for a fully trained CNN for DEM Inversion.**

The model is as follows:

```python
model = nn.Sequential(
    nn.Conv2d(6, 300, kernel_size=1),
    nn.LeakyReLU(),
    nn.Conv2d(300, 300, kernel_size=1),
    nn.LeakyReLU(),
    nn.Conv2d(300, 300, kernel_size=1),
    nn.LeakyReLU(),
    nn.Conv2d(300, 300, kernel_size=1),
    nn.LeakyReLU(),
    nn.Conv2d(300, 18, kernel_size=1)).cuda()

dem_model_file = 'deepEM_model_cnn.pth'
model.load_state_dict(torch.load(dem_model_file))
```

This originates from the Gitlab repo.

<b>The model has been trained on the first 291 days in 2011</b>

--
