# 🌽 Projeto de Simulação de Irrigação e Equilíbrio de pH do Solo com ESP32

Projeto desenvolvido pelos alunos da **turma 1TIAOR** do curso de **Inteligência Artificial** da **Faculdade FIAP**.

![Simulação do circuito no Wokwi]("C:\Users\Pichau\Desktop\asset\projeto sensores.png")

## 📘 Descrição Geral

Este projeto tem como objetivo simular a **automatização da irrigação** e o **equilíbrio do pH do solo** por meio da adubação com NPK, utilizando sensores conectados a uma placa **ESP32**. O modelo de cultivo utilizado é o **milho**, com parâmetros técnicos baseados nas recomendações da **Embrapa**.

A simulação foi realizada na plataforma [Wokwi](https://wokwi.com), que permite a compilação e visualização do funcionamento do sistema embarcado.

---

## ⚙️ Funcionamento do Sistema

### 🌡️ Sensor de Umidade (DHT22)
- O sensor DHT22 foi adaptado para simular a **umidade do solo**, embora originalmente meça a umidade relativa do ar.
- A umidade é inserida manualmente no formato `U=65.00`, simulando 65% de umidade.
- Quando a umidade simulada está **abaixo de 70%**, o sistema:
  - Aciona o **relé**
  - Liga o **LED azul** (representando a bomba de irrigação)
  - Exibe uma **mensagem de alerta** sobre a baixa umidade e início da irrigação

### 💡 Sensor de pH (LDR + Botões)
- Um **sensor LDR** foi utilizado para simular a leitura de pH, com três **botões verdes** representando:
  - **N** – Nitrogênio
  - **P** – Fósforo
  - **K** – Potássio
- Cada botão simula um **desequilíbrio no pH** do solo.
- Ao pressionar qualquer botão:
  - O sistema aciona a **fertirrigação**
  - O LED azul é ligado
  - Uma mensagem alerta sobre o desequilíbrio e a correção via adubação

### 💧 Bomba de Irrigação (Relé + LED)
- A bomba é representada por um **LED azul**:
  - **Ligado**: irrigação ou fertirrigação em andamento
  - **Desligado**: solo em condições ideais
- O **relé** controla o acionamento da bomba com base nas leituras dos sensores

---

## 🧪 Simulação e Parâmetros

- A simulação inicia com **0% de umidade**
- O valor ideal de pH para o milho é **6,5**, mas na simulação foi utilizado o valor **1000** como referência de equilíbrio
- A lógica de controle é baseada em **condições simples** de comparação e acionamento de atuadores

---

## 🔌 Componentes Utilizados

| Componente     | Função                                      |
|----------------|---------------------------------------------|
| ESP32          | Placa microcontroladora principal           |
| DHT22          | Sensor de umidade (simulado como solo)      |
| LDR            | Sensor de luminosidade (simulado como pH)   |
| Botões (3x)    | Simulação de desequilíbrio de N, P e K      |
| Relé           | Controle da bomba de irrigação              |
| LED Azul       | Representa o estado da bomba                |

---

## 🖥️ Plataforma de Simulação

- **Wokwi.com** foi utilizado para simular o circuito e compilar o código
- A pinagem dos sensores segue os padrões da **ESP32**

---

## 🚀 Como Usar

1. Acesse o projeto no [Wokwi](https://wokwi.com/projects/444371288476560385)
2. Digite o valor de umidade no formato `U=65.00`
3. Pressione os botões verdes para simular desequilíbrios de pH
4. Observe os alertas e o acionamento do LED azul

---

## 📚 Referências

- [Embrapa – Cultivo de Milho](https://www.embrapa.br/milho-e-sorgo)
- [Wokwi – Simulador de Arduino e ESP32](https://wokwi.com)

---

## 👨‍💻 Autoria

Projeto acadêmico desenvolvido pelos alunos da **1TIAOR – FIAP** no curso de **Inteligência Artificial**.
