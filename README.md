# 🌌 My Quantum Algorithms & Simulations Playground

Welcome to my quantum computing project repository. I developed this space to implement, simulate, and document foundational quantum algorithms using the modern **Qiskit v1.x** framework. 

My goal with this project is to move beyond theoretical equations and practically demonstrate the computational speedups that quantum mechanics provides over classical architectures.

---

## 🚀 Algorithms Implemented

### 1. The Deutsch-Jozsa Algorithm
I implemented this circuit to explore the core concept of quantum parallelism. The algorithm evaluates a hidden black-box function (oracle) to determine if it is constant or balanced. While a classical approach scales exponentially in the worst-case scenario, this quantum circuit successfully determines the global property of the oracle in **exactly one single evaluation**.

#### 📊 Performance Scaling Contrast
| Input Size ($n$ bits) | Classical Queries Needed (Worst Case) | Quantum Queries Needed |
| :--- | :--- | :--- |
| **1 bit** | 2 | **1** |
| **10 bits** | 513 | **1** |
| **30 bits** | 536,870,913 | **1** |

---

### 2. Shor's Algorithm (Factoring $N=15$)
To study quantum Fourier systems, I built a toy-model simulation of Shor’s Algorithm configured to find the prime factors of $N=15$. The circuit utilizes an **Inverse Quantum Fourier Transform (IQFT)** to handle the critical period-finding step, showcasing the mathematical framework that poses a theoretical threat to modern RSA cryptography.

#### 📊 Cryptographic Impact (Factoring an RSA-2048 Key)
| Architecture | Core Mathematical Approach | Time Complexity / Estimated Duration |
| :--- | :--- | :--- |
| **Classical Supercomputer** | General Number Field Sieve (GNFS) | **~300 Trillion Years** |
| **Quantum Computer** | Shor's Period-Finding Algorithm | **~Just a few hours** (Fault-Tolerant) |

---

## 🛠️ Framework & Implementation Standards

To ensure the longevity and relevance of the codebase, I intentionally avoided deprecated legacy Qiskit backends (such as `execute` or `AerBackend`) and strictly adhered to contemporary Qiskit design patterns:

* **Language:** Python 3.10+
* **SDK Version:** Qiskit v1.x
* **Execution Engine:** `qiskit.primitives.StatevectorSampler`
* **Circuit Layouts:** Pure gate-level compositions with text-based schematic rendering enabled.

---

## 💻 How to Evaluate the Simulations

The codebase is optimized for seamless, immediate grading and review without requiring local virtual environments or package installations:

1. Open the accompanying `.ipynb` notebook file in this repository.
2. Click the **"Open in Colab"** badge located at the top of the file.
3. Execute the cells sequentially. The notebook includes a pre-configured setup block (`!pip install qiskit qiskit-aer`) that automatically provisions the cloud environment with all necessary dependencies.

---
