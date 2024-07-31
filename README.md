# Image-Similarity-using-Simple-Structural-Features

## Overview

The repository is designed for evaluating image similarity and constructing graph representations from image features. It includes methods for detecting edges, corners, lines, curves, and smooth regions in images, as well as comparing them using similarity scores. It contains code for comparing images using various quality metrics and graph matching algorithms. It provides functionalities to calculate similarity metrics such as SSIM, PSNR, RMSE, and ISSM, and perform graph matching using graph edit distance and optimal assignment algorithms. 

## Features

- **Resize and Preprocess Images** : Resize images and optionally convert them to grayscale.
- **Divide Images into Patches**: Split images into non-overlapping patches for detailed analysis.
- **Feature Detection**: Detect edges, corners, lines, curves, and smooth regions in image patches.
- **Similarity Calculation**: Calculate the similarity between images based on detected features.
- **Graph Visualization**: Visualize image features as graphs and compare them using the Hungarian algorithm.
- **Image Visualization**: Display images and detected features (edges, corners, lines, curves, smooth regions).
- **Image Quality Metrics**:
  - **SSIM (Structural Similarity Index)**: Measures similarity between two images.
  - **PSNR (Peak Signal-to-Noise Ratio)**: Evaluates image quality based on compression.
  - **RMSE (Root Mean Square Error)**: Quantifies the difference between two images.
  - **ISSM (Image Similarity and Structure Measure)**: Combines entropy and edge differences for image comparison.

- **Graph-Based Image Analysis**:
  - **Graph Construction**: Converts images into graphs by dividing them into non-overlapping patches based on simple structural features.
  - **Graph Matching**: Computes graph edit distance and optimal assignment for comparing image graphs.

## Requirements

- Python 3.x
- NumPy
- OpenCV
- Matplotlib
- scikit-image
- NetworkX
- Pandas
- Pillow

## Installation

Ensure you have Python installed. Install the required libraries using `pip`:

```sh
pip install opencv-python numpy tqdm matplotlib pandas pillow networkx scipy scikit-image
```

## Data

- **Dataset**: Images should be organized in a directory structure where each folder contains images belonging to a category. Metadata is stored in `Dataset.csv`. Other folders are used for the purpose of testing.

- **Example**:
  ```
  ./Dataset.csv
  ./two
  ./three
  ./Test
  ./dataset/
  ├── dew/
  │   ├── image1.jpg
  │   └── image2.jpg
  └── fogsmog/
      ├── image1.jpg
      └── image2.jpg
  ```

## Notes

- The graph matching algorithm may require tuning of parameters based on specific use cases.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- This work utilizes various libraries for image processing and graph analysis, including OpenCV, Matplotlib, scikit-image, and NetworkX.
