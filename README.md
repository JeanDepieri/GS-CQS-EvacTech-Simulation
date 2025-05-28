# GS-CQS-EvacTech-Simulation


=## 💻 Exemplo de Simulação

O trecho abaixo simula sensores sísmico, de temperatura, de CO₂/O₂ e de vento em um circuito quântico com Qiskit:

```python
from qiskit import QuantumCircuit, execute
from qiskit_aer import Aer
from qiskit.visualization import plot_histogram
import matplotlib.pyplot as plt

qc = QuantumCircuit(4, 4)

# Superposição: sensores fazendo leitura
qc.h([0, 1, 2, 3])

# Emaranhamento: sensores interdependentes
qc.cx(0, 1)  # sismo afeta temperatura
qc.cx(2, 3)  # CO₂/O₂ afeta vento

# Medição
qc.measure([0, 1, 2, 3], [0, 1, 2, 3])

# Simulação
backend = Aer.get_backend('qasm_simulator')
resultado = execute(qc, backend=backend, shots=1024).result()
plot_histogram(resultado.get_counts())
plt.show()
