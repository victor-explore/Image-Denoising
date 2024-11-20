# Image Denoising Project

This repository contains implementations of various image denoising techniques using Python. The project explores different approaches to remove noise from images while preserving important details.

## Table of Contents
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Methods](#methods)
- [Results](#results)
- [Dependencies](#dependencies)

## Installation

```bash
git clone https://github.com/yourusername/image-denoising.git
cd image-denoising
pip install -r requirements.txt
```

## Project Structure

```
├── src/
│   ├── part1_gaussian_filter.py
│   ├── part2_mmse_filter.py
│   └── part3_wavelet_transform.py
├── data/
│   └── lighthouse2.bmp
├── results/
├── requirements.txt
└── README.md
```

## Usage

```python
# Example usage
from src.part1_gaussian_filter import denoise_gaussian
from src.part2_mmse_filter import denoise_mmse
from src.part3_wavelet_transform import denoise_wavelet

# Load and process image
img = load_image('data/lighthouse2.bmp')
denoised_img = denoise_gaussian(img)
```

## Methods

### 1. Gaussian Filter
- Implementation of low-pass Gaussian filtering
- Optimal filter parameter selection using MSE

### 2. MMSE Filter
- High-pass domain transformation
- Patch-based processing
- Adaptive MMSE filtering

### 3. Wavelet Transform
- Discrete Wavelet Transform (DWT) decomposition
- SURE shrinkage threshold estimation
- Patch-based denoising

## Results

The project includes three different denoising approaches:
- Gaussian filtering achieved MSE: X
- MMSE filtering achieved MSE: Y
- Wavelet transform achieved MSE: Z

## Dependencies

- NumPy
- Matplotlib
- SciPy
- scikit-image
- PyWavelets

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
