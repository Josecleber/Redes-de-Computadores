# Prática de Redes – DNS, HTTP e Captura TCP com netcat/tcpdump

## Parte 1 – Simulação de Cliente, DNS e HTTP no Packet Tracer

### Objetivo

Simular em uma rede local o funcionamento de **requisições DNS e HTTP**, utilizando um cliente, um servidor DNS e um servidor HTTP interligados por um roteador.

---

### Topologia

- 1 PC (cliente)
- 2 Servidores (DNS e HTTP)
- 1 Switch
- 1 Roteador

---

### Configurações

- O servidor DNS foi configurado com uma entrada para `site.com`, apontando para o IP do servidor HTTP.
- O cliente acessou a página via navegador utilizando o nome de domínio.
- Durante a montagem, foi necessário substituir o PC cliente por falha na resolução de nomes.

---

### Análise com Simulation Mode

- Visualização do tráfego DNS: `DNS Request` e `DNS Reply`
- Visualização do tráfego HTTP: `HTTP Request` e `HTTP Response`
- Camadas observadas: **Aplicação**, **Transporte** e **Rede**

---

### Conclusão Parte 1

A simulação validou o funcionamento dos protocolos DNS e HTTP em uma topologia simples e reforçou o entendimento prático da comunicação cliente-servidor em redes locais.

---

## Parte 2 – Simulação Real com netcat + tcpdump

### Objetivo

Demonstrar a comunicação **TCP** real entre duas VMs usando `netcat`, e capturar os pacotes da conexão usando `tcpdump`.

---

### Etapas

- Configuração de IP nas VMs
- Instalação das ferramentas `netcat` e `tcpdump`
- Estabelecimento de conexão TCP entre as máquinas com `nc`
- Captura dos pacotes da sessão TCP em tempo real com `tcpdump`

---

### Conclusão Parte 2

A atividade comprovou o funcionamento real da pilha de protocolos TCP/IP. A captura dos pacotes permitiu observar os **handshakes TCP**, os dados trafegando, e entender o papel das **camadas de transporte e rede** no tráfego real.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
