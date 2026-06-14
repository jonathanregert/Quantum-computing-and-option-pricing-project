# Quantum Call Option Pricing

This project shows how quantum computing can be used to approximate the price of a European call option.

The implementation uses **Qiskit** and is based on **Quantum Amplitude Estimation (QAE)**. The notebook builds the quantum pricing workflow step by step, from the financial model to the final payoff estimation.

## Project Description

A European call option gives its holder the right to buy an underlying asset at a fixed strike price. Its payoff at maturity is:

```text
max(S_T - K, 0)
```

where:

- `S_T` is the asset price at maturity;
- `K` is the strike price.

The goal of this project is to approximate the expected payoff of the option by encoding the problem into a quantum circuit.

## Main Steps

The notebook follows these main steps:

1. **Discretize the asset price distribution**
   
   The possible values of the asset price at maturity are represented on a finite grid.

2. **Build a probability distribution**
   
   The distribution of the underlying asset is approximated on this discrete grid.

3. **Encode probabilities into a quantum state**
   
   A quantum state is constructed so that the amplitudes represent the square roots of the probabilities.

4. **Encode the call payoff**
   
   The payoff function is approximated using controlled rotations.

5. **Apply Quantum Amplitude Estimation**
   
   QAE is used to estimate the probability associated with the payoff, which is then converted into an approximation of the option value.

## Technologies Used

- Python
- Qiskit
- NumPy
- Matplotlib
- Jupyter Notebook

## How to Run

Clone the repository:

```bash
git clone <repository-url>
cd <repository-name>
```

Install the required dependencies:

```bash
pip install qiskit numpy matplotlib
```

Open the notebook:

```bash
jupyter notebook pricing_project_english.ipynb
```

Then run the cells in order.

## Educational Purpose

This project is mainly educational. It is designed to illustrate how a financial pricing problem can be transformed into a quantum algorithm and simulated with a small number of qubits.

It is not intended to be a production-ready option pricing engine.

## Repository Description

Quantum circuit for pricing a European call option with Qiskit, using probability encoding, controlled payoff rotations, and Quantum Amplitude Estimation.
