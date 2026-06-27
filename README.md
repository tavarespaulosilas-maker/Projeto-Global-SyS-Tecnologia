

# 🚀 Global SyS Tecnologia — Monitoramento Inteligente de Fluxo via IoT

> Solução eficiente e de baixo custo baseada em Internet das Coisas (IoT) para automação da contagem de clientes e gestão inteligente de fluxo em lojas de varejo.

## 📋 Sobre o Projeto
A **Global SyS Tecnologia** enfrenta desafios críticos na gestão de fluxo de clientes, especialmente nos horários de pico. A ausência de métricas precisas sobre a taxa de ocupação gera filas excessivas, desistência de compras e escalas de funcionários ineficientes.

### O Problema: O "Pico Cego"
Atualmente, o gerente não possui dados em tempo real para decidir o momento exato de abrir novos caixas ou reforçar o atendimento, baseando-se apenas em perceção visual subjetiva.

### A Solução
Este projeto propõe a utilização de sensores ultrassónicos e microcontroladores para automatizar a contagem de clientes que entram no estabelecimento, gerando inteligência de negócio através de dashboards em tempo real.

## 🛠️ Arquitetura do Sistema

O sistema é dividido em três camadas fundamentais para garantir robustez e escalabilidade:

1. **Camada de Borda (Edge):** Microcontrolador realizando a leitura física e deteção de presença através de sensores posicionados na entrada do estabelecimento.
2. **Camada de Comunicação (Network):** Estruturação dos dados em formato JSON e envio seguro via protocolo HTTP/MQTT com criptografia WPA2.
3. **Camada de Aplicação (Cloud):** Integração com a plataforma **TagoIO** para armazenamento de logs, análise histórica e exibição de dashboards gerenciais.
<img width="584" height="429" alt="Diagrama" src="https://github.com/user-attachments/assets/9c1ae763-bd54-4664-abdd-9b2dbdc6bef9" />

## ⚙️ Especificação de Componentes
| Componente | Função Técnica |
| **Microcontrolador (ESP32 / Arduino)** | Processamento lógico e conectividade Wi-Fi nativa (ESP32 recomendado para implementação real)
| **Sensor HC-SR04** | Deteção de presença via ondas ultrassónicas, garantindo a total privacidade dos clientes.
<img width="541" height="268" alt="ESP 32" src="https://github.com/user-attachments/assets/7cfee631-3a9e-440a-808a-84bef0f7d227" />
<img width="509" height="281" alt="Arduino" src="https://github.com/user-attachments/assets/c52baced-62db-4e8b-be57-804cd6900381" />

⚠️ **Nota de Implementação:** Para o desenvolvimento do protótipo em ambiente de simulação utilizou-se o Arduino por facilidade no Tinkercad. No entanto, para a implantação real em ambiente físico, deve ser utilizado o **ESP32**, dado que o Arduino nativo não possui conectividade Wi-Fi para comunicação com a nuvem.

---

## 💻 Protocolo de Comunicação (JSON)
Para a comunicação com a API da TagoIO, os dados são estruturados de forma leve e padronizada:

  "variable": "fluxo_clientes",
  "value": 49,
  "unit": "pessoas",
  "metadata": {
    "local": "Entrada Principal",
    "status": "Normal"
  }d" />

}```json


<img width="500" height="280" alt="Dashboard" src="https://github.com/user-attachments/assets/3b943d7d-a685-46fe-bf09-24e73094e833" />

Dashboard parecido com a implementação
