# pokedex-ai - computer vision pokemon classifier

An end-to-end machine learning project that identifies the original 151 Pokémon using computer vision and deep learning. Built as a learning exercise with plans for deployment on a Raspberry Pi.


## Project Goal

Create a physical Pokédex that works like in the Pokémon anime: point a camera at a Pokémon (drawing, figure, card) and get its name and information instantly.


## Technical Approach

- **Task**: Multi-class image classification (150 classes)
- **Model**: MobileNetV2 with transfer learning
- **Framework**: PyTorch + torchvision
- **Dataset**: 30-50 images per Pokémon (~6,000 total images)
  - Dataset originally from Lance Zhang available at https://www.kaggle.com/datasets/lantian773030/pokemonclassification
- **Data Pipeline**: Custom preprocessing with augmentation (random flips, rotations, color jitter)
- **Training Strategy**: Fine-tuning with unfrozen final convolutional layers


## Results

- **Validation Accuracy**: 91.8%
- **Test Accuracy**: 91.4%
- **Training Time**: ~10 epochs on CPU

The model generalizes well with minimal overfitting, achieving consistent performance across validation and test sets.


## Tech Stack

- Python 3.12
- PyTorch
- torchvision
- Pillow (image processing)
- scikit-learn (metrics)
- matplotlib (visualization)
- tqdm (progress tracking)


## Next Steps

- Expand to all Pokemon generations (800+ Pokémon)
- Convert model to TorchScript/ONNX for deployment
- Integrate with Raspberry Pi + camera module
- Assemble electronics (screen, battery, buttons)
- Build physical case and UI


---

*Gotta classify 'em all!* 
