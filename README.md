# gaze-and-tell

A from-scratch recreation of **"Show, Attend and Tell: Neural Image Caption Generation with Visual Attention"** — a model that looks at an image and writes a caption for it, one word at a time, while paying attention to different parts of the image as it goes. You can actually see where the model is "looking" at each step, shown as a heatmap over the image.

This project is inspired by the original 2015 paper by Kelvin Xu, Jimmy Ba, Ryan Kiros, and others — a collaboration between the University of Toronto and Université de Montréal. It was one of the first papers to bring visual attention into image captioning, and it helped lay the groundwork for the attention mechanisms used in today's language models.

---

## About the paper

- **Title:** Show, Attend and Tell: Neural Image Caption Generation with Visual Attention
- **Authors:** Kelvin Xu, Jimmy Ba, Ryan Kiros, Kyunghyun Cho, Aaron Courville, Ruslan Salakhutdinov, Richard Zemel, Yoshua Bengio
- **Year:** 2015
- **Paper:** [arXiv:1502.03044](https://arxiv.org/abs/1502.03044)

The model combines a CNN (to understand the image) with an RNN (to generate the caption), plus an attention mechanism that lets the model focus on different regions of the image as it writes each word.

## What this project does

- Implements the encoder-decoder-with-attention architecture from scratch
- Trains on the Flickr8k dataset
- Generates captions for new images
- Visualizes attention as a heatmap over the image for each generated word
- Compares soft attention vs. hard attention (the two variants from the paper)

## Project structure (not confirmed)

```
gaze-and-tell/
├── data/                  # dataset + preprocessing scripts
├── models/                # encoder, decoder, attention modules
├── notebooks/             # exploration and training notebooks (Colab-friendly)
├── outputs/                # sample captions + attention visualizations
├── train.py
├── evaluate.py
├── requirements.txt
└── README.md
```

## Setup

```bash
git clone https://github.com/<your-username>/gaze-and-tell.git
cd gaze-and-tell
pip install -r requirements.txt
```

## Dataset

This project uses the **Flickr8k** dataset (8,000 images, 5 captions each).

Download instructions and preprocessing steps are in `data/README.md`.

## Training

```bash
python train.py --config configs/soft_attention.yaml
```

## Results

| Model | BLEU-4 | Notes |
|---|---|---|
| Soft Attention | TBD | |
| Hard Attention | TBD | |

Sample output:

> *(caption + attention heatmap example goes here once training is done)*

## What's different from the original

- Implemented independently from the paper, using existing public implementations only as a reference for debugging, not as source code
- Trained on a smaller scale (Flickr8k instead of MS COCO) to fit university project constraints
- Added [your extra angle here — e.g. modern CNN backbone, extra ablations, failure case analysis]

## Acknowledgements and Credits

Inspired by the original paper by Xu et al. (2015) and the University of Toronto / Vector Institute research community. This is an independent educational reproduction, not affiliated with the original authors.

