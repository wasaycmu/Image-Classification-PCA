# Image-Classification-PCA

# Sports Image Classification 
## Technologies and Techniques Used

- **Languages & Libraries**: Python, Pandas, NumPy, Matplotlib, PIL (Pillow), Scikit-learn, Plotly
- **Image Processing**: Grayscale conversion, resizing, flattening to 1D vectors
- **Data Handling**: CSV parsing, NumPy arrays for memory efficiency
- **Dimensionality Reduction**: Principal Component Analysis (PCA)
- **Visualization**: Matplotlib for static graphs, Plotly for interactive explained variance charts

---

## Project Overview

### Objective

This project explores image data classification using a dataset of sports images sourced from Kaggle:
https://www.kaggle.com/datasets/sidharkal/sports-image-classification

The primary task is to classify sports images (e.g., tennis, swimming, soccer, etc.) using a machine learning pipeline involving preprocessing, PCA-based dimensionality reduction, and visualization.

### Dataset Details

- **Total Images**: 8227
- **Image Types**: JPEG
- **Average Size**: ~140x100 pixels (resized to 150x100 for processing)
- **Labels**: Cricket, Wrestling, Tennis, Badminton, Soccer, Swimming, Karate

---

## Applications

### 1. Medical Memory Training
A memory training tool for Alzheimer’s patients. Correct identification reinforces memory through recognition tasks involving familiar sports.

**Required Accuracy**: 95% minimum – High precision is critical to prevent memory confusion in clinical settings.

### 2. Sports Discovery & Booking App
Automatically identify sports in a broadcast and let users find local venues to play or attend similar events.

**Required Accuracy**: ~70–80% – Flexibility is acceptable since users interested in one sport may also enjoy similar alternatives.

### 3. Enterprise Image Filtering
Organizations like MLB can scan thousands of images for marketing, analysis, or content generation by filtering for relevant sports.

---

## Data Preparation Workflow

1. **Loading & Labeling**: Read image metadata and labels using Pandas.
2. **Previewing**: Randomly sample and display images to confirm integrity.
3. **Dimension Analysis**: Histogram of image resolutions to standardize resizing.
4. **Grayscale Conversion**: Reduces noise and improves PCA performance.
5. **Image Resizing**: Standardized to 150x100 (aspect ratio ~3:2) for performance and consistency.
6. **Flattening**: Each image reshaped into a 1D vector (15,000 pixels).

---

## Feature Extraction and Storage

- Flattened grayscale images saved as `.csv` to bypass expensive reprocessing.
- Image features and labels are stored separately to allow flexibility in model training.

---

## Principal Component Analysis (PCA)

### Goals
- Reduce 15,000-dimensional image vectors to a manageable feature set
- Preserve >99% variance with minimal components (≈3000)

### Analysis
- Explained variance plotted to determine optimal number of components
- Eigenimages (principal components) visualized to understand feature abstraction
- Image reconstruction from reduced features demonstrated successfully

---

## Notes & Limitations

- **Memory Constraints**: Full dataset takes hours to process into memory with naive methods — CSV caching and NumPy arrays mitigate this.
- **Performance Tradeoffs**: Grayscale and resizing reduce fidelity but enable practical modeling.
- **Scalability**: Current pipeline supports reloading processed data, facilitating quick experimentation without recomputation.

---

## License

Dataset is licensed under Open Data Commons Attribution License (ODC-By) v1.0.
