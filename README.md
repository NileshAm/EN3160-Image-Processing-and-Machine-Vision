# EN3160 - Image Processing and Machine Vision

Assignment 1: **Intensity Transformations and Neighborhood Filtering**

Python implementations of ten image processing exercises, with visual comparisons, histograms, and numerical evaluations in a Jupyter notebook.

**Index number:** 230038E

## Repository contents

| File or folder | Description |
| --- | --- |
| [main.ipynb](main.ipynb) | Notebook containing the implementations, explanations, and saved outputs for Questions 1-10. |
| [main.html](main.html) | HTML export of the notebook; download and open it in a browser to view the results. |
| [230038E_a01.pdf](230038E_a01.pdf) | Assignment PDF. |
| [Images/](Images/) | Input images used by the exercises. |

## Exercises

| Question | Topics covered |
| --- | --- |
| 1 | Piecewise linear intensity transformations on a grayscale image. |
| 2 | Histogram analysis and intensity transformations to highlight brain tissue regions. |
| 3 | Gamma correction on the lightness channel in Lab color space. |
| 4 | Vibrance enhancement by transforming saturation in HSV color space. |
| 5 | Manual histogram equalization using a cumulative distribution function. |
| 6 | Foreground separation using saturation and enhancement of the foreground value channel. |
| 7 | Sobel gradients using OpenCV, manual spatial filtering, and separable kernels. |
| 8 | Manual nearest-neighbor and bilinear interpolation, compared using normalized squared differences. |
| 9 | GrabCut foreground segmentation and Gaussian background blurring. |
| 10 | Gaussian and bilateral filtering, including a manual bilateral filter compared with OpenCV. |

## Setup and execution

Use **Python 3.12 or newer**. The notebook records Python 3.12.8, and Question 8 uses f-string syntax that requires Python 3.12 or later.

From the repository root, create a virtual environment:

```sh
python -m venv .venv
```

Activate it using the command for your shell:

- Windows PowerShell: `.\.venv\Scripts\Activate.ps1`
- Windows Command Prompt: `.venv\Scripts\activate.bat`
- macOS/Linux: `source .venv/bin/activate`

Install the notebook dependencies and launch JupyterLab:

```sh
python -m pip install --upgrade pip
python -m pip install numpy opencv-python matplotlib pandas jupyterlab
python -m jupyterlab
```

Open `main.ipynb`, select the environment's Python kernel, and run the cells from top to bottom. Keep the notebook alongside `Images/`: image paths are relative to the repository root. The OpenCV installation must provide `cv.IMREAD_COLOR_RGB`, which several exercises use.

The manual filtering and interpolation implementations use pixel-by-pixel loops, so some cells may take longer to run than their OpenCV equivalents. To inspect the saved results without executing the code, view the notebook on GitHub or download and open `main.html` locally.
