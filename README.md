
# ECU Fusca - Controle Eletrônico para Fusca Clássico com ESP32

## 🎯 Objetivo
Este projeto consiste no desenvolvimento de uma Unidade de Controle Eletrônico (ECU) personalizada para o Volkswagen Fusca, utilizando ESP32 e um display TFT touch. O sistema visa modernizar o painel e agregar funcionalidades de segurança e conforto.

---

## 📦 Funcionalidades

- **Display TFT com Touch (SPI)**: Interface gráfica no painel do carro
- **Alarme Sonoro**: Emissão de alerta por buzzer para falhas ou eventos
- **Monitoramento de Falhas**:
  - Fusíveis queimados
  - Lâmpadas queimadas (lanternas, freio, ré, faróis)
- **Luz de Cortesia**:
  - Acende com abertura da porta
  - Fade automático de 100% → 0% em até 30 segundos
- **Conta-Giros**:
  - Leitura por sinal negativo da bobina de ignição
  - Conversão em RPM via frequência
- **Alarmes Inteligentes**:
  - Porta aberta com farol aceso e motor desligado

---

## ⚙️ Arquitetura

### Microcontrolador
- ESP32-WROOM-32 (DevKit V1)
- Programação em Arduino IDE
- Comunicação SPI com display
- PWM para luz de cortesia

### Interface com o usuário
- Display TFT 2.4” (ILI9341) com XPT2046 (touch resistivo)
- Biblioteca recomendada: `TFT_eSPI`

### Entradas / Sensores
- Estado das portas (reed switch ou botão)
- Estado das luzes (via relé ou sinal 12V)
- Leitura da bobina (via optoacoplador)

### Saídas
- PWM para LED da luz de cortesia
- Buzzer para sinalização sonora

---

## 🧾 Lista de Arquivos

| Arquivo                         | Descrição                                 |
|--------------------------------|-------------------------------------------|
| ECU_Fusca_Eagle.sch            | Esquemático eletrônico (Eagle)            |
| ECU_Fusca_Eagle.brd            | Layout da PCB (Eagle)                     |
| ECU_Fusca_Schematic.pdf        | Versão em PDF do esquemático              |
| ECU_Fusca_PCB.pdf              | Visão 2D da placa em PDF                  |
| ECU_Fusca_BoM_Completo.xlsx    | Lista de materiais (BoM) detalhada        |

---

## 🚧 Proximos Passos

- Finalização do esquemático real (.sch) com símbolos e conexões
- Geração do layout real da PCB (.brd)
- Exportação dos arquivos Gerber
- Desenvolvimento do firmware (.ino) para ESP32
- Integração e testes no veículo

---

## 👨‍💻 Desenvolvido por

**Andre**  
Fullstack Developer | Eng. de Negócios | Especialista em Sistemas Embarcados

