# Meta Quantum Backend (MQBac)

## 2 goals:

1) **Auto select QPM backend for QFw**, at the same place where MPI processes are decided based on #qubits.

2) **Estimate runtime** of a given quantum circuit/algorithm, and a chosen QPM backend (or choose 1 from goal-1), and resources available to it (could be classical/quantum queue priorities etc..)

   *(basically all features/metrics collected via QBacMet tool: https://github.com/srikarchundury/QBacMet)*