## Results
Version|Accuracy|Precision|Recall|F1 score|Improvements|Reason
|--|--|--|--|--|--|--|
|1|0.8593|0.8592|0.8746|0.8582|original notebook|/
|2|0.9222|0.9217|0.9290|0.9219|reduce `LR` to e-5, add weight decay in loss function by `AdamW`|try popular overfit solutions
|3|0.9370|0.9364|0.9424|0.9364|add `ReduceLROnPlateau` and `EarlyStopping`, tune hyperparameters|search highest accuracy of the model
|4|0.9296|0.9291|0.9358|0.9295|reduce the number of neurons of inner layers, enable denoise()|`train loss` ≈ 100 * `valid loss`<br> the model may be too complex

## Report

Compared to the offline method, online recognition responds faster, while bringing 3 technical problems. See [Problem_Definition.pdf](Problem_Definition.pdf)

## Dataset and Model

Models: [Google Drive](https://drive.google.com/drive/folders/1DxGDkx2jUxWzBV1m0Y0hdDqEDl0OJWBU?usp=share_link) <br>
Dataset: [SHREC 2021 Gesture Benchmark](https://univr-vips.github.io/Shrec21/)