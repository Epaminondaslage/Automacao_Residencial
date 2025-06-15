<td style="width: 20%;"><img src="/img/top_automacao_residencial.png" width="100%" /></td>

# Plataforma de Automação Residencial 

A escolha de plataforma de automação residencial de código aberto que permite aos usuários controlar e monitorar dispositivos e serviços em suas casas é o mote deste projeto. Construído em torno de um núcleo central, optou-se pelo Home Assistant sendo que este atua como um hub de automação, oferecendo suporte a uma ampla gama de dispositivos e integrações.

Uma das sua principais características é a capacidade de integração com várias marcas e protocolos. Ele suporta a integração com marcas conhecidas, como Philips Hue, Nest, Sonos, Amazon Echo, Google Home, Z-Wave, Zigbee, entre outras. Isso permite que os usuários reúnam todos os dispositivos e serviços em uma única plataforma, simplificando o controle e a automação residencial.

Com este software, os usuários podem integrar e controlar dispositivos populares, como lâmpadas inteligentes, termostatos, câmeras de segurança, fechaduras de portas, sensores de movimento e muito mais. Através de uma interface web ou de aplicativos móveis, é possível gerenciar esses dispositivos de forma conveniente. Também oferece recursos avançados de automação, permitindo aos usuários criar rotinas e cenários personalizados. Por exemplo, é possível configurar uma automação para ligar as luzes da sala de estar, ajustar a temperatura do termostato e reproduzir música ambiente quando alguém chegar em casa.

Esta plataforma possui recursos de monitoramento e notificação. Os usuários podem receber alertas quando sensores detectarem movimento, quando a temperatura estiver fora dos limites desejados ou quando uma porta for aberta. Essa funcionalidade garante que os usuários estejam sempre cientes do que está acontecendo em suas residências, mesmo quando estiverem ausentes.

## Repositórios Disponíveis

* <a href="https://github.com/Epaminondaslage/HomeAssistant">Home Assistant</a> 
* <a href="https://github.com/Epaminondaslage/HomeAssistant-ESPHome">Home Assistant e ESPHome</a> 
* <a href="https://github.com/Epaminondaslage/HomeAssistant-MQTT">Home Assistant e MQTT</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-Tuya">Home Assistant e Tuya</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-Tasmota-MQTT">Home Assistant Tasmota e MQTT</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-Sonoff">Home Assistant e Sonoff</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-NodeRED">Home Assistant e NodeRED</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-Telegram">Home Assistant e Telegram</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-NodeMCU-MQTT">Home Assistant - NodeMCU e MQTT</a>
* <a href="https://github.com/Epaminondaslage/HomeAssistant-ESP32-ESP8266-ESPHome">Home Assistant-ESP32-ESP8266-ESPHome</a>


# Comparativo entre Protocolos: Sonoff, Zigbee, Tuya, SmartThings, Tasmota e Matter

## 📊 Tabela Comparativa

| Plataforma/Marca   | Protocolo Principal     | Controle Local | Integração com Home Assistant | Nuvem Necessária? | Código Aberto? | Precisa de Gateway? | Observações                          |
|--------------------|-------------------------|----------------|-------------------------------|-------------------|----------------|----------------------|--------------------------------------|
| **Sonoff (stock)**     | Wi-Fi + eWeLink         | ❌            | ✅ (via eWeLink add-on)      | ✅               | ❌            | ❌                    | Depende da nuvem                     |
| **Sonoff (Tasmota)**   | Wi-Fi + MQTT            | ✅            | ✅ (via MQTT)                | ❌               | ✅            | ❌                    | Controle local total                 |
| **Zigbee**             | Zigbee (IEEE 802.15.4)  | ✅            | ✅ (via Zigbee2MQTT ou ZHA)  | ❌               | ✅            | ✅                    | Requer gateway Zigbee               |
| **Tuya (stock)**       | Wi-Fi (Tuya Cloud)      | ❌            | ✅ (via Tuya Integration)    | ✅               | ❌            | ❌                    | Integração via nuvem                |
| **Tuya (LocalTuya)**   | Wi-Fi + protocolo local | ✅            | ✅ (via LocalTuya)           | ❌               | ❌ (reverso)  | ❌                    | Controle local via IP               |
| **SmartThings**        | Zigbee, Z-Wave, Wi-Fi   | ❌ (geralmente)| ✅ (via SmartThings API)     | ✅               | ❌            | ✅                    | Requer hub SmartThings              |
| **Tasmota**            | Wi-Fi + MQTT/HTTP       | ✅            | ✅ (via MQTT ou HTTP)        | ❌               | ✅            | ❌                    | Ideal para projetos DIY             |
| **Matter (Wi-Fi)**     | Wi-Fi                   | ✅            | ✅ (nativo no HA 2023.11+)   | ❌               | ✅ (em partes)| ❌                    | IP nativo, sem gateway necessário   |
| **Matter (Thread)**    | Thread                  | ✅            | ✅ (com Thread Border Router)| ❌               | ✅ (em partes)| ✅                    | Requer gateway Thread (border router) |

