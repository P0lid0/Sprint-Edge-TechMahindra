# Sprint-Edge-TechMahindra

Guilherme - 554962
Pedro - 555556
Fabrício - 558216
Vitor - 554893
Matheus - 555447

Projeto IoT para Monitoramento de Pista e Alertas de Voltas
Descrição do Projeto
Este projeto consiste em um sistema IoT que monitora as condições ambientais de uma pista de corrida da Fórmula E, utilizando sensores de temperatura, umidade e proximidade. Através de um dispositivo com um sensor DHT22 (para captar temperatura e umidade), um sensor PIR (detector de movimento) e um buzzer, o sistema envia dados para um dispositivo remoto via Wi-Fi e oferece alertas em tempo real. O sensor PIR detecta a passagem de objetos, como carros, e ativa o buzzer para indicar a conclusão de uma volta.

Funcionalidades Principais:
Medição da temperatura e umidade da pista de corrida.
Estimativa das condições da pista com base nos dados de umidade e temperatura.
Detecção de movimento com o sensor PIR.
Alerta sonoro através do buzzer ao detectar uma volta completa.
Comunicação Wi-Fi com um servidor remoto para monitoramento em tempo real.

Arquitetura Proposta
Dispositivos IoT:
DHT22: Sensor de temperatura e umidade que coleta dados da pista.
PIR: Sensor de movimento que detecta a passagem de um objeto (carro) para indicar a conclusão de uma volta.
Buzzer: Ativado pelo sensor PIR quando uma volta é detectada.
Back-end:
Servidor Remoto: Recebe os dados dos sensores (temperatura, umidade, e estado do PIR) através de uma conexão Wi-Fi. Processa os dados e os armazena para visualização e análise posterior.
Front-end:
Dashboard de Monitoramento: Interface web ou aplicativo que exibe em tempo real os dados enviados pelo dispositivo IoT. Apresenta gráficos de temperatura e umidade e ativa notificações visuais quando uma volta é completada.
Fluxo de Dados:
O dispositivo IoT coleta a temperatura e umidade da pista e envia os dados para o servidor.
Quando o sensor PIR detecta movimento, o buzzer é ativado e uma mensagem é enviada ao servidor indicando a conclusão da volta.
O servidor processa os dados e exibe as informações no front-end, alertando os operadores das condições da pista e o progresso das voltas.

Recursos Necessários
Dispositivos IoT:
Sensor DHT22: Para medir temperatura e umidade.
Sensor PIR: Para detectar movimento.
Buzzer: Para emitir o alerta sonoro.
Microcontrolador com Wi-Fi (como ESP8266 ou ESP32): Para coletar dados dos sensores e enviar via Wi-Fi.
Back-end:
Servidor Web: Pode ser um servidor local ou na nuvem para receber, armazenar e processar os dados. Linguagens comuns para o servidor incluem Node.js, Python (Flask, Django), ou qualquer serviço que aceite requisições HTTP.
Front-end:
Dashboard: Desenvolvido em HTML, CSS, JavaScript ou frameworks como React ou Vue.js, para exibir os dados de maneira visual. Ferramentas como Chart.js podem ser usadas para gráficos de temperatura e umidade.
Dependências:
Bibliotecas para o sensor DHT22 e PIR no microcontrolador.
Conexão Wi-Fi configurada no dispositivo para envio dos dados.
Servidor configurado para receber requisições HTTP e armazenar os dados (banco de dados como SQLite, MySQL, etc.).
Hospedagem da interface gráfica (local ou na nuvem).
Instruções de Uso
Configuração do Dispositivo IoT:
Conecte o DHT22, PIR e o buzzer ao microcontrolador conforme o esquema de pinos.
Configure a rede Wi-Fi no código do microcontrolador para se conectar ao servidor.
Compile e faça o upload do código para o microcontrolador.
Inicie o sistema, que começará a coletar dados e enviar para o servidor.
Configuração do Back-end:
Configure o servidor para aceitar requisições HTTP do dispositivo IoT.
Armazene os dados recebidos em um banco de dados.
Configure o servidor para fornecer os dados para o front-end em tempo real.
Configuração do Front-end:
Configure o dashboard para se conectar ao back-end e obter os dados em tempo real.
Exiba gráficos de temperatura e umidade, e inclua alertas visuais para a conclusão de voltas.

Requisitos e Dependências
Microcontrolador compatível com Wi-Fi (ESP8266, ESP32).
Sensor DHT22 e Sensor PIR.
Bibliotecas: DHT e Adafruit_Sensor para o DHT22, e PIRSensor para o PIR.
Servidor web (Node.js, Flask, etc.).
Dashboard em HTML/JavaScript com suporte a gráficos.
