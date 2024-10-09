# CS585: Semantic Segmentation Assignment

This repository contains the code and resources for the CS585 Semantic Segmentation assignment completed in Spring 2024. The assignment focused on implementing a Fully Convolutional Network (FCN) for semantic segmentation based on the architecture introduced in the paper: [Fully Convolutional Networks for Semantic Segmentation](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf) by Long et al., 2015.

## Project Structure

```bash
├── fcn_dataset.ipynb      # Notebook for dataset exploration and testing
├── fcn_dataset.py         # Python script for dataset loading and preprocessing (implemented)
├── fcn_model.py           # Python script for defining the FCN model architecture (implemented)
├── train.py               # Python script for training the FCN model (implemented)
├── job_script             # Example script to submit an SCC batch job
├── scc_quick_setup_guide.txt # Guide to set up SCC environment
├── README.md              # Project README (this file)
├── CamVid                 # Folder containing CamVid dataset (not included here)
├── image_vis.png          # Sample visualization of input image
├── label_vis.png          # Sample visualization of ground truth label
```

## Instructions

The goal of this assignment was to implement and train a semantic segmentation model using the Fully Convolutional Networks (FCN) architecture. Below are the key tasks completed:

1. **Data Loading and Preprocessing**:
   - Implemented in `fcn_dataset.py`
   - The script loads images and their corresponding labels, applies transformations, and prepares data for training.
   - Example visualizations are included (`image_vis.png`, `label_vis.png`).

2. **Model Architecture**:
   - Implemented in `fcn_model.py`
   - This script defines the FCN model architecture, based on the FCN-8s with a VGG backbone.

3. **Training Script**:
   - Implemented in `train.py`
   - The script sets up the training loop, including the loss function, optimizer (Adam with learning rate 0.001), and evaluation metrics (mIoU, pixel accuracy).
   - The model was trained for 50 epochs with a batch size of 16 and a resolution of 512x384.

4. **Job Script**:
   - `job_script` provides an example of how to submit the training job to the SCC (Shared Computing Cluster) environment.

## Results

- The model reached a minimum intersection over union (mIoU) of 22\% on the validation set.
- Performance was further improved to an mIoU of 27\% through hyperparameter tuning.

## Installation and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/CS585-SemanticSegmentation.git
   cd CS585-SemanticSegmentation
   ```

2. Set up the environment:
   - Follow the instructions in `scc_quick_setup_guide.txt` to set up the SCC environment.

3. Run the training:
   ```bash
   python train.py
   ```

## Visualization

The repository includes a visualization tool to generate predictions and compare them to ground truth. Example images can be found in `image_vis.png` and `label_vis.png`.


## References

- [Fully Convolutional Networks for Semantic Segmentation](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf) by Long et al., 2015.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