---

## 🧠 Detalhamento por Plataforma

### 🔹 Sonoff (stock)
- Usa Wi-Fi e se conecta à nuvem eWeLink.
- Integração com Home Assistant por API ou integração eWeLink.
- Sem controle local por padrão.

### 🔹 Sonoff com Tasmota
- Firmware alternativo de código aberto.
- Conecta-se via Wi-Fi usando MQTT ou HTTP.
- Controle local total e integração nativa com Home Assistant.

### 🔹 Zigbee
- Protocolo sem fio de baixo consumo e ideal para sensores e atuadores.
- Cria rede mesh e exige um **gateway Zigbee**.
- Integração via ZHA ou Zigbee2MQTT no Home Assistant.

### 🔹 Tuya (stock)
- Usa Wi-Fi e se comunica via nuvem Tuya Smart Life.
- Integração via API Tuya no Home Assistant.
- Pode ter limitações de velocidade/responsividade.

### 🔹 Tuya com LocalTuya
- Integração local, rápida e sem dependência da nuvem.
- Precisa de IP fixo e configuração manual.
- Não é oficialmente suportado pela Tuya.

### 🔹 SmartThings
- Hub da Samsung que suporta Zigbee, Z-Wave e Wi-Fi.
- Integração via API na nuvem com Home Assistant.
- Requer o Hub físico SmartThings.

### 🔹 Tasmota
- Firmware alternativo para ESP8266/ESP32.
- Controle local completo via MQTT.
- Ideal para quem busca autonomia, personalização e segurança.

### 🔹 Matter (Wi-Fi ou Thread)
- Novo padrão unificado e aberto para casas inteligentes.
- Integração local com Home Assistant (v2023.11+).
- Usa Wi-Fi ou Thread (Thread requer um **gateway Thread**).
- Compatível com Apple, Google, Amazon e outros.

---

## 🧭 Recomendação por Perfil

| Perfil                     | Melhor Escolha                |
|---------------------------|-------------------------------|
| Totalmente local/privado  | Zigbee + Tasmota ou Matter    |
| Facilidade/praticidade    | Tuya (stock), SmartThings     |
| Barato e personalizável   | Sonoff com Tasmota            |
| Alta compatibilidade      | Zigbee + Zigbee2MQTT ou Matter|

---

## 🧩 Gateways Recomendados

### ✅ Zigbee
Requer gateway USB ou integrado para comunicar com a rede Zigbee.

**Gateways Compatíveis:**
- Sonoff Zigbee USB Dongle Plus (E/P)
- ConBee II
- CC2652P (ZZH!, Slaesh)
- Home Assistant SkyConnect

### ✅ Z-Wave
Também exige gateway para conversão da rede Z-Wave.

**Gateways Compatíveis:**
- Aeotec Z-Stick 7
- Zooz ZST10
- Qualquer dongle compatível com Z-Wave JS

### ✅ Thread (para Matter)
Matter usando Thread requer um **Thread Border Router**.

**Gateways Compatíveis:**
- Apple HomePod Mini
- Google Nest Hub (2ª geração)
- Amazon Echo (4ª geração)
- Home Assistant SkyConnect (modo multi-protocolo)

---

## ❓ O que significa "Stock"

**"Stock"** refere-se ao firmware original que acompanha o dispositivo de fábrica.

### Exemplo:
- **Sonoff stock** = usa eWeLink
- **Tuya stock** = usa Tuya Smart Life Cloud
- **SmartThings stock** = vinculado ao app da Samsung

### Diferença:
| Tipo de Firmware | Características |
|------------------|------------------|
| Stock            | Depende da nuvem |
| Custom           | Controle local, personalizável |

### Por que usar firmware custom?
- Independência da nuvem
- Maior segurança
- Resposta mais rápida
- Integração com Home Assistant

---

## 🆕 Sobre o Matter

- Padrão desenvolvido pela CSA com Apple, Google, Amazon, Samsung.
- Suporte local e aberto.
- Compatível com Home Assistant e várias plataformas.
- Usa Wi-Fi, Thread e Ethernet.
- Espera-se ampla adoção nos próximos anos.