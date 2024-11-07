CS5787 HW4 Deep Learning with Prof. Hadar Elor - Sean Hardesty Lewis (shl225)
# DDPM for Image Generation

## Contents
- `HW4_Notebook_P3.ipynb`: Forward diffusion process visualization
- `HW4_Notebook_P4.ipynb`: Efficiency of DDIM (Denoising Diffusion Implicit Models)
- `HW4_Notebook_P5.ipynb`: Generative applications of diffusion models with prompt-to-prompt manipulations (Google)

## Notebook P3: Forward Diffusion Process
In this notebook, we implement the forward diffusion process using PyTorch. We start with clean images and progressively corrupt them by adding Gaussian noise based on a variance schedule.

### Implementation
- Loading 5 clean images
- Implementing Gaussian noise addition according to variance schedule βₜ
- Visualizing and quantifying corruption over time steps: 0, 10, 50, 100, 500

### Visualization
![P3_Chart](https://github.com/user-attachments/assets/d69244ac-f20d-4620-8338-429a98aab49c)

## Notebook P4: Denoising Diffusion Implicit Models (DDIM)
We explore DDIM, a model that accelerates the diffusion process from 1000 steps to as few as 50 without significant loss in image quality.

### Implementation
- Comparing image outputs at different sampling steps: 100, 50, 10 (and extras I added)
- Using a pre-trained CIFAR-10 model from the DDIM repository

### Results
![P4_Chart_All](https://github.com/user-attachments/assets/3272ba6b-8c14-481d-9e34-145f19d7e9e0)

## Notebook P5: Generative Applications with Google's Prompt-to-Prompt
We manipulate images using the prompt-to-prompt technique, demonstrating the power of text-driven image manipulation.

### Examples
- From "A painting of a squirrel eating a burger" to "A painting of a lion eating a burger"
- From "A photo of a house on a mountain" to "A photo of a house on a mountain in winter"

### Discussion
The prompt-to-prompt method allows precise image adjustments through simple text changes, though it sometimes struggles with complex interactions and abstract concepts.

### Example Outputs
![P5_Chart1](https://github.com/user-attachments/assets/bdef5e8e-e2ea-4f30-9cd6-22db77aeaaa9)
![P5_Chart2](https://github.com/user-attachments/assets/bc5c9b0a-281e-4b43-8bc3-d31306247bd9)

## Analysis and Conclusion

The three projects within the Jupyter notebooks showcase the potential and limitations of diffusion models in image processing. Each project targets a unique aspect of diffusion modeling, demonstrating practical applications and uncovering areas for improvement.

**Project 1: Forward Diffusion Process** - We explored how Gaussian noise incrementally corrupts image clarity over time, demonstrating the forward diffusion process's ability to simulate data deterioration. The quantification of image corruption through mean squared error illustrated the impact of noise and highlighted challenges in controlling image quality during the diffusion process.

**Project 2: Efficiency of DDIM** - The DDIM project illustrated the model's efficiency by reducing the number of diffusion steps required, significantly speeding up the process without severely compromising image quality. However, the reduced steps showed a noticeable trade-off in detail and color accuracy, suggesting a need for optimization between speed and fidelity.

**Project 3: Generative Applications with Google's Prompt-to-Prompt** - This project leveraged a prompt-based diffusion model to manipulate images, revealing the model's capability to adapt to specific textual instructions and maintain stylistic consistency. While effective in straightforward scenarios, the model struggled with complex interactions and finer details, pointing to opportunities for refining the understanding and generation of nuanced visual content.

These projects highlight a few capabilities and constraints of diffusion models, providing insights into efficiency, quality management, and varying interpretation of prompts. These findings lay the groundwork for future enhancements in model precision and efficiency.

## References

1. **Denoising Diffusion Probabilistic Models**  
   Jonathan Ho, Ajay Jain, Pieter Abbeel.  
   *arXiv preprint arXiv:2006.11239*, 2020.  
   
   [arXiv:2006.11239](https://arxiv.org/abs/2006.11239)

2. **Denoising Diffusion Implicit Models**  
   Jiaming Song, Chenlin Meng, Stefano Ermon.  
   *arXiv preprint arXiv:2010.02502*, 2020.  
   
   [arXiv:2010.02502](https://arxiv.org/abs/2010.02502)

3. **Prompt-to-Prompt Image Editing with Cross Attention Control**  
   Amir Hertz, Ron Mokady, Jay Tenenbaum, Kfir Aberman, Yael Pritch, Daniel Cohen-Or.  
   *arXiv preprint arXiv:2208.01626*, 2022.  
   
   [arXiv:2208.01626](https://arxiv.org/abs/2208.01626)




