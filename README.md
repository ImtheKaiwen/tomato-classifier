# Tomato Classifier

An experimental image-classification training script built with TensorFlow and Keras. It defines a convolutional neural network, applies image augmentation, trains with a validation split, and saves the resulting model as `trained1.h5`.

## Repository contents

```text
.
├── app.py       # Data loading, model definition, training, and model export
└── README.md
```

## Dataset requirement

The dataset is not included. `app.py` expects a local `data/` directory in the folder structure used by Keras `flow_from_directory`, with one subdirectory per class:

```text
data/
├── class-a/
│   └── image-files...
└── class-b/
    └── image-files...
```

The script resizes images to 224×224 pixels and reserves 20% of the available images for validation.

## Run the experiment

Use a Python environment with compatible TensorFlow and Keras versions, place the dataset under `data/`, and then run:

```bash
python app.py
```

This command starts model training for up to 40 epochs and may require substantial compute time. Early stopping monitors validation loss.

## Reproducibility status

This repository does not currently record dependency versions, the dataset source, class definitions, or benchmark results. Training was therefore not executed during the documentation refresh, and no accuracy claim is made.
