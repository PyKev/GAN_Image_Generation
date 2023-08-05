# MNIST Image Generator using GANs

This repository presents an implementation of a Generative Adversarial Network (GAN) for generating images in the style of the MNIST dataset.

## Requirements

- Python
- TensorFlow
- NumPy
- Matplotlib

## Usage

1. Clone this repository into your local environment.
2. Ensure you have the required packages.
3. Run the `GAN.ipynb` file to train the GAN and generate images.

## Architecture

The GAN consists of two main components:

### Generator

- Utilizes a Convolutional Neural Network (CNN).
- Transforms a latent noise space into realistic images.
- Employs transpose convolutional layers to increase resolution.

### Discriminator

- Based on a Convolutional Neural Network (CNN).
- Performs binary classification task: real or generated images.
- Helps refine the generator's performance through feedback.

## Training

GAN training follows a competition strategy between the generator and discriminator:

1. The generator creates fake images from random noise.
2. The discriminator is trained to distinguish real images from generated ones.
3. Training cycles alternate between both components.
4. Losses are adjusted using binary cross-entropy function.

## Results

After a specified number of training epochs, the generator is capable of producing images resembling handwritten digits from the MNIST dataset.
