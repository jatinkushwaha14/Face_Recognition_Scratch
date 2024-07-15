# Face Detection and Localization with VGG16 and Custom Layers

This project involves using the VGG16 pre-trained model as a base and adding custom layers to perform face detection and bounding box localization. The project includes data augmentation, custom loss functions, and saving/loading model weights.

## Project Structure

- `model2.0.ipynb`: Jupyter notebook containing the implementation of the model and training process.
- `compressed/`: Directory containing images.
- `labelesscompressed/`: Directory containing images with no face.
- `label/`: Directory containing JSON files with bounding box annotations for each image.
- `vgg16_weights.weights.h5`: Pre-saved VGG16 weights file.

## Setup Instructions

### Prerequisites

- Python 3.7 or higher
- TensorFlow 2.x
- OpenCV
- Albumentations
- NumPy
- JSON

## Data Augmentation

Data augmentation is performed using Albumentations. The augmentation pipeline includes random resized cropping, horizontal and vertical flips, random brightness/contrast adjustment, random gamma adjustment, and RGB shifts. The bounding box parameters are handled to ensure the bounding box remains valid after augmentation.

## Custom Loss Function

A custom loss function is used for bounding box localization, which calculates the difference between the predicted and true coordinates and sizes of the bounding boxes.

## Additional Notes

	•	Ensure that the image paths and JSON annotation paths are correctly specified in the code.
	•	Adjust the data augmentation parameters as needed based on the dataset and desired augmentation effects.
	•	Ensure the virtual environment is activated before running the training script to use the correct package versions.

## Side Note

Due to computational constraints, the model may not perform very well. Further training and optimization on more powerful hardware might be necessary to achieve better performance.
