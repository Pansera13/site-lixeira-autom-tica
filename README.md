# 🗑️ Lixeira Inteligente

Projeto de uma lixeira automática utilizando Arduino, sensores ultrassônicos e servo motor, integrada a uma dashboard moderna para monitoramento em tempo real.

---

# 📌 Objetivo

O objetivo do projeto é automatizar a abertura da tampa da lixeira e monitorar o nível de lixo de forma inteligente, melhorando:

* higiene;
* praticidade;
* automação;
* monitoramento de capacidade;
* experiência do usuário.

---

# ⚙️ Funcionamento do Projeto

A lixeira funciona através da integração entre hardware e software.

## 🔧 Hardware (Arduino)

O Arduino é responsável por:

* ler os sensores;
* detectar aproximação;
* controlar o servo motor;
* monitorar o nível da lixeira;
* enviar dados para o dashboard.

### Componentes Utilizados

* Arduino Uno
* Sensor Ultrassônico HC-SR04
* Servo Motor MG90S
* Jumpers
* Protoboard

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
```

---

## Sensor Interno

Responsável por medir o nível de lixo dentro da lixeira.

Quanto menor a distância:

* mais cheia a lixeira está.

Exemplo:

* 30 cm → vazia
* 10 cm → cheia

```cpp
nivel = map(distancia, 30, 5, 0, 100);
```

---

# 🔄 Fluxo Completo do Sistema

1. Usuário aproxima a mão
2. Sensor frontal detecta presença
3. Arduino processa os dados
4. Servo motor abre a tampa
5. Usuário descarta o lixo
6. Tampa fecha automaticamente
7. Sensor interno mede o nível
8. Dados são enviados ao dashboard
9. Dashboard atualiza em tempo real

---

# 💻 Dashboard Web

A dashboard foi desenvolvida utilizando:

* HTML
* CSS
* JavaScript

Ela exibe:

* status da tampa;
* porcentagem de lixo;
* sensores ativos;
* animações;
* modo escuro;
* monitoramento em tempo real.

---

# 🖼️ Imagens do Projeto

## Dashboard

![Dashboard](./images/dashboard.png)

## Arduino e Componentes

![Arduino](./images/arduino.jpg)

## Estrutura da Lixeira

![Lixeira](./images/lixeira.jpg)

---

# 📂 Estrutura do Projeto

```bash
📁 lixeira-inteligente
 ├── 📄 index.html
 ├── 📄 style.css
 ├── 📄 script.js
 ├── 📄 arduino.ino
 └── 📁 images
```

---

# 🚀 Tecnologias Utilizadas

## Hardware

* Arduino Uno
* HC-SR04
* Servo MG90S

## Software

* HTML5
* CSS3
* JavaScript
* Arduino IDE
* VS Code

---

# 🔮 Melhorias Futuras

* Integração com Wi-Fi
* Aplicativo mobile
* Notificações automáticas
* Histórico de uso
* Energia solar
* Inteligência artificial
* Dashboard online

---

# 👨‍💻 Desenvolvido por

Lucas Pansera, Bernaro Patriarca, Matheus Nunes.
