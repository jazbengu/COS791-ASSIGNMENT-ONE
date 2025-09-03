📸 Image Enhancement using Genetic Algorithm and Variable Neighbourhood Search

This project implements and compares two metaheuristic optimization algorithms—Genetic Algorithm (GA) and Variable Neighbourhood Search (VNS)—to automate the enhancement of grayscale images. The goal is to discover optimal sequences (pipelines) of image processing techniques that improve image quality, evaluated using a fitness function combining PSNR, SSIM, and MSE.

📁 Code Structure

The code is organized in a Jupyter notebook with the following structure:

Cell	Functionality
1	Setup and Dependencies: Mounts Google Drive and installs required libraries (
2	Imports: All necessary libraries for image processing, optimization, and handling
3	extract_images: Loads and separates input/ground truth images from a folder
4	Image Enhancement Techniques: Implements Gamma Correction, Gaussian Blur, Unsharp Masking, Histogram Equalization, and Contrast Stretching
5	technique_dict: Dictionary of all enhancement techniques and their parameters
6	ran_pipeline: Generates a random image enhancement pipeline
7	image_to_pipeline: Applies a pipeline to an image
8	fitness_function: Scores pipeline quality based on PSNR, SSIM, and MSE
9	random_population: Generates an initial random population for GA
10	select_parents: Tournament selection for GA parents
11	crossover: Creates new pipelines from parent pipelines
12	mutation: Applies mutation in GA and VNS
13	genetic_algorithm: Main loop for the GA optimization process
14	vns_shake: Shaking step in VNS
15	vns_local_search: Local search step in VNS
16	variable_neighbourhood_search: Main loop for VNS optimization
17	test_pipelines: Evaluates best pipelines on test images
18	show_images: Visual comparison of original, ground truth, and enhanced images
19	indi_meterics: Calculates individual MSE, PSNR, SSIM metrics (not in main flow)
20	results_table: Summarizes results in a DataFrame
21	Main Execution: Loads data, runs GA & VNS, evaluates results, shows plots and tables
🚀 Setup and Usage
📂 Prerequisites

Use Google Colab (recommended)

Mount your Google Drive at /content/drive

Organize your data as follows:

/content/drive/MyDrive/COS791-ASSIGNMENT-ONE-DATA/
├── Training_data/
│   └── train_data/
└── Test_data/
    └── Test_data/


Ensure ground truth images contain _gt in the filename.

▶️ Running the Project

Mount Drive
Run the first cell to mount your Google Drive.

Install Dependencies
The notebook auto-installs any missing libraries.

Prepare Data
Place your training and testing images in the correct folders.

Execute Notebook
Run each cell in order.

View Results
The final section displays:

Best GA and VNS pipelines

Convergence plot

Test set metrics

Side-by-side image comparisons

Results summary table

📊 Results
✅ Output Includes:

Convergence Plot
Shows improvement in fitness score over generations (GA) and epochs (VNS)

Best Pipelines
List of enhancement techniques and parameters used

Test Metrics

MSE (Mean Squared Error)

PSNR (Peak Signal-to-Noise Ratio)

SSIM (Structural Similarity Index)

Visual Comparisons
Original vs Ground Truth vs Enhanced (GA & VNS)

Summary Table
Average metrics comparing GA and VNS performance

🏁 Conclusion

This project demonstrates how metaheuristic optimization techniques can automate and improve grayscale image enhancement. Results indicate that:

Genetic Algorithm (GA) consistently achieved:

Higher fitness scores during training

Lower MSE

Higher PSNR and SSIM on test images

Thus, GA outperformed VNS in this task, producing higher-quality enhancements for unseen data.


Explore other metaheuristics (e.g., Particle Swarm Optimization, Simulated Annealing)

Optimize runtime and scalability
