# image_inpainting_using_GroundingDINO_SAM_and_StableDiffusion
Image_inpainting_using_GroundingDINO_SAM_and_StableDiffusion

<img alt="BC" src="https://developer-blogs.nvidia.com/wp-content/uploads/2024/01/ces-stable-diffusion-featured.jpg" width='500'  align='center'/>

<!-- ABOUT THE PROJECT -->
## About The Project
<b>In this project. Firstly, we used GroundingDINO for detecting a bounding box that we want to segment using via a prompt that we write, 
and then using Segment- Anything model, we created a segment from this bounding box. Finally, we inpainted this segmment via a stable diffusion prompt.</b>

The steps of the project are as follows:

- <b> 1)Feature Extraction (Grounding DINO):</b>

  +Grounding DINO is utilized for feature extraction. In this stage, the deep learning-based model Grounding DINO extracts significant features from the image. Additionally, it assists in separating objects and background by being combined with the Segment Anything (SA) method. This stage provides a fundamental guide for inpainting by determining the positions and classes of objects.

- <b> 2)Object Segmentation (Segment Anything):</b>

  +Segment Anything performs object segmentation on the image. This is achieved by utilizing the features obtained by Grounding DINO. Object segmentation delineates the boundaries and contours of objects, providing a basic framework for the inpainting process.

- <b> 3)Identification of Missing Regions:</b>

  +Subsequently, the missing regions to be filled for inpainting are identified. This is typically done through masking or marking the missing regions. This step determines where the inpainting algorithm should focus.

- <b> 4)Filling in Missing Regions (Stable Diffusion):</b>

  +Stable Diffusion is employed for filling in the missing regions. In this stage, using the object segments obtained from Segment Anything, the colors and patterns of the pixels surrounding the missing regions are calculated. Then, the Stable Diffusion algorithm intelligently fills in the missing regions based on this information. This process ensures that the filled regions are consistent with the surrounding pixels, resulting in a natural appearance.

### Built With

* ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
* ![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
* ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
* ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
