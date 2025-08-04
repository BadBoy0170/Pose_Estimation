
# Multi-Modal Fusion for Real-Time Pose Estimation Setup & Inference Guide

This guide explains how to set up and run a multi-modal fusion technique for real-time pose estimation. It combines 2D and 3D images to predict all the joints in the human body, unlocking a wide range of applications in computer vision.

---

## Steps to Set Up the Pose Estimation

### **Step 1: Clone the Repository**

To begin, download the repository. You can do this by either cloning it using Git or downloading the files manually.

#### **Option 1: Clone using Git**

Run the following command in your terminal to clone the repository into your working directory:

```bash
git clone https://github.com/BadBoy0170/Pose_Estimation.git
```

#### **Option 2: Download Files Directly**

Download the necessary files from the repository, including the required weights for pose estimation.

---

### **Step 2: Create and Activate a Conda Environment**

Using a dedicated Conda environment ensures that the dependencies are isolated and do not interfere with other projects.

1. **Create the Conda environment** using the provided `environment.yml` file:
   ```bash
   conda env create -f environment.yml
   ```

2. **Activate the Conda environment**:
   ```bash
   conda activate posefusion
   ```

---

### **Step 3: Navigate to the Project Directory**

After activating the Conda environment, navigate to the directory containing the project files:

```bash
cd Pose_Estimation
```

---

### **Step 4: Download the Pre-trained Weights**

The pose estimation model requires pre-trained weights to perform inference.

1. **Download the pose weights**:  
   Visit [this link](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-w6-pose.pt) and download the `yolov7-w6-pose.pt` file.

2. **Alternatively, download using the terminal (Ubuntu)**:
   ```bash
   wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-w6-pose.pt
   ```

3. Place the `yolov7-w6-pose.pt` file in the `Pose_Estimation` directory where other project files are located.

---

### **Step 5: Run Pose Estimation Inference**

With everything set up, you can now run the pose estimation model. Below are different methods for running inference based on your requirements:

#### **1. Real-Time Inference Using Webcam**

To use a webcam as the input source (source `0`):

```bash
python run_pose.py --source 0
```

#### **2. Inference on a Video File**

To perform pose estimation on a specific video file, provide the path to the video:

```bash
python run_pose.py --source [path_to_video]
```

#### **3. Inference on GPU for Better Performance**

If you have a GPU available, specify the GPU device (default `0`) for faster processing:

```bash
python run_pose.py --source 0 --device 0
```

After running the commands, the model will process the input and display pose estimation results, including the keypoints detected on the human body.

---

By following this guide, you will have the multi-modal fusion pose estimation fully set up and running. This enables you to incorporate advanced pose estimation capabilities into your computer vision projects.

---

