# DISTRA: Flood Prediction AI Model

DISTRA is an artificial intelligence model designed for predicting floods based on rainfall data. It leverages Long Short-Term Memory (LSTM) networks, a type of recurrent neural network (RNN), to capture and analyze temporal patterns in rainfall data.

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Data Format](#data-format)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)

## Overview

Flood prediction is a critical aspect of disaster management. DISTRA utilizes LSTM, a type of neural network well-suited for sequence prediction, to analyze historical rainfall data and predict potential flood occurrences. The model takes into account the temporal dependencies in the data, making it robust for capturing evolving weather patterns.

## Key Features

- **LSTM Architecture**: Utilizes Long Short-Term Memory networks for effective sequence modeling.
- **Rainfall Data Input**: Takes historical rainfall data as input for flood prediction.
- **Scalability**: Can be trained on diverse datasets for different geographical locations.
- **Customizable Thresholds**: Allows users to set custom thresholds for flood prediction alerts.

## Installation

To install DISTRA and its dependencies, follow these steps:

```bash
pip install -r requirements.txt
```

## Usage

Use DISTRA for flood prediction by following these steps:

```python
from distra import Distra

# Load the model
model = Distra()
# Provide rainfall data for prediction
rainfall_data = [0.1, 0.5, 1.2, 0.8, ...]

# Get flood prediction
prediction = model.predict(rainfall_data)

print(f"Flood Prediction: {prediction}")
```

## Data Format

DISTRA expects input data in the form of a time series array, where each element corresponds to the amount of rainfall at a specific time. Ensure that the data is properly preprocessed and normalized before feeding it to the model.

## Model Training

To train DISTRA on your own dataset, follow these steps:

1. Prepare your dataset in the required format.
2. Use the `train` function, providing your dataset and desired hyperparameters.

```python
from distra import train

# Example training
train_data = [...]  # Your training dataset
train_model(train_data, epochs=50, batch_size=32)
```

## Contributing

Contributions to DISTRA are welcome! If you find issues or have ideas for improvements, please open an issue or submit a pull request. See [CONTRIBUTING.md](CONTRIBUTING.md) for more details.

## License

This project is licensed under the [MIT License](LICENSE).
