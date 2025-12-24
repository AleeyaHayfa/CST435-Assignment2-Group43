# CST435-Assignment2-Group43
This assignment implements a parallel image processing pipeline in Python using multiprocessing and concurrent.futures. It applies multiple filters to a subset of the Food-101 dataset and is deployed on Google Cloud Platform (GCP). Performance is evaluated using execution time, speedup, and efficiency metrics.

## Multiprocessing Implementation
The project utilizes Python's multiprocessing module, specifically the Pool class, to parallelize image processing tasks. Images from the Food-101(100 images) dataset are processed in parallel across multiple processes.

### Key Features:
- Parallel Processing: Uses multiprocessing.Pool to distribute image processing tasks across available CPU cores.
- Filters Applied: Each image undergoes a series of filters:
  - Grayscale conversion
  - Gaussian blur
  - Sobel edge detection
  - Sharpening
  - Brightness adjustment (factor 1.2)
- Process Counts Tested: Experiments are run with 1, 2, and 4 processes to evaluate performance.

This setup allows for efficient processing of large image datasets by leveraging multiple CPU cores.

## Machine Configuration
The experiments were conducted on the following GCP machine configuration:
- Machine Type: e2-standard-4 (4 vCPUs, 16 GB memory)

