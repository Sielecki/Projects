# Hello World - TinyML

An introductory TinyML project demonstrating how to train a model to recognize the **sin function** and deploy it on an **Arduino Nano BLE Sense 33**. This project explores model training, quantization, and running inference on a microcontroller.

## Features
- Train a neural network to approximate the sin function.
- Export and convert the model to **TensorFlow Lite** format.
- Explore **quantization** for deployment on resource-constrained devices.
- Run inference directly on **Arduino Nano BLE Sense 33**.

## Technologies
- **Python** & **TensorFlow**: for model training and conversion.
- **TensorFlow Lite (TFLite)**: for microcontroller-friendly model deployment.
- **C++ / Arduino IDE**: for running inference on Arduino.

## Getting Started

### Prerequisites
- Arduino IDE (or PlatformIO) installed.
- Arduino Nano BLE Sense 33 board.
- Python 3.x with TensorFlow installed.

### Installation & Usage

1. **Train the model and convert** (optional, pre-trained TFLite model can be used):
create_sine_model.ipynb

23. **Load the model onto Arduino**:
   - Export `.tflite` to `.cc` using ```bash xxd -i sine_model_quantized.tflite > sine_model_quantized.cc```
   - Include the `.cc` file in your Arduino project.
   - Use the **Arduino_TensorFlowLite** library to run inference.

## Notes
- Input and output quantization parameters may affect the model’s accuracy.
- This project is an **introductory TinyML example** and can be extended to more complex functions.

## License
MIT License

