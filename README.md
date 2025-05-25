![BlueQubit_Challenge_Yale_University Y_Quantum_Winner](https://github.com/user-attachments/assets/dc63b450-93f9-4065-9608-93626e7f5cf2)
🎯 Peaked Circuits Challenge
Participants will receive special quantum circuits (Peaked Circuits) in .qasm format where each circuit sets up a specific quantum state. Hidden within that state is a single bitstring that appears with high probability. 

Your mission is to find this bitstring!
![image](https://github.com/user-attachments/assets/d3369b2c-c9ee-425e-aa63-e18fb444fb90)

In the example above, 0110 is the peak bitstring as it has comparatively much higher probability  to be measured than all the other bitstrings. And below you can find the .qasm file that prepared this state:

OPENQASM 2.0;
include "qelib1.inc";
qreg q[4];
x q[0];
x q[3];
ry(0.8*pi) q[0];
ry(0.8*pi) q[1];
ry(0.8*pi) q[2];
ry(0.8*pi) q[3];
You are welcome to use BlueQubit’s quantum and simulation devices to tackle these circuits. To crack the hardest ones though - you have to get creative and you might need to use other simulation tools as well. 

📚 Peaked Circuits in a Nutshell
“Peaked circuits” are pre-constructed quantum circuits with a non-uniform distribution of measurement outcomes. They are designed in a way that one particular bitstring has a higher probability than others, e.g. O(1) as opposed to exponentially small amplitude. 

They were introduced by Scott Aaronson as a way to achieve verifiable quantum advantage. Carefully crafted peaked circuits look like random circuits  - like the one used by Google in their benchmark that would take supercomputers septillion=10²⁵ years to replicate. However, unlike random circuits - peaked circuits are much easier to verify: all you need to do is to run them on a quantum computer and verify you get the correct hidden bitstring!

This quantum hackathon aims to test the skills of quantum researchers and enthusiasts in how well they can use quantum computers and simulators to crack such peaked circuits. 
