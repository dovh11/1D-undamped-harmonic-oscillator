
# Physics-Informed Neural Networks (PINNs) for 1D Undamped Harmonic Oscillator

## 📌 Overview

<img width="954" height="328" alt="image" src="https://github.com/user-attachments/assets/efbea6a3-9a5b-4d13-9981-7fe28b560ec7" />


This repository contains the implementation of a Physics-Informed Neural Network (PINN) designed to simulate and predict the dynamics of a 1D ideal, undamped spring-mass system (Simple Harmonic Oscillator).

Instead of relying purely on data-driven approaches or traditional numerical solvers (like Runge-Kutta), this model embeds physical laws—specifically **Newton's Second Law** and **Hooke's Law**—directly into the neural network's loss function. This forces the network to learn solutions that strictly adhere to the underlying physics, ensuring long-term energy conservation and high-fidelity predictions.

## ✨ Features

-   **Physics-Driven Loss Function:** The custom loss function penalizes the network not only for data mismatch but also for violating the governing ordinary differential equation (ODE): $m \frac{d^2x}{dt^2} + kx = 0$.
    
-   **Energy Conservation:** Demonstrates the PINN's ability to maintain zero energy dissipation over extended time domains, characteristic of an undamped system.
    
-   **Analytical Validation:** Automatically compares the neural network's predictions against the exact analytical sinusoidal solution $x(t) = A \cos(\omega t + \phi)$ to calculate absolute errors.
    
-   **Phase-Space Visualization:** Utilizes Matplotlib to plot kinematic trajectories (Position vs. Velocity) and loss convergence graphs for robust model evaluation.
    

## 🛠️ Technologies Used

-   **Language:** Python 3.x
    
-   **Deep Learning Framework:** PyTorch
    
-   **Data & Math Libraries:** NumPy, SciPy
    
-   **Visualization:** Matplotlib, Seaborn
    

## 🚀 How to Run

1.  Clone this repository to your local machine:
    
    ```
    git clone [https://github.com/dovh11/1D-undamped-harmonic-oscillator.git](https://github.com/dovh11/1D-undamped-harmonic-oscillator.git)
    
    ```
    
2.  Navigate to the project directory:
    
    ```
    cd 1D-undamped-harmonic-oscillator
    
    ```
    
3.  Install the required dependencies:
    
    ```
    pip install torch numpy matplotlib
    
    ```
    
4.  Run the main simulation script:
    
    ```
    python3 1D_harmonic_oscillator.ipynb
    
    ```
    

## 📊 Expected Outputs

Upon running the script, the model will train the PINN and generate visualizations showcasing:

1.  **Prediction vs. Exact Solution:** A time-series plot overlaying the PINN's predicted position/velocity with the analytical truth.
    
2.  **Loss History:** A graph demonstrating the convergence of both the Data Loss and the Physics (ODE) Loss.
    
3.  **Phase-Space Portrait:** A cyclic trajectory plotting velocity against position, confirming the periodic and conservative nature of the modeled system.
    

## 📚 References

-   Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations. _Journal of Computational Physics_, 378, 686-707.
    

_Developed by Vu Huy Do - Exploring the intersection of Deep Learning and Classical Mechanics._
