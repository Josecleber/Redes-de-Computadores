# Projeto de Redes – Acesso via IP e DNS no Cisco Packet Tracer

## Descrição

Este projeto simula uma rede local no **Cisco Packet Tracer** com o objetivo de permitir o acesso a um site tanto por **IP** quanto por **nome DNS**, utilizando um **servidor local** configurado com os serviços **HTTP** e **DNS**.

Além disso, o projeto relaciona os protocolos utilizados com as respectivas camadas do **modelo TCP/IP**.

---

## Topologia da Rede

- **3 PCs**: PC1, PC2 e PC3
- **1 Switch**
- **1 Servidor Web (Server0)**

---

## Endereçamento IP

O servidor Web foi configurado com IP fixo **192.168.1.100**, utilizado tanto para o acesso direto quanto para associação DNS.

---

## Configuração do Servidor

No **Server0** foram ativados:

- **Serviço HTTP**
- **Serviço DNS**

### Entrada DNS criada:
- **Nome:** `www.siteempresa.com`
- **IP:** `192.168.1.100`

---

## Testes de Acesso

### Acesso via IP:
- PCs acessaram o servidor pelo endereço `192.168.1.100` com sucesso.

### Acesso via Nome DNS:
- Após a entrada DNS, os PCs acessaram o site com o nome `www.siteempresa.com`.

---

## Modelo TCP/IP e Protocolos Utilizados

| Protocolo | Função                               | Camada TCP/IP         |
|-----------|--------------------------------------|------------------------|
| **HTTP**  | Solicitação e entrega de páginas     | Aplicação              |
| **DNS**   | Resolução de nomes para IPs          | Aplicação              |
| **TCP**   | Transporte confiável dos dados       | Transporte             |
| **IP**    | Encaminhamento entre dispositivos    | Internet               |
| **Ethernet** | Comunicação dentro da LAN        | Acesso à Rede (Link)   |

---

## Considerações Finais

- O funcionamento do acesso via IP e via nome DNS foi validado com sucesso.
- A simulação demonstrou como os serviços **DNS** e **HTTP** atuam em conjunto.
- O projeto reforça a compreensão das **camadas TCP/IP** e a importância da **resolução de nomes em redes**.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
