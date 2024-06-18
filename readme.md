## Results
Version|Accuracy|Precision|Recall|F1 score|Improvements|Reason
|--|--|--|--|--|--|--|
|1|0.8593|0.8592|0.8746|0.8582|original notebook|/
|2|0.9222|0.9217|0.9290|0.9219|reduce `LR` to e-5, add weight decay in loss function by `AdamW`|try popular overfit solutions
|3|0.9370|0.9364|0.9424|0.9364|add `ReduceLROnPlateau` and `EarlyStopping`, tune hyperparameters|search highest accuracy of the model
|4|0.9296|0.9291|0.9358|0.9295|reduce the number of neurons of inner layers, enable denoise()|`train loss` ≈ 100 * `valid loss`<br> the model may be too complex

## Future Improvements

The current data argumentation method is a simple replication of the same data. We can add random noise to the replicates, which encourages the robustness of models. 