# Fourier Spectral Imaging with Modular Frequency Filtration

## Project Overview
This project explores Fourier Spectral Imaging techniques by implementing modular frequency filtration on images. Using graph-based representations of images, the project applies spectral filtering to extract high-frequency and low-frequency components, demonstrating their effects on image features.

### Key Features
- **Graph Representation of Images:** Represents image pixel intensity as a graph, defining edges based on pixel similarity.
- **Graph Laplacian Computation:** Constructs the Laplacian matrix to capture graph structure.
- **Spectral Decomposition:** Computes eigenvalues and eigenvectors to transform image data into the spectral domain.
- **Frequency Filtering:** Applies high-pass and low-pass filters to emphasize or suppress image features.

## Installation
### Prerequisites
- Python 3.7+
- Required Python libraries:
  - `numpy`
  - `matplotlib`
  - `scipy`

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/vidyut-veedgav/Fourier-Spectral-Imaging.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Fourier-Spectral-Imaging
   ```
3. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
### Running the Code
1. Place your input image in the `images` directory.
2. Modify the script to specify the input image path and desired filter settings (e.g., `tau` for frequency threshold).
3. Run the script:
   ```bash
   python spectral_filtering.py
   ```
4. View the filtered images, which will be saved in the `outputs` directory.

### Parameters
- **`tau`:** Threshold value used to separate high and low frequencies. Adjust `tau` to modify the filtering effect.
- **High-Pass Filtering:** Emphasizes high-frequency regions, such as edges and fine details.
- **Low-Pass Filtering:** Emphasizes low-frequency regions, such as broad structures and gradients.

## Examples
### Input Image
![Input Image](images/sample_input.png)

### High-Pass Filtered Output
![High-Pass Output](outputs/high_pass_sample.png)

### Low-Pass Filtered Output
![Low-Pass Output](outputs/low_pass_sample.png)

## Project Structure
```
Fourier-Spectral-Imaging/
├── images/               # Input image files
├── outputs/              # Filtered output images
├── spectral_filtering.py # Main script
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

## Theory and Methodology
1. **Graph Representation:**
   - Pixels are treated as nodes, and edges are defined based on pixel intensity similarity.
2. **Graph Laplacian:**
   - Diagonal entries represent node degree, while off-diagonal entries represent edge weights.
3. **Spectral Domain Transformation:**
   - Eigenvectors of the Laplacian serve as basis functions for the graph.
   - Transforming data into the spectral domain reveals frequency-specific components.
4. **Filtering:**
   - Filters are applied by modifying the spectral coefficients using a diagonal matrix `H`.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-branch-name
   ```
3. Commit your changes and push to your fork.
4. Submit a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For questions or feedback, please contact [Vidyut Veedgav](https://github.com/vidyut-veedgav).


