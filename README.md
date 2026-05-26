# 🗑️ Lixeira Inteligente

Projeto de uma lixeira automática utilizando Arduino, sensores ultrassônicos e servo motor, integrada a uma dashboard moderna para monitoramento em tempo real.

---

# 📌 Objetivo

O objetivo do projeto é automatizar a abertura da tampa da lixeira e monitorar o nível de lixo de forma inteligente, melhorando:
- higiene;
- praticidade;
- automação;
- monitoramento de capacidade;
- experiência do usuário.

---

# ⚙️ Funcionamento do Projeto

A lixeira funciona através da integração entre hardware e software.

## 🔧 Hardware (Arduino)

O Arduino é responsável por:
- ler os sensores;
- detectar aproximação;
- controlar o servo motor;
- monitorar o nível da lixeira;
- enviar dados para o dashboard.

### Componentes Utilizados

- Arduino Uno
- Sensor Ultrassônico HC-SR04
- Servo Motor MG90S
- Jumpers
- Protoboard

---

# 📡 Funcionamento dos Sensores

## Sensor Frontal

Detecta quando uma mão se aproxima da lixeira.

Quando a distância é pequena:
1. o Arduino detecta a presença;
2. o servo motor é acionado;
3. a tampa abre automaticamente;
4. após alguns segundos ela fecha.

```cpp
if (distanciaFrente < 20) {
    abrirTampa();
}