# Image-Processing

A set of 10 Jupyter notebooks covering core digital image processing techniques, implemented in Python with NumPy and OpenCV. Every notebook is self-contained: the input image is generated in code (gradient + shapes + light texture), so there are no external image files to download or upload.

> **Credit:** the assignment structure and algorithms come from a friend's original `Image_Processing` notebooks. This version was refactored (clearer names, comments and formatting, generated demo image, no `input()` prompts / `cv2.imshow`) and re-tested.

## Assignments

| # | Topic | What the notebook does |
|---|-------|------------------------|
| 1 | Grayscale to binary | Thresholds a grayscale image using (a) its mean intensity and (b) a user-set threshold. |
| 2 | Colour to grayscale | Converts RGB to gray by (a) averaging R, G, B and (b) user-defined channel weights that must sum to 1. |
| 3 | Borders and complements | Adds a constant-colour border with `cv2.copyMakeBorder`; computes grayscale and binary complements (negatives). |
| 4 | Intensity transformations | Log transform, power-law (gamma) transform and piecewise-linear contrast stretching, all with explicit pixel loops. |
| 5 | Histogram processing | Histogram equalization using the normalised CDF, and histogram matching to a reference image. |
| 6 | Spatial filtering | Hand-written 2-D filtering with averaging, weighted and Gaussian kernels, with zero or replicate padding. |
| 7 | Image sharpening | Laplacian sharpening, Sobel and Canny edge-based sharpening, and unsharp masking. |
| 8 | Noise models | Uniform, Gaussian, Erlang, Exponential and Rayleigh noise, each derived manually and via NumPy, with histograms and noisy images. |
| 9 | LBP and denoising | Local Binary Pattern texture map; Wiener, Median, Gaussian and Bilateral filters on Gaussian and speckle noise. |
| 10 | Adaptive median and Otsu | Adaptive median filter vs. standard median on salt-and-pepper noise (compared by PSNR); Otsu thresholding implemented from scratch. |

## Technologies

- Python 3.9+
- NumPy
- OpenCV (`opencv-python`)
- Matplotlib
- SciPy (Wiener filter in Assignment 9)
- Jupyter Notebook

## Installation

```bash
git clone https://github.com/<your-username>/Image-Processing.git
cd Image-Processing

# optional but recommended
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

pip install -r requirements.txt
```

## Running the notebooks

### Jupyter Notebook

```bash
jupyter notebook
```

Open any `Assignment-N.ipynb` and choose **Run > Run All Cells**.

### Google Colab

1. Go to <https://colab.research.google.com> and choose **File > Upload notebook** (or open it straight from GitHub via the *GitHub* tab).
2. Run all cells. NumPy, OpenCV, Matplotlib and SciPy are already available in Colab, so nothing needs installing.

## Notes

- Settings that were previously typed in with `input()` (threshold, gamma, kernel size, window sizes, etc.) are now variables at the top of the relevant cell. Edit them and re-run.
- Random noise uses a fixed seed, so results are reproducible.
- Assignments 4, 6, 9 and 10 use explicit pixel loops on purpose (to show the algorithm); the demo image is 128x128 so they finish in seconds.

## Dependencies

See [`requirements.txt`](requirements.txt): `numpy`, `opencv-python`, `matplotlib`, `scipy`, `notebook`.
