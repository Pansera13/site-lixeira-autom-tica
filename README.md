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

Sensor Interno

Responsável por medir o nível de lixo dentro da lixeira.

Quanto menor a distância:

mais cheia a lixeira está.

Exemplo:

30 cm → vazia
10 cm → cheia
nivel = map(distancia, 30, 5, 0, 100);
🔄 Fluxo Completo do Sistema
Usuário aproxima a mão
Sensor frontal detecta presença
Arduino processa os dados
Servo motor abre a tampa
Usuário descarta o lixo
Tampa fecha automaticamente
Sensor interno mede o nível
Dados são enviados ao dashboard
Dashboard atualiza em tempo real
💻 Dashboard Web

A dashboard foi desenvolvida utilizando:

HTML
CSS
JavaScript

Ela exibe:

status da tampa;
porcentagem de lixo;
sensores ativos;
animações;
modo escuro;
monitoramento em tempo real.
🖼️ Imagens do Projeto
Dashboard

Arduino e Componentes

Estrutura da Lixeira

📂 Estrutura do Projeto
📁 lixeira-inteligente
 ├── 📄 index.html
 ├── 📄 style.css
 ├── 📄 script.js
 ├── 📄 arduino.ino
 └── 📁 images
🚀 Tecnologias Utilizadas
Hardware
Arduino Uno
HC-SR04
Servo MG90S
Software
HTML5
CSS3
JavaScript
Arduino IDE
VS Code
🔮 Melhorias Futuras
Integração com Wi-Fi
Aplicativo mobile
Notificações automáticas
Histórico de uso
Energia solar
Inteligência artificial
Dashboard online
👨‍💻 Desenvolvido por

Lucas