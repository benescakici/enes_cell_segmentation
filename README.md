# Cell Segmentation Demo

Cell and nuclei segmentation on the BBBC018 dataset using CellPose pretrained models.

## Dataset

The data is located in the `data/` folder:
- **Images**: `BBBC018_v1_images/` - 3-channel DIB files (DNA, actin, pH3)
- **Ground Truth**: `BBBC018_v1_outlines/` - PNG mask files (nuclei and cells)

Source: [Broad Bioimage Benchmark Collection (BBBC018)](https://bbbc.broadinstitute.org/)

## Quick Start

### 1. Create a Virtual Environment

**Using venv (Python 3.9+):**
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

**Using conda:**
```bash
conda create -n cell-seg python=3.10
conda activate cell-seg
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Demo

```bash
cd notebooks
jupyter notebook cell_segmentation_demo.ipynb
```

## Project Structure

```
├── data/                          # Dataset folder
│   ├── BBBC018_v1_images/        # Input images
│   └── BBBC018_v1_outlines/      # Ground truth masks
├── notebooks/
│   └── cell_segmentation_demo.ipynb   # Main demo notebook
├── scripts/                       # Utility scripts
├── models/                        # Trained/pretrained models
├── requirements.txt               # Python dependencies
└── README.md
```

## Notebooks

- **cell_segmentation_demo.ipynb**: Main demo showing:
  - Data loading and visualization
  - CellPose model predictions
  - Evaluation metrics (IoU, Dice)
  - Comparison with ground truth

## Requirements

- Python 3.9 or higher
- All dependencies listed in `requirements.txt`
- ~2GB disk space for model downloads (CellPose)
- Optional: GPU support (CUDA/cuDNN for faster inference)

## Reproducibility

All dependencies are pinned in `requirements.txt` to ensure reproducible results across different systems and users. The same Python version (3.9+) is recommended.