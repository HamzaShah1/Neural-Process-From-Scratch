# README
This is a project to research and showcase my learning of neural networks. 

This README goes through the background learning process i went through, and then the final product i built <ins>**[insert explanation]**</ins>

## Background Knowledge 
- Firstly, i brushged up my knowledge on Deep Neural Networks and Tensor Data Processing 
- Then, the process of **automatic differentiation** in **PyTorch**
- Softmax regression was an interesting and necessary topic to learn;
- The next step up from there was to learn about **Linear Regression** & **Multi Layer Perceptions (MLPs)** 
- Then after covering **Convolutional Neural Networks**, i was set to start this project.

### Some interesting resources
Here are some resources i found interesting and helpful to the creation of this project.
- [PyTorch in 100 seconds](https://www.youtube.com/watch?v=ORMx45xqWkA) by Fireship — quick orientation
- [What are Neural Processes?]() Just a quick little search on YouTube
- [Neural Networks](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) playlist by 3Blue1Brown, best intuition for MLPs, no maths required
- [PyTorch Tutorial for Beginners](https://www.youtube.com/playlist?list=PLqnslRFeH2UrcDBWF5mfPGpqQDSta6VK4) by Patrick Loeber — practical coding side
- [PyTorch in 1 Hour](https://www.youtube.com/watch?v=r1bquDz5GGA)

## Building Process
- Step 1 — Set Up Google Colab
- Step 2 — Build the Model
    - **Encoder: Input** (one x,y pair) &rarr; a couple hidden layers &rarr; **Output** (r vector)
    - Take the average of all r vectors from N observed points into one r_O
    - **Decoder: Input** (concatentate r_O with an x_t value) &rarr; few hidden layers (same hidden dim) &rarr; **Output:** a single predicted y value
- Step 3 — Write the **Training Loop**
    - **Loss Function** (Use **MSE** - Mean Squared Error) &rarr; **Optimiser** (Adam) &rarr; <ins>during each training step randomly sample N observed points from each function to create context, then output remaining points</ins>
- Step 4 — Train All 3 Models
    - Train Models 2, 4, and 8. Keeping everything the same but <ins>Changing the **r_dim**</ins>
- Step 5 — Analysis
    - Anal;ysis of plotting r_dim vs test error
    - Computing a correlation matrix of the latent dimensions