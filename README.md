# Canny, Hough Transform & High-Boost Filter

This repository contains my complete solutions to three fundamental image processing assignments implemented in Python. The exercises focus on edge detection, line extraction, and image sharpening using classical algorithms and OpenCV.
For more info please read the question document provided as `Ex03_IP_Edge&Resolution.pdf` .

---

##  Exercise 1: Canny Edge Detector (From Scratch + OpenCV)

**Goal:** Implement the full 5-step Canny algorithm manually and compare with `cv2.Canny`.

###  Steps Implemented:
- Grayscale conversion
- Gaussian smoothing
- Gradient calculation (Sobel)
- Non-maximum suppression
- Double thresholding + hysteresis

###  Key Learnings:
- Effect of `sigma` on noise reduction vs. edge preservation
- Importance of proper low/high thresholds
- Manual hysteresis tracking is tricky but rewarding

---

## Exercise 2: High‑Boost Filter Combined with Sobel

**Goal:** Sharpen blurred images while preserving edges using a hybrid approach.

###  Features:
- Gaussian blur to create low-pass version
- Sobel for edge map
- Adjustable boost factor `A` and blend coefficient `α`

### Effect of α:
| α = 0 (pure HB) | α = 0.6 (balanced) | α = 1 (pure Sobel) |
|----------------|--------------------|---------------------|
| Sharp but noisy | Best structure + edges | Only edges, no sharpening |

## What I Learned

- Manual implementation of Canny teaches edge detection internals
- Hough accumulator visualization demystifies line voting
- High‑Boost + Sobel combination avoids oversharpening artifacts
- Parameter tuning is an essential skill — no one‑size‑fits‑all

---

## Exercise 3: Hough Transform Line Detection

**Goal:** Detect structural lines (roof, walls) from `hill.png` using Canny + Hough Transform.

### Implementation:
- Canny for edge extraction
- Probabilistic Hough Line Transform (`cv2.HoughLinesP`)
- Visualization of accumulator space (peaks = lines)
- Parameter tuning to reject texture noise


###  Analysis Covered:
- Effect of Hough threshold on line count
- How noisy Canny edges pollute the accumulator space
- Optimal parameter selection for `hill.png`




