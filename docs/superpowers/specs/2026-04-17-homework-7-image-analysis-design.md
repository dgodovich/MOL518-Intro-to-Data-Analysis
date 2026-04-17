# Homework 7 Design: Image Analysis (Lectures 31-33)

## Purpose

Design Homework 7 for `MOL518 Spring 2026` as a short image-analysis assignment that matches the level and style of earlier homeworks while drawing on material from `Lecture_31` through `Lecture_33`.

The homework should:

- focus mainly on image-processing mechanics rather than biological interpretation
- use a mix of shared repo images and student-generated images
- avoid directly copying the in-class exercises
- stay guided overall, with one more open-ended problem at the end
- be appropriate for a notebook-based submission

## Course Context

Students have already seen:

- arrays, indexing, slicing, plotting, loops, file handling, and functions
- basic statistics and fitting
- digital images as arrays
- image histograms, line profiles, thresholding, stacks, and projections from `Lecture_31`
- bit depth, noise, mean/median/Gaussian filtering, and background subtraction from `Lecture_32`
- Fourier transforms, affine transforms, cropping, resizing, decimation, and interpolation from `Lecture_33`

They have not been asked to build large software-style analyses. Existing homework style is guided, notebook-based, and broken into concrete subparts.

## Assignment Shape

Homework 7 will contain `3` problems.

- `Problem 1` uses the shared microscopy image from `Lecture_33`
- `Problem 2` uses a student-taken photo and Fourier-space filtering
- `Problem 3` uses a student-taken photo again for a small custom image-processing pipeline

This structure keeps the first half standardized for grading while still asking students to transfer methods to their own data.

## Problem 1: Inspecting and Cleaning the Mitosis Image

### Dataset

Use:

- `Lecture_33/media/microscopy_example.png`

### Learning Goals

- inspect an image as an array
- connect visual appearance to pixel-intensity distributions
- use line profiles as a targeted inspection tool
- compare noise-reduction methods

### Required Tasks

Students should:

1. load and display the image
2. report:
   - `shape`
   - `dtype`
   - minimum intensity
   - maximum intensity
   - total number of pixels
3. plot an intensity histogram
4. make one horizontal and one vertical line profile at locations they choose
5. briefly explain what the histogram and line profiles show
6. apply two denoising methods to the image
7. compare the original and filtered images side by side
8. briefly explain what changed after filtering

### Method Constraints

The denoising methods should be explicitly suggested so students know what is allowed. The prompt should name examples such as:

- Gaussian filtering
- median filtering

Students do not need to implement these filters from scratch.

### Why This Works

This problem uses the lecture image but does not simply repeat the in-class Fourier or interpolation exercises. It reinforces inspection habits and filtering mechanics from Lectures 31 and 32.

## Problem 2: Fourier-Space Filtering of Your Own Photo

### Dataset

Students take their own photo with a phone or other camera.

The homework should instruct them to choose an image with visible structure or texture so Fourier filtering produces a meaningful result.

### Learning Goals

- compute and visualize a 2D Fourier transform
- interpret the centered power spectrum
- apply a mask in Fourier space
- compare image content before and after inverse transforming

### Required Tasks

Students should:

1. take and load their own image
2. display the original color image and a grayscale version
3. compute the 2D Fourier transform of the grayscale image
4. display the centered power spectrum using `np.fft.fftshift`
5. construct a Fourier-space mask
6. apply the mask and reconstruct the filtered image with an inverse transform
7. show a comparison figure with:
   - original image
   - grayscale image
   - power spectrum
   - Fourier mask
   - filtered image
8. explain which visual features were suppressed or preserved

### Method Constraints

To keep the problem focused and gradeable, the prompt should constrain the filter choice to one of:

- low-pass
- high-pass
- notch filter, if the student sees a clear directional or periodic feature

### Why This Works

This transfers the Fourier material from lecture to a student-chosen image without requiring them to discover an advanced use case from scratch.

## Problem 3: Build a Small Image-Processing Pipeline

### Dataset

Use the same student-taken photo from Problem 2.

### Learning Goals

- choose image operations to accomplish a concrete goal
- think in terms of sequential transformations rather than isolated commands
- evaluate what each step contributes

### Required Tasks

Students should:

1. choose one image-processing goal for their photo
2. state the goal before showing code
3. build a pipeline with at least three operations
4. show intermediate outputs after each major step
5. justify why each step was included
6. show the final output
7. briefly assess what worked well and what did not

### Suggested Goal Menu

The prompt should provide concrete goal options such as:

- highlight edges
- isolate a foreground object from the background
- emphasize large-scale structure
- suppress fine texture
- make a repeated pattern easier to see

### Acceptable Operations

The prompt can explicitly mention operations such as:

- smoothing or denoising
- thresholding
- cropping
- resizing
- interpolation
- affine transforms
- Fourier filtering
- contrast adjustment

### Why This Works

This is the open-ended component, but it remains bounded. Students are not being asked for a full biological interpretation or a novel algorithm. They are being asked to assemble familiar tools into a short, purposeful workflow.

## Allowed Libraries and Functions

The homework should include a short note stating that students may use higher-level functions introduced or adjacent to the lectures, provided they say what they used.

Recommended allowed packages:

- `numpy`
- `matplotlib`
- `scipy.ndimage`
- `scipy.fft` or `numpy.fft`
- `skimage.filters`
- `skimage.transform`
- `cv2`

The prompt should explicitly state:

- students do not need to implement filters from scratch
- if they use a higher-level helper function, they should name it in their notebook

## Style and Difficulty Targets

- keep the assignment guided and concrete
- emphasize plotting and visual comparison
- require short written interpretation, but keep the center of gravity on mechanics
- avoid requiring a long report
- keep the scope reasonable for one homework notebook

## Expected Deliverable Structure

The eventual LaTeX homework should:

- match the formatting style of `Homework_1` and `Homework_2`
- ask students to submit a Jupyter notebook
- use problem titles and lettered subparts
- include short package guidance where appropriate

## Implementation Notes

When drafting the actual homework file:

- update `Homework_7/MOL518_HW2.tex` in place unless the file is renamed as part of cleanup
- rename notebook references so they say `HW7`, not `HW2`
- clearly distinguish the shared microscopy file from the student photo
- keep prompts specific enough that grading is consistent
