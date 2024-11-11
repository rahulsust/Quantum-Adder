### Quantum Noise Model and Draper Adder Analysis
This project explores the effects of noise on quantum circuits, specifically focusing on a quantum addition circuit implemented using the Draper adder algorithm. Using custom functions to model quantum noise with probabilistic Pauli errors, we analyze how different noise levels affect the fidelity and accuracy of quantum addition. The project is implemented in a chosen quantum framework (e.g., Qiskit or Cirq) and culminates in a notebook that visualizes and interprets the results.

#### Project Structure
##### Noise Model:

  We define a function to introduce noise in the quantum circuit by applying Pauli errors (random X, Y, Z rotations) based on a specified probability after each gate. The noise model distinguishes between single-qubit and two-qubit gates, allowing for flexible control over noise intensity for each type of gate.
###### Parameters:
    alpha: Probability of adding noise after single-qubit gates.
    beta: Probability of adding noise after two-qubit gates.
#### Gate Basis Transformation:

  To align with typical quantum hardware constraints, the project includes a function that transforms any general quantum circuit into a restricted gate basis (e.g., {CX, ID, RZ, SX, X}).
  This transformation standardizes the circuit to ensure compatibility with available quantum hardware and helps us analyze the effects of basis restriction on noise and fidelity.
#### Quantum Addition with Draper Adder:

  The core quantum operation implemented is addition, performed by the Draper adder algorithm. This algorithm utilizes the Quantum Fourier Transform (QFT), which we implemented manually for educational purposes.
The quantum_sum function simulates quantum addition and serves as the basis for the noise analysis.
Noise Analysis and Results:

We analyze how different noise levels (alpha and beta) affect the fidelity and accuracy of the quantum addition results.
Using fidelity as a benchmark, the notebook assesses the accuracy of the quantum adder under varying noise levels and discusses potential strategies for noise mitigation.
Additional analyses include the impact of gate count on cumulative noise and the effects of transforming circuits to restricted gate bases.
#### Key Questions Explored
- How does noise affect the results of quantum addition?
- Is there a way to reduce the effect of noise on the results?
- How does the number of gates in a circuit impact noise accumulation?
#### Dependencies
Qiskit used For building and running quantum circuits.
NumPy: For probability handling and random selection.
#### How to Use
Install the required dependencies.
Run the notebook to see the implementation and analysis. The notebook includes:
Noise model setup
Draper adder implementation with QFT
Fidelity analysis of quantum addition under varying noise conditions
#### Future Directions
Implement error-correction codes to mitigate noise.
Explore optimized gate sets that reduce the impact of basis transformations.
Implement the KAK decomposition.
Extend the noise model to include realistic device-specific noise profiles.
This project provides insights into the effects of noise in quantum computing, with practical implications for implementing error-resilient quantum algorithms.
