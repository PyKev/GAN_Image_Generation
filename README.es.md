# Generador de Imágenes MNIST mediante GANs

Este repositorio presenta una implementación de un Generative Adversarial Network (GAN) para la generación de imágenes en el estilo del conjunto de datos MNIST.

## Requisitos

- Python
- TensorFlow
- NumPy
- Matplotlib

## Uso

1. Clonar este repositorio en tu entorno local.
2. Asegurarse de contar con los paquetes requeridos.
3. Ejecutar el archivo `GAN.ipynb` para entrenar el GAN y generar imágenes.

## Arquitectura

El GAN está compuesto por dos componentes principales:

### Generador

- Emplea una red neuronal convolucional (CNN).
- Transforma un espacio latente de ruido en imágenes realistas.
- Utiliza capas convolucionales transpuestas para aumentar la resolución.

### Discriminador

- Se basa en una red neuronal convolucional (CNN).
- Realiza la tarea de clasificación binaria: imágenes reales o generadas.
- Ayuda a refinar el rendimiento del generador mediante retroalimentación.

## Entrenamiento

El entrenamiento del GAN sigue una estrategia de competencia entre el generador y el discriminador:

1. El generador crea imágenes falsas a partir de ruido aleatorio.
2. El discriminador se entrena para distinguir imágenes reales de las generadas.
3. Se alternan ciclos de entrenamiento para ambos componentes.
4. Las pérdidas se ajustan con función de entropía cruzada binaria.

## Resultados

Después de un número determinado de épocas de entrenamiento, el generador es capaz de producir imágenes que se asemejan a los dígitos manuscritos del conjunto de datos MNIST.
