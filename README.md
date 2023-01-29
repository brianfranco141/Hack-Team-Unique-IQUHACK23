<img src="https://github.com/mohadesehazari98/Hack-Team-Unique-IQUHACK23/blob/main/duck_logo.svg" align="right"
     alt="Size Limit logo by Anton Lovchikov" width="120" height="178">

# Hack-Team-Unique-IQUHACK23 

* Step 0:

we need the data set as an excel file to generate the graph, but for now, since the data is not a big issue and we just want to check the algorithm, we are using Quantum Random number generatr to create the seed. 

The first python quantum code, which is called step0_generate_random generate the text file, which is used as our initial seed to create a random excel file.

```js
q = QuantumRegister(5,'q')
c = ClassicalRegister(5,'c')
circuit = QuantumCircuit(q,c)
circuit.h(q) # Applies hadamard gate to all qubits
circuit.measure(q,c) # Measures all qubits 

backend = provider.get_backend('ibmq_qasm_simulator')
job = execute(circuit, backend, shots=35)
```

* Step 1:

we can use the previous generated seed to creat the excel file, the excel file is called sensor.xlsx

also the value.txt is the input file where you can determine how your cost function values should be

the cost_function code will simulate different cost function based on all the different criteria that you find, each criteria can be activated with a flag that you can issue. So after changing each flag, you can go on and see the matrix, this way you can decide weather it is an acceptable graph or you need to filter further.
The cost function can give you the optimized graph that you can use, as an input, to the actual quantum computer

* Step 2:

The final state is where we use the actual quantum algorithm called QAOA, Quantum Approximate Optimization Algorithm

by running this, we will get the quantum state which will determine which nodes we need to delete, in order to destroy the whole graph connections






