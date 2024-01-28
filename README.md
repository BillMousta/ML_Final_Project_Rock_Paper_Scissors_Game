# ML_Final_Project_Rock_Paper_Scissors_Game

# Introduction
In the culminating project for our Machine Learning course, we were tasked with developing a machine learning agent to compete in the classic game of Rock-Paper-Scissors against a randomly playing opponent. The objective was to design an intelligent agent capable of recognizing the opponent's move and strategically countering it to secure a win. To achieve this, we employed a neural network model to empower our agent's decision-making capabilities, pitting it against an opponent that makes random choices

# Agent Model
Our CNN model for the Rock-Paper-Scissors game is designed with the following key layers:

**Convolutional Layers:**

* First Layer: 32 filters (3x3).
* Second Layer: 64 filters (3x3).
* Activation: ReLU (Rectified Linear Unit) for introducing non-linearity.
  
**Max Pooling Layers:**

* Pool Size: 2x2, reducing spatial dimensions and computational load.
  
**Flatten Layer:**

Converts pooled feature maps into a single vector, serving as input to the dense layers.

**Dense Layers:**
* One dense layer with 128 neurons.
* Output layer with 3 neurons (for rock, paper, scissors) using softmax activation.

### Model Advantages
* **Feature Learning:** Efficiently learns spatial features from images, crucial for distinguishing hand signs.
* **Parameter Efficiency:** Fewer parameters due to shared weights, enhancing performance.
* **Robustness:** Handles spatial variations effectively, ideal for recognizing hand signs irrespective of their positioning.
This architecture is tailored for the task of recognizing and classifying hand signs in the Rock-Paper-Scissors game, leveraging CNN's strengths in image processing and pattern recognition.

# Model Training and Validation

Our model is trained and validated on the Rock-Paper-Scissors dataset sourced from Kaggle: https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors:
* **Resizing:** Images are reshaped to 32x32 to reduce model complexity.
* **Color Transformation:** RGB images are converted to grayscale.
* **Normalization:** Pixel values are normalized to the [0, 1] range by dividing each pixel by 255.

# Game Simulation
Our agent competes against a "Random Agent" in a series of N rounds in the Rock-Paper-Scissors game.

* **Betting Mechanism:** Each round involves a bet of €1.
* **Winning:** If our agent wins, it earns €2.
* **Tie:** In a tie, the agent gets a refund of €1.
* **Losing:** If our agent loses, it forfeits €1.

### Random Agent Strategy
* **Image Selection:** Randomly chooses from 2100 images (rock, paper, or scissors).
* **Image Manipulation:**
  * Applies a vertical flip with a 50% probability.
  * Applies a horizontal flip with a 50% probability.
  * Adds random noise to each pixel (mean 0, standard deviation 5% of the maximum pixel value).

# Model's Performance on test set
![image](https://github.com/BillMousta/ML_Final_Project_Rock_Paper_Scissors_Game/assets/45403400/a0faf32a-8235-4089-abcd-035ec9e197f4)

# Conclusion
Our AI Agent for the Rock-Paper-Scissors game showcases the capabilities of machine learning in both strategic gameplay and image recognition. It excels in handling our current dataset; however, enhancing its adaptability to a wider range of real-world situations is an objective we are actively pursuing. Keep an eye out for future developments and enhancements
