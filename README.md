Task 1: Image Reading and Visualization
Objective

To understand how digital images are stored, loaded, and visualized in a computer system.

Step-by-Step Explanation

Image Upload and Reading

An image is uploaded into the Colab environment.

OpenCV is used to read the image in BGR format.

The reason OpenCV reads images in BGR instead of RGB is due to historical memory alignment optimizations.

Color to Grayscale Conversion

The image is converted into grayscale using weighted intensity conversion.

This reduces computational complexity and is useful for many image processing tasks such as segmentation and edge detection.

Visualization

The original color image and grayscale image are displayed using Matplotlib.

Color conversion is applied before visualization to ensure correct color display.

Image Properties Analysis

Image shape explains resolution and number of channels.

Data type shows how pixel values are stored (usually uint8).

Sample pixel values help in understanding intensity distribution.

Outcome

Clear understanding of image structure, pixel representation, and color models.

Visualization of both color and grayscale images.

Task 2: Connected Component Labeling
Objective

To detect, label, and count distinct objects in a binary image.

Step-by-Step Explanation

Grayscale Conversion

Converts the image into a single intensity channel to simplify thresholding.

Otsu’s Thresholding

Automatically determines the optimal threshold value by minimizing intra-class variance.

Produces a binary image separating foreground from background.

Noise Removal

Morphological opening (erosion followed by dilation) removes small unwanted noise.

This improves object detection accuracy.

Connected Component Labeling

Each connected region is assigned a unique label.

Components smaller than a predefined area threshold are discarded.

Visualization

Binary image, cleaned image, and color-labeled components are displayed.

Outcome

Accurate object detection and counting.

Visual distinction between different connected components.

Task 3: Histogram Equalization and Contrast Stretching
Objective

To improve image contrast using histogram-based enhancement techniques.

Step-by-Step Explanation

Grayscale Conversion

Histogram operations are simpler and more effective in grayscale images.

Built-in Histogram Equalization

Redistributes intensity values to span the full dynamic range.

Enhances global contrast.

Custom Histogram Equalization

Histogram and cumulative distribution function (CDF) are calculated manually.

Provides insight into how histogram equalization works internally.

Contrast Stretching

Linearly stretches intensity values between minimum and maximum pixel values.

Preserves relative intensity differences.

Comparison Display

Original and processed images are displayed side by side.

Outcome

Improved image visibility.

Conceptual understanding of histogram manipulation.

Task 4: Color Image Enhancement
Objective

To enhance color images while preserving natural color appearance.

Step-by-Step Explanation

Color Space Conversion (YCrCb)

Separates luminance from chrominance.

Histogram equalization is applied only on the luminance channel to avoid color distortion.

Manual Histogram Equalization

Demonstrates control over enhancement process.

Contrast Stretching

Improves dynamic range of color channels.

Logarithmic Transformation

Enhances darker regions while compressing bright regions.

Gamma Correction

Adjusts brightness non-linearly.

Useful for display and illumination correction.

Histogram Analysis

Histograms before and after enhancement are plotted.

Outcome

Multiple color enhancement results.

Better understanding of color models and intensity transformations.

Task 5: Image Filtering
Objective

To remove noise using spatial filtering techniques.

Step-by-Step Explanation

Mean Filter

Smooths image by averaging neighboring pixels.

Reduces Gaussian noise but blurs edges.

Median Filter

Replaces pixel with median of neighbors.

Highly effective for salt-and-pepper noise.

Mode Filter

Assigns the most frequent value in the neighborhood.

Useful for discrete noise patterns.

Gaussian Filter

Uses weighted averaging based on Gaussian distribution.

Preserves edges better than mean filtering.

Result Comparison

Original and filtered images are compared visually.

Outcome

Clear comparison of filtering techniques.

Understanding trade-offs between smoothing and edge preservation.

Task 8: Noise Addition and Restoration
Objective

To analyze the effect of noise and evaluate restoration techniques.

Step-by-Step Explanation

Noise Addition

Gaussian noise simulates sensor noise.

Salt & Pepper noise simulates transmission errors.

Motion blur simulates camera or object movement.

Restoration Techniques

Wiener filter minimizes mean square error.

Median filter removes impulse noise effectively.

Performance Evaluation

PSNR is calculated to quantitatively evaluate restoration quality.

Visualization

Original, noisy, and restored images are displayed.

Outcome

Understanding noise models and restoration strategies.

Quantitative and qualitative comparison using PSNR.

Task 9: Color Spaces, White Balance, and Segmentation
Objective

To explore different color representations and perform color-based segmentation.

Step-by-Step Explanation

Channel Splitting

RGB channels analyzed independently.

Color Space Conversion

HSV, YCbCr, and Lab color spaces explored for different properties.

Gray World White Balance

Assumes average scene color should be gray.

Corrects color casts.

Color-Based Segmentation

HSV masking isolates green objects.

Lab a-channel separates objects based on color distribution.

Outcome

Improved color consistency.

Effective color-based object segmentation.

Task 10: JPEG-like DCT Compression and Huffman Coding
Objective

To understand image compression principles used in JPEG.

Step-by-Step Explanation

Block Division

Image is divided into 8×8 blocks.

Discrete Cosine Transform (DCT)

Converts spatial information into frequency components.

Quantization

Reduces high-frequency components using JPEG quantization matrix.

Huffman Coding

Compresses data using variable-length coding.

Performance Metrics

Compression Ratio, MSE, PSNR, and Rate Distortion calculated.

Visualization

Difference image amplified to highlight compression loss.

Outcome

Practical understanding of lossy compression.

Analysis of quality vs compression trade-off.

Task 11: Morphological Operations
Objective

To analyze shapes and remove structural noise.

Step-by-Step Explanation

Binary Conversion

Image converted to binary for morphology.

Basic Operations

Erosion and dilation modify object boundaries.

Opening removes noise.

Closing fills gaps.

Advanced Operations

Boundary extraction highlights object edges.

Hole filling improves object completeness.

Shape Detection

Contours analyzed to detect triangles, rectangles, and circles.

Outcome

Clean binary images.

Successful detection and labeling of shapes.

Task 12: Thresholding and Segmentation
Objective

To segment images using intensity- and clustering-based methods.

Step-by-Step Explanation

Thresholding Techniques

Global thresholding uses fixed value.

Otsu’s method selects optimal threshold automatically.

Adaptive thresholding handles uneven illumination.

K-Means Segmentation

Clusters pixels based on intensity and color.

Tested with k = 2, 3, and 4.

Mean Shift Segmentation

Non-parametric clustering based on feature space.

Result Comparison

All segmentation results displayed together.

Outcome

Understanding strengths and weaknesses of segmentation methods.

Visual comparison of different techniques.
