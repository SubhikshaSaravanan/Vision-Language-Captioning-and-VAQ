# Multimodal Vision-Language System for Image Captioning, Storytelling, and VQA

This repository contains the implementation of a modular, transformer-based system for image captioning, visual storytelling, and visual question answering (VQA). The system leverages Vision Transformers (ViT) and BLIP for multimodal generation tasks and includes multilingual support for captioning. A Gradio interface is provided for real-time interaction.

## Features

- Multilingual image captioning (supports English, Hindi, French, Spanish, Mandarin)
- Story generation based on visual content
- Visual question answering (VQA) from natural language queries
- Gradio-based web interface for user interaction
- Modular design built using PyTorch and Hugging Face Transformers

## Dataset

The system is designed around the Flickr30K dataset. Users can choose one of the following options:

1. Automatically download a compressed version using kagglehub (recommended for memory-constrained environments like Google Colab).
2. Download all 30,000 images locally if sufficient memory and storage are available.

## Dependencies


Required Python libraries include:

- kagglehub
- os
- pandas
- glob
- PIL (Pillow)
- matplotlib
- torchvision
- transformers
- torch
- concurrent.futures
- csv
- scikit-learn

Transformer models used:

- ViTForImageClassification
- ViTModel
- ViTFeatureExtractor
- BlipProcessor
- BlipForConditionalGeneration
- AutoTokenizer
- MarianMTModel
- MarianTokenizer
- pipeline

## Model Overview

- ViT (Vision Transformer): Used for extracting visual features from input images.
- BLIP (Bootstrapped Language Image Pretraining): Used for captioning, storytelling, and VQA.
- MarianMT: Used for translating generated captions into supported languages.

## Gradio Interface

The system includes a user interface built with Gradio, allowing real-time interaction with the models. Users can:

- Upload an image
- Select a task: captioning, storytelling, or VQA
- Choose a target language for translation (if captioning)
- Input a question (if VQA)
- View the generated output directly in the browser

## How to Run

This project can be executed in environments such as Google Colab, Jupyter Notebook, or locally using VSCode with a Python environment.

Steps to run:

1. Clone the repository:

2. Open the .ipynb notebook file in Jupyter or Colab.

3. Install required dependencies (see list above).

4. Choose dataset option:
- Use kagglehub to download images
- Or place manually downloaded images in a flickr30k_images directory

5. Run all cells in the notebook to:
- Load the models
- Preprocess images
- Generate outputs based on user interaction

## Evaluation

Basic token-level evaluation is included using the following metrics:

- Precision
- Recall
- F1-score

Note: Evaluation shown in the notebook is for a representative sample and should not be interpreted as a full model benchmark.

## Project Notes

- GPU is highly recommended for inference due to model size
- MarianMT models require internet access during the first run to download language models
- Ensure the CSV file (image_captions.csv) and images are accessible at the expected paths

## Possible Extensions

- Add batch inference for processing large sets of images
- Improve multilingual translation quality with fine-tuned models
- Introduce external knowledge sources for better VQA
- Expand language coverage beyond the current supported options

## License

This project is released under the MIT License.

## Acknowledgements

- Hugging Face Transformers
- Flickr30K Dataset on Kaggle
- Salesforce BLIP Model
- Google ViT Model



