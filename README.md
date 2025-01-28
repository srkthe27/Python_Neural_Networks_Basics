# Dense Layers with TensorFlow

This project demonstrates the use of TensorFlow's `Dense` layers for building a simple neural network. The code covers reshaping data, sequentially processing it through multiple layers, and interpreting the outputs. It is designed to serve as an educational example for those learning about neural networks and TensorFlow.

## Features

1. **Data Preparation**:

   - Input data is reshaped and processed for compatibility with TensorFlow layers.
   - Conversion of NumPy arrays to TensorFlow tensors ensures proper integration with the TensorFlow API.

2. **Layer Usage**:

   - Demonstrates the use of `Dense` layers with different configurations.
   - Activation functions (`sigmoid`) are applied to transform the data at each layer.

3. **Output Interpretation**:

   - Outputs of the network are displayed layer by layer.
   - Conditional logic is implemented to classify results based on a threshold (0.5).

## Prerequisites

- Python 3.7+
- TensorFlow 2.x
- NumPy

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### File Structure

```
.
├── main.py         # The primary Python script containing the code
├── README.md       # Project documentation
└── requirements.txt # List of dependencies (TensorFlow, NumPy)
```

### Running the Code

1. Open the terminal and navigate to the project directory.
2. Run the script:
   ```bash
   python main.py
   ```

### Expected Output

The script will:

- Print the shapes and values of the input data.
- Display the outputs of each layer (`a11`, `a21`, `a12`, `a22`, `a32`).
- Classify outputs as `1` or `0` based on a threshold of `0.5`.

### Code Overview

#### Data Preparation

The input data is defined as NumPy arrays and converted to TensorFlow tensors for compatibility.

```python
x = tf.convert_to_tensor([[1, 2, 3], [4, 5, 6]], dtype=tf.float32)
y = tf.convert_to_tensor([[1, 2, 3], [4, 5, 6], [7, 8, 9]], dtype=tf.float32)
```

#### Layer Definitions

Dense layers are defined and applied sequentially to transform the data:

```python
layer_11 = Dense(3, activation='sigmoid', input_shape=(3,))
a11 = layer_11(x)
```

#### Output Interpretation

Outputs are printed and classified as `1` or `0` based on a threshold:

```python
for i in range(len(a21)):
    print(a21[i].numpy())
    if a21[i] > 0.5:
        print("1")
    else:
        print("0")
```

### Contributing

Contributions are welcome! Feel free to fork this repository and submit pull requests.

### License

This project is licensed under the MIT License. See the LICENSE file for details.

### Acknowledgments

- TensorFlow documentation: [TensorFlow.org](https://www.tensorflow.org)
- NumPy documentation: [numpy.org](https://numpy.org)

Happy coding!

