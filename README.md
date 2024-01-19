# Landmark Classification & Tagging for Social Media 2.0

## Project Overview
Photo sharing and photo storage services like to have location data for each photo that is uploaded. With the location data, these services can build advanced features, such as automatic suggestion of relevant tags or automatic photo organization, which help provide a compelling user experience. Although a photo's location can often be obtained by looking at the photo's metadata, many photos uploaded to these services will not have location metadata available. This can happen when, for example, the camera capturing the picture does not have GPS or if a photo's metadata is scrubbed due to privacy concerns.

If no location metadata for an image is available, one way to infer the location is to detect and classify a discernible landmark in the image. Given the large number of landmarks across the world and the immense volume of images that are uploaded to photo sharing services, using human judgment to classify these landmarks would not be feasible.

In this project, we take the first steps towards addressing this problem by building models to automatically predict the location of the image based on any landmarks depicted in the image.
 
The project goes through the machine learning design process end-to-end: performing data preprocessing, designing and training CNNs, and comparing the accuracy of different CNNs

<img alt="Examples from the landmarks dataset - a road in Death Valley, the Brooklyn Bridge, and the Eiffel Tower" src="https://video.udacity-data.com/topher/2021/February/602dac82_landmarks-example/landmarks-example.png" class="chakra-image css-mvsohj"> *Examples from the landmarks dataset - a road in Death Valley, the Brooklyn Bridge, and the Eiffel Tower*

## Project Steps
### 1- Training a CNN model from scratch
A Convolutional Neural Network (CNN) is created to classify landmarks, with a focus on visualizing the dataset, preparing it for training, and building the network from scratch. Emphasis is placed on the decision-making process regarding data processing and network architecture. The best network is then exported using Torch Script.

corresponding Jupyter Notebook: [cnn_from_scratch.ipynb](cnn_from_scratch.ipynb)

**Try installing the notebook if it gives an error in the GitHub viewer. It seems like a common issue. Maybe it happens due to some elements in the notebook**
### 2- Using transfer learning
A CNN is established for landmark classification using Transfer Learning. Different pre-trained models are explored, and a specific model is chosen for the classification task. The process includes training and testing the transfer-learned network, accompanied by an explanation of the decision-making behind selecting the pre-trained network. The optimal transfer learning solution is exported using Torch Script.

corresponding Jupyter Notebook: [transfer_learning.ipynb](transfer_learning.ipynb)

## How to navigate the project

### `src` folder
`src` folder contains a file for each function implementation along with its test cases. 

### The Jupyter Notebooks
The Jupyter Notebooks contain the basic structure of the project with the code to call and run all the functions together but without the actual implementation of each function.   

## Getting Started

1. **Clone This repository**

2. **Navigate to the repo Directory:**
   - Open a terminal and navigate to the directory where you installed the starter kit.

3. **Download and Install Miniconda:**
   - Follow the [Miniconda installation instructions](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) relevant to your operating system.

4. **Create a New Conda Environment:**
   - Open a terminal and run the following commands:
     ```bash
     conda create --name landmark python=3.7.6 pytorch=1.11.0 torchvision torchaudio cudatoolkit -c pytorch
     ```

5. **Activate the Environment:**
   - Run the following command:
     ```bash
     conda activate landmark
     ```
   **Note:** You will need to activate your environment every time you open a new terminal.

6. **Install Required Packages:**
   - Run the following command:
     ```bash
     pip install -r requirements.txt
     ```

7. **Test GPU Availability:**
   - Execute the following command (only if you have an NVIDIA GPU on your machine with proper Nvidia drivers installed):
     ```bash
     python -c "import torch;print(torch.cuda.is_available())"
     ```
     This should return `True`. If it returns `False`, your GPU cannot be recognized by PyTorch. Test with `nvidia-smi` to check if your GPU is working. If not, check your NVIDIA drivers. If you encounter difficulties, consider using the Project Workspace instead of working locally.

8. **Install and Open Jupyter Lab:**
   - Run the following commands:
     ```bash
     pip install jupyterlab
     jupyter lab
     ```
## This was the third project of the "Udacity Machine Learning Fundamentals Nandegree" offered by AWS as part of the "AWS AI & ML scholarship"
Confirmation  link: [link](https://graduation.udacity.com/confirm/e/ba2b0610-ee8f-11ed-8e43-fbdc25fcc49f)
![Certificate](https://github.com/Kshishtawy/Developing-a-Handwritten-Digits-Classifier-with-PyTorch/blob/main/Certificate/Udacity%20-%20Machine%20Learning%20Fundamentals.png?raw=true)
