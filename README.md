# 🔔 Quantum Bell State Creation: A Quantum Entanglement Experiment

# What are Bell States and How Are They Created?
Bell states (also known as EPR states) are four states of two entangled qubits. This entanglement is caused by superposition of one of the qubits. The four Bell states are shown below:

$\ket{\Phi^+} = \frac{\ket{00} + \ket{11}}{\sqrt2}$ 

$\ket{\Phi^-} = \frac{\ket{00} - \ket{11}}{\sqrt2}$

$\ket{\Psi^+} = \frac{\ket{01} + \ket{10}}{\sqrt2}$

$\ket{\Psi^-} = \frac{\ket{01} - \ket{10}}{\sqrt2}$

To create each of these states, we will need a Hadamard gate (H gate) and Controlled NOT gate (CNOT gate). The H gate essentially puts a qubit into a superposition of 0 and 1 (e.g. $\ket{0}$ becomes $\ket{0} + \ket{1}$). A CNOT gate has a control and target qubit. If the control qubit is 0, the target qubit remains the same. If the control qubit is 1, the CNOT gate acts as a NOT gate for the target qubit (i.e. 0 becomes 1, 1 becomes 0).

To create $\ket{\Phi^+} = \frac{\ket{00} + \ket{11}}{\sqrt2}$, we first have two qubits: qubit 1 and qubit 2. 

$q_1=q_2=\ket{0}$
We assume that both are initialized to 0. First, we take qubit 1 and apply an H gate, to put it in superposition (i.e. making a linear combination of $\ket{0}$ and  $\ket{1}$.

$q_1=\frac{\ket{0} + \ket{1}}{\sqrt2}$
Note: the coefficient of $\frac{1}{\sqrt2}$ is needed for normalization. Since there are two possible states that are equally likely ($\ket{0}$ and $\ket{1}$), they will each have a probability of $\frac{1}{2}$ occuring. The coefficients of each of these states is the square root of its probability.

Now the 2-qubit system becomes:
$\frac{\ket{00}+\ket{10}}{\sqrt2}$


Next, we use a CNOT gate, where the measurement of qubit 1 (the control) will determine the value of qubit 2 (the target, which is currently equal to 0). Based on the explanation for how CNOT gates work from above, the system becomes:
$\frac{\ket{00}+\ket{11}}{\sqrt2}$ \
**Circuit:** \
![image](https://github.com/user-attachments/assets/0fea2115-c61f-4f68-b88a-1c74dce8b2c7)


We have now created our first Bell state $\ket{\Phi^+}$. 

To get $\ket{\Phi^-}$, we can apply a Z gate on qubit 2, which flips its sign. Therefore, the system becomes:
$\frac{\ket{00}-\ket{11}}{\sqrt2}$ \
**Circuit:** \
![image](https://github.com/user-attachments/assets/f57faa92-bae3-4fe4-b44e-18b18c148899)


To get $\ket{\Psi^+}$, we can modify the circuit we used to get $\ket{\Phi^+}$ but apply an X gate on qubit 2. This changes it from 0 to 1 or 1 to 0. Thus, the system becomes:
$\frac{\ket{01}+\ket{10}}{\sqrt2}$ \
**Circuit:** \
![image](https://github.com/user-attachments/assets/22fce6ce-e4eb-4396-a6a3-e52c1362080e)


To get $\ket{\Psi^-}$, we can modify the circuit we used to get $\ket{\Psi^+}$ and apply a Z gate on qubit 1. This flips its sign. Thus, the system becomes:
$\frac{\ket{01}-\ket{10}}{\sqrt2}$ \
**Circuit:** \
![image](https://github.com/user-attachments/assets/6b020853-2eb1-4f75-9c8b-be3173d3643f)

As a result, we have gotten all four Bell states. 

Sources: 
- https://pennylane.ai/qml/glossary/what-are-bell-states
- https://en.wikipedia.org/wiki/Bell_state#:~:text=In%20quantum%20information%20science%2C%20the,entangled%20and%20normalized%20basis%20vectors.
- https://www.quera.com/glossary/bell-state
- https://www.aliroquantum.com/blog/what-are-bell-states

# 🔗 Installation
Install dependencies using ```pip``` by running:
```pip install -r requirements.txt```
