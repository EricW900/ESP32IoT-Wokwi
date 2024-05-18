# ESP32 DHT22 MQTT Publisher

Este projeto demonstra como utilizar um ESP32 para ler dados de um sensor de temperatura e umidade DHT22 e publicar esses dados em um broker MQTT. 

## Sumário

- [Descrição](#descrição)
- [Pré-requisitos](#pré-requisitos)
- [Configuração](#configuração)
- [Acesso](#acesso)
- [Uso](#uso)
  
## Descrição

Este projeto é um exemplo de IoT que utiliza um ESP32 para coletar dados de um sensor DHT22 e enviar essas informações para um broker MQTT. Ele inclui a configuração de rede WiFi e a reconexão automática ao broker MQTT em caso de falhas na conexão.

## Pré-requisitos

Antes de começar, você precisará ter o seguinte instalado:

- [Arduino IDE](https://www.arduino.cc/en/Main/Software)
- [Biblioteca DHT](https://github.com/adafruit/DHT-sensor-library)
- [Biblioteca PubSubClient](https://pubsubclient.knolleary.net/)
- [Biblioteca LittleFS](https://github.com/lorol/LITTLEFS)

## Configuração

Antes de carregar o código no ESP32, configure as seguintes constantes no código:

- **SSID**: Nome da sua rede WiFi.
- **PASSWORD**: Senha da sua rede WiFi.
- **BROKER_MQTT**: URL do broker MQTT.
- **MQTT_USERNAME**: Nome de usuário para autenticação MQTT.
- **MQTT_PSWD**: Senha para autenticação MQTT.

```
const char *SSID = "SuaRede";
const char *PASSWORD = "SuaSenha";
const char *BROKER_MQTT = "URLdoBrokerMQTT";
const char* MQTT_USERNAME = "UsernameMQTT";
const char* MQTT_PSWD = "SenhaMQTT";
```

## Acesso

1. Acesse este link:

```
https://wokwi.com/projects/397343259758912513
```

## Uso

Após carregar o código, o ESP32 irá:

1. Conectar-se à rede WiFi configurada.
2. Conectar-se ao broker MQTT configurado.
3. Ler a temperatura e umidade do sensor DHT22.
4. Publicar os dados de temperatura no tópico MQTT configurado.

Você pode monitorar a saída serial para ver as leituras de temperatura e umidade e as mensagens de depuração relacionadas à conexão WiFi e MQTT.
