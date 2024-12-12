# *Very Low Exposure Simulator*

## *Overview*
The *Very Low Exposure Simulator* leverages Monte Carlo simulations to model and analyze images taken under extremely low light conditions. This tool aims to explore how minimal light exposure affects image resolution and signal-to-noise ratio (SNR). It offers a computational framework to simulate photon distribution in imaging scenarios with limited lighting, providing insights into low-light imaging systems.

## *Features*
- **Bulk Processing**: Efficiently handles large sets of luminance distribution images.
- **Monte Carlo Simulation**: Models low-light environments using stochastic photon distributions.
- **Image Preprocessing**: Normalizes and adjusts images for low-light simulations.
- **Customizable Settings**: Provides flexibility with photon counts and image resolutions for tailored simulations.
- **YOLOv9 Integration**: Utilizes YOLOv9 for object detection on simulated low-exposure images.

## *Motivation*
- Simulate images captured in very low exposure settings.
- Investigate how low exposure impacts image quality, specifically resolution and SNR.
- Assess the performance of neural networks under low-light conditions.

## *Objectives*
- Generate low-exposure images based on luminance distributions using Monte Carlo simulations.
- Estimate the minimum lighting required for object detection in autonomous driving environments.
- Examine the effects of photon distribution on image resolution and SNR.

## *Methodology*

### 1. *Define Simulation Parameters*
- **Array Size**: Start with an initial image size (e.g., 64x64) and update based on the final dimensions.
- **Photon Count**: Adjust the number of photons to balance accuracy with computation time.

### 2. *Image Preprocessing*
- **Normalize Image**: Scale pixel intensities to a range between 0 and 1.
- **Adjust Array Size**: Ensure the array size matches the final image dimensions.

### 3. *Monte Carlo Simulation*
- **Initialization**: Set up an array initialized with zeros for the simulated image.
- **Simulation Loop**:
  - Randomly sample pixel coordinates.
  - Retrieve pixel intensity to estimate photon detection probability.
  - Simulate photon detection using random number generation.

### 4. *Postprocessing and Visualization*
- Generate low-exposure images with noise that simulates the characteristics of low-light conditions.
- Display the original and simulated images side-by-side for easy comparison.

### 5. *Results Analysis*
- Compare resolution and SNR across various photon counts and lighting conditions.
- Analyze the impact of exposure parameters like F-Stop, ISO, and exposure time on quanta per pixel.

## *Results*
The simulator provides detailed analysis based on:
- Photon counts ranging from 10,000 to 100,000,000.
- The impact of ISO settings and exposure times on SNR and resolution.
- Visualizations of low-light image characteristics.

## *Requirements*
- Python (latest version)
- Required libraries:
  - **NumPy**
  - **OpenCV**
  - **Matplotlib**
  - **YOLOv5** (with pre-trained weights for object detection)

