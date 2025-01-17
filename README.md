# Repo for Entanglement Encoding
## Abstract
Quantum entanglement is a critical resource for quantum networks, enabling quantum network applications, such as distributed quantum computing. However, entanglement degradation caused by quantum channel noise may hinder the proper functioning of these applications. In this paper, we qualitatively and quantitatively analyze the characteristics and shortcomings of Quantum Error Correction (QEC) and Entanglement Purification (EP), two mainstream schemes for mitigating entanglement degradation. QEC uses qubits as basic coding units to create logical qubits and logical entanglements, achieving high effectiveness in mitigating entanglement degradation. However, the resource requirements of QEC are enormous. EP utilizes simple quantum gates to improve entanglement fidelity and mitigate entanglement degradation, but the effect is less significant than that of QEC. Therefore, we propose a novel scheme called Entanglement Encoding (EE). The core idea of EE is to use physical entanglements as basic coding units to realize highly robust logical entanglement for mitigating entanglement degradation. We prove the feasibility of EE while discussing its scalability, logical state error rate, effectiveness, limitations, and potential. The simulation experiments show that the effectiveness of EE in mitigating entanglement degradation is superior to that of EP and equal to that of QEC, while the resource efficiency of EE has the potential to surpass that of QEC.
## Repository Structure
- `EE`                   source code of EE
	+ `D-CNOT`  the experiment of EE-based D-CNOT
		* `EE Based D-CNOT.ipynb` including the quantum circuit of EE-based D-CNOT, the experiment of EE-based D-CNOT performance, and the experiment of EE-based D-CNOT under different noise
	+ `EntanglementDistribution` source code of the experiment of EEBED
		* `EEBED(3_nodes).ipynb` including the quantum circuit of 3-hop EEBED and the experiment of EEBED performance
		* `EEBED(4_nodes).ipynb` including the quantum circuit of 4-hop EEBED and the experiment of EEBED performance
		* `EEBED(indirectly throughput test).ipynb` calculating the throughput of EEBED according to the result of EEBED(3_nodes) and EEBED(4_nodes).
- `ComparisonMethods`          source code of Entanglement Purification(EP), Surface Code(SC), traditional D-CNOT, and traditional Entanglement Distribution (traditional ED)
	+ `D-CNOT` the experiment of EP-based D-CNOT, SC-based D-CNOT and traditional D-CNOT
		* `EP Based D-CNOT.ipynb` including the quantum circuit of EP-based D-CNOT, and the experiment of EP-based D-CNOT performance
		* `Surface Code Based D-CNOT(approximate simulation).ipynb` including the quantum circuit of SC-based D-CNOT, the experiment of SC-based D-CNOT performance
		* `Traditional D-CNOT.ipynb` including the quantum circuit of traditional D-CNOT, the pilot experiment, and the experiment of traditional D-CNOT performance
	+ `EntanglementDistribution` the experiment of traditional ED
		* `ordinary_long_distance_ED(3_nodes).ipynb` including the quantum circuit of 3-hop traditional ED, the experiment of traditional ED performance, and the throughput of 3-hop traditional ED
		* `ordinary_long_distance_ED(4_nodes).ipynb` including the quantum circuit of 4-hop traditional ED, the experiment of traditional ED performance, and the throughput of 4-hop traditional ED
## Run Experiments
```bash
# Choice 1: Run locally. (Recommended)
# 1. *This step is platform-specific* 
# install Python >= 3.8.2, qiskit >= 1.1.2, qiskit-aer >= 0.14.2, and qiskit-ibm-runtime >= 0.27.0
# 2. Install qiskit and qiksit-ibm-runtime
# refer to https://docs.quantum.ibm.com/guides/install-qiskit
# 3. Install qiskit-aer
# refer to https://qiskit.github.io/qiskit-aer/getting_started.html
# 4, Install jupyter
# pip3 install jupyterlab
# 5. Download source code
# git clone https://github.com/hebinjie33/EntanglementEncoding.git
# 6. Run experiments
# command: cd EntanglementEncoding/
# command: jupyter lab
# run the code in the web page of jupyter lab

# Choice 2: Run on the cloud.
# users can direclty run the source code in the IBM quantum platform.
# 1. Download source code
# git clone https://github.com/hebinjie33/EntanglementEncoding.git
# 2. Copy the source code to IBM quantum platform 
# refer to https://quantum.ibm.com/
```
## Note
```bash
# 1，Users can visualize the quantum circuit by using "circuit.draw("mpl")".
# 2, Users can simulate different scenarios by changing the parameters according to the code annotation, such as scenarios A, B, and C described in the paper.
```
## Authors
- Binjie He (hebinjie33@gmail.com)
- Seng W. Loke (seng.loke@deakin.edu.au)
- Dong Zhang (zhangdong@fzu.edu.cn) 
- Shengrui Lin (xmlsr@foxmail.com)
- Luke Lu (luklu@cisco.com)

