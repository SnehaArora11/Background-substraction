---

# Background Subtraction using Gaussian Mixture Models (GMM)

This project implements a custom Gaussian Mixture Model (GMM) for background subtraction in images and videos. GMM is a probabilistic model that represents a mixture of multiple Gaussian distributions, commonly used for modeling pixel distributions in background subtraction tasks.

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [References](#references)

## Project Overview

This implementation focuses on using a GMM for background subtraction in visual data. The primary steps include:

1. **Building the GMM Class**: Implements GMM from scratch with methods for initialization, expectation-maximization (E-step and M-step), and prediction.
2. **Video Frame Processing**: Helper functions to display video frames or save them to a file, enabling analysis and visualization of GMM-based background subtraction.
3. **Application to Background Subtraction**: Uses pixel distributions modeled by GMM to separate foreground (moving objects) from the background.

## Installation

To run this project, you will need the following dependencies:

```bash
pip install numpy matplotlib opencv-python
```

## Usage

1. **Implement the GMM**:
   - The `GMM` class provided in `Background Subtraction.ipynb` contains methods for GMM-based background subtraction.
   
2. **Run the Notebook**:
   - Execute the notebook to fit the GMM model to visual data. The notebook includes:
     - Class definitions for the GMM.
     - Helper functions for frame display and saving.
   
3. **Display and Save Frames**:
   - The helper functions `display_frames` and `save_frames` help visualize and save the background subtraction results.

### Sample Commands
```python
# Instantiate and fit GMM
gmm = GMM(n_components=3, tol=1e-4, max_iter=100)
gmm.fit(data)

# Display results as video
display_frames(frames, fps=10)

# Save results
save_frames(frames, fps=10, output_path='./results', file_name='background_subtraction_result')
```

## Project Structure

```
Background Substraction.ipynb   # Main notebook with GMM implementation and example usage
README.md                       # Project README file
```

## Results

Example output showing background subtraction results using GMM and averaging:

[Background Subtraction Results - Frame Averaging](foreground_avg.mp4)  
[Background Subtraction Results - GMM](foreground%20GMM.mp4)


## References

- [Gaussian Mixture Models - scikit-learn](https://scikit-learn.org/stable/modules/mixture.html)
- [Understanding GMMs - YouTube Video 1](https://youtu.be/qMTuMa86NzU)
- [Introduction to GMMs - YouTube Video 2](https://youtu.be/ZBLyXgjBx3Q)

--- 
