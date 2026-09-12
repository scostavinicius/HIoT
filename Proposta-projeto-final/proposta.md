# Proposta de Projeto

**Disciplina:** Plataformas de Hardware para IoT

**Aluno:** Vinicius Costa Soares

**Título:** Monitoramento remoto de temperatura com controle de climatização via ESP32

---

## 1. Descrição

O projeto consiste em um dispositivo que mede a temperatura de um ambiente e envia essa informação ao usuário pela internet, permitindo também que ele ligue ou desligue a climatização à distância.

A ideia surge de uma situação comum: o usuário só percebe que o ambiente está desconfortável quando chega nele, ou deixa o aparelho ligado sem necessidade. O problema se encaixa bem em IoT porque reúne os três elementos da área — sensoriamento do ambiente, comunicação dos dados por rede e atuação remota.

## 2. Objetivos

- Ler a temperatura do ambiente periodicamente com um sensor digital.
- Enviar as leituras pela rede Wi-Fi usando o protocolo MQTT.
- Exibir os dados ao usuário em um painel acessível remotamente.
- Permitir o acionamento remoto da climatização pelo mesmo painel.

## 3. Arquitetura

O ESP32 lê o sensor e publica o valor em um tópico MQTT, que o painel exibe ao usuário. No sentido inverso, o comando acionado no painel é publicado em outro tópico, recebido pelo ESP32 e convertido em um sinal infravermelho enviado ao ar-condicionado — o mesmo sinal que o controle remoto original emitiria.

## 4. Componentes

| Componente | Função |
|---|---|
| ESP32 DevKit V1 | Leitura, processamento e comunicação Wi-Fi |
| Sensor DHT22 | Medição de temperatura e umidade |
| LED emissor infravermelho | Envio dos comandos ao ar-condicionado |
| Receptor infravermelho TSOP1838 | Captura dos códigos do controle original (fase de desenvolvimento) |
| Protoboard, jumpers e resistores | Montagem do protótipo |

O ESP32 foi escolhido por já trazer Wi-Fi integrado, dispensando módulo externo. O MQTT foi escolhido por ser o protocolo padrão em IoT: leve, com baixo overhead e baseado em publicação/assinatura, o que desacopla o dispositivo do painel.

## 5. Ferramentas

Firmware em C++ pela Arduino IDE, usando as bibliotecas `DHT sensor library` (sensor), `PubSubClient` (MQTT) e `IRremoteESP8266` (infravermelho). O broker será o Mosquitto e o painel será montado no Node-RED.

## 6. Etapas previstas

| Etapa | Atividade |
|---|---|
| 1 | Montagem do circuito e leitura do sensor no monitor serial |
| 2 | Conexão Wi-Fi e publicação das leituras via MQTT |
| 3 | Construção do painel e recebimento dos comandos no dispositivo |
| 4 | Decodificação dos códigos IR e acionamento da climatização |
| 5 | Testes, documentação e entrega |

## 7. Resultados esperados

Um protótipo funcional em que a temperatura do ambiente apareça no painel remoto com poucos segundos de atraso e um comando enviado pelo painel acione efetivamente a climatização.

O principal risco é o aparelho de ar-condicionado usar um protocolo infravermelho não suportado pela biblioteca. Nesse caso, a alternativa é acionar um ventilador por meio de um módulo relé.