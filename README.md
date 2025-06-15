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

| Plataforma/Marca   | Protocolo Principal     | Controle Local | Integração com Home Assistant | Nuvem Necessária? | Código Aberto? | Observações                          |
|--------------------|-------------------------|----------------|-------------------------------|-------------------|----------------|--------------------------------------|
| **Sonoff (stock)**     | Wi-Fi + eWeLink         | ❌            | ✅ (via eWeLink add-on)      | ✅               | ❌            | Depende da nuvem                     |
| **Sonoff (Tasmota)**   | Wi-Fi + MQTT            | ✅            | ✅ (via MQTT)                | ❌               | ✅            | Controle local total                 |
| **Zigbee**             | Zigbee (IEEE 802.15.4)  | ✅            | ✅ (via Zigbee2MQTT ou ZHA)  | ❌               | ✅            | Requer coordenador Zigbee           |
| **Tuya (stock)**       | Wi-Fi (Tuya Cloud)      | ❌            | ✅ (via Tuya Integration)    | ✅               | ❌            | Integração via nuvem                |
| **Tuya (LocalTuya)**   | Wi-Fi + protocolo local | ✅            | ✅ (via LocalTuya)           | ❌               | ❌ (reverso)  | Controle local via IP               |
| **SmartThings**        | Zigbee, Z-Wave, Wi-Fi   | ❌ (geralmente)| ✅ (via SmartThings API)     | ✅               | ❌            | Integração com nuvem Samsung        |
| **Tasmota**            | Wi-Fi + MQTT/HTTP       | ✅            | ✅ (via MQTT ou HTTP)        | ❌               | ✅            | Ideal para projetos DIY             |
| **Matter**             | Thread, Wi-Fi, Ethernet | ✅            | ✅ (nativo no HA 2023.11+)   | ❌               | ✅ (em partes) | Suporte nativo crescente, padrão aberto |

---

## 🧠 Detalhamento por Plataforma

- **Sonoff (stock)**: Usa Wi-Fi com nuvem eWeLink. Não possui controle local por padrão.
- **Sonoff com Tasmota**: Firmware alternativo com controle local via MQTT. Totalmente integrado ao Home Assistant.
- **Zigbee**: Protocolo de baixo consumo. Integração com Home Assistant via ZHA ou Zigbee2MQTT.
- **Tuya (stock)**: Usa Wi-Fi com a nuvem da Tuya. Integração via API.
- **Tuya com LocalTuya**: Integração local via IP com o Home Assistant.
- **SmartThings**: Usa vários protocolos e depende da nuvem da Samsung.
- **Tasmota**: Firmware open-source para ESP8266/ESP32. Integração local via MQTT.
- **Matter**: Novo protocolo unificado, local-first, baseado em Thread, Wi-Fi ou Ethernet. Suporte nativo no Home Assistant e compatível com Apple, Google, Amazon e outros.

---

## 🧭 Recomendações por Perfil de Usuário

| Perfil                     | Melhor Escolha                |
|---------------------------|-------------------------------|
| Totalmente local/privado  | Zigbee + Tasmota ou Matter    |
| Facilidade/praticidade    | Tuya (stock), SmartThings     |
| Barato e personalizável   | Sonoff com Tasmota            |
| Alta compatibilidade      | Zigbee + Zigbee2MQTT ou Matter|

---

## ❓ O que significa "Stock"?

**"Stock"** significa firmware original de fábrica.

### Exemplos:
- **Sonoff stock**: vem com firmware eWeLink.
- **Tuya stock**: vem com firmware Tuya Cloud.
- **SmartThings stock**: controlado por app da Samsung.

### Diferença entre "stock" e "custom firmware":

| Tipo de Firmware   | Características                          |
|--------------------|------------------------------------------|
| **Stock firmware**     | Original do fabricante, usa nuvem        |
| **Custom firmware**    | Alternativo como Tasmota ou ESPHome      |

### Por que mudar o firmware stock?
- Controle local sem internet
- Melhor integração com Home Assistant
- Maior segurança e privacidade
- Funções extras

---

## 🆕 Sobre o Matter

**Matter** é um novo protocolo aberto de automação residencial desenvolvido pela **CSA (Connectivity Standards Alliance)** com apoio de grandes empresas como Apple, Google, Amazon e Samsung.

### Características:
- Foco em **interoperabilidade** e **privacidade**;
- Suporte local via **Thread**, **Wi-Fi** e **Ethernet**;
- Compatível com **Home Assistant nativamente** desde a versão 2023.11;
- Permite que dispositivos funcionem sem depender de nuvem;
- Espera-se rápida adoção por fabricantes nos próximos anos.

