# GS-EvacTech-Simulation

## 📘 Notebook do Projeto

Clique para acessar o notebook com a simulação quântica completa:

📘 Acesse o notebook do projeto:  
👉 [quantum_routing_simulation.ipynb](https://github.com/JeanDepieri/GS-CQS-EvacTech-Simulation/blob/main/quantum_routing_simulation.ipynb.ipynb)

Este código simula um sistema de monitoramento para situações de emergência usando computação quântica. Cada qubit representa um sensor diferente: sensor sísmico, de temperatura, de CO₂/O₂ e de vento. Inicialmente, os sensores são colocados em estado de superposição, simulando a incerteza natural nas leituras em tempo real. Em seguida, são aplicadas portas CNOT para emaranhar sensores interdependentes, como por exemplo: tremores influenciando a temperatura e a qualidade do ar afetando os padrões de vento.

A medição colapsa o circuito em diferentes combinações de leitura, que são simuladas 1024 vezes para gerar um histograma com os cenários mais prováveis. O resultado representa, de forma probabilística, quais combinações de risco podem ocorrer em campo — permitindo prever padrões perigosos e tomar decisões rápidas em rotas de evacuação.

Este modelo demonstra como a computação quântica pode ser aplicada para otimizar a resposta a desastres naturais, processando múltiplos cenários ao mesmo tempo, com sensores interligados, mesmo em situações de incerteza e dados incompletos.
