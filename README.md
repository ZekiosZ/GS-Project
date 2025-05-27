# Detector de Nível de Água com ESP32 e Sensor Ultrassônico

## 👨‍💻 Integrantes do Grupo

- **José Rafael Tejeda Mantilla** – RM: 561849  
- **Theodoro Sievers** – RM: 562036  
- **Walter Henrique Pereira de Toledo** – RM: 562476  

---

## 🌧️ Descrição do Projeto

Este projeto simula um sistema de monitoramento de enchentes utilizando um **ESP32** e um **sensor ultrassônico HC-SR04**. Ele mede o nível da água e, com base nessa leitura, aciona alertas visuais e sonoros. O sistema também simula uma comunicação com a nuvem (IoT) para enviar notificações sobre a situação.

A proposta visa oferecer uma solução acessível e eficaz para **prevenção de desastres em áreas de risco de alagamento** no Brasil.

---

## 🎯 Objetivos

- Detectar aumento no nível da água de forma contínua.
- Alertar visualmente com LEDs (verde, amarelo e vermelho).
- Acionar um buzzer em situações críticas.
- Simular envio de dados para um servidor (IoT teórico).
- Tornar o projeto aplicável e funcional em um simulador como o Wokwi.

---

## ⚙️ Componentes Utilizados

- ESP32 DevKit v1  
- Sensor ultrassônico HC-SR04  
- LEDs: verde, amarelo e vermelho  
- Buzzer piezoelétrico  
- Resistores e jumpers (conforme necessário)  
- Protoboard  

---

## 🧠 Funcionamento

1. O sensor ultrassônico mede a distância entre ele e a superfície da água.
2. Com base na distância lida, o sistema classifica o nível em:
   - **Normal** (> 200 cm): LED verde aceso.
   - **Alerta** (100–199 cm): LED amarelo aceso.
   - **Crítico** (≤ 99 cm): LED vermelho aceso + buzzer ativo.
3. Mensagens são exibidas no Serial Monitor simulando o envio de dados para a nuvem.

---

## ☁️ Simulação de IoT (Teórica)

Embora o projeto rode no Wokwi sem Wi-Fi real, o código contém trechos comentados com instruções de como enviar os dados para um servidor real utilizando:
- Biblioteca `WiFi.h`
- Biblioteca `HTTPClient.h`
- Envio via protocolo HTTP com JSON

---

## 🧪 Como Testar no Wokwi

1. Acesse o projeto no Wokwi: **(https://wokwi.com/projects/432023123854233601)**  
2. Clique em ▶️ "Start Simulation"
3. Aproxime ou afaste um objeto do sensor (simulação do nível da água)
4. Observe os LEDs e mensagens no Serial Monitor

---

## 💡 Futuras Melhorias

- Integração real com plataforma IoT como Firebase, Blynk ou ThingSpeak
- Alimentação via painel solar com bateria
- Envio de SMS/emails em caso de alerta
- Aplicativo para monitoramento remoto
- Comunicação via LoRa para áreas sem internet
