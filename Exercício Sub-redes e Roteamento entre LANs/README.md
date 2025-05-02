# Exercício de Redes – Sub-redes e Roteamento entre LANs

## Objetivo

Realizar o **subendereçamento da rede 192.168.100.0/25** e simular duas sub-redes conectadas por um roteador no **Cisco Packet Tracer**. O objetivo é compreender a divisão de redes IP, o conceito de broadcast, e o roteamento básico entre LANs.

---

## Sub-redes Calculadas

Endereço base: **192.168.100.0/25**  
Divisão em **duas sub-redes**:

| Sub-rede | IP da Rede       | IPs Válidos                      | Broadcast         |
|----------|------------------|----------------------------------|-------------------|
| 1        | 192.168.100.0     | 192.168.100.1 – 192.168.100.126  | 192.168.100.127   |
| 2        | 192.168.100.128   | 192.168.100.129 – 192.168.100.254| 192.168.100.255   |

Cada sub-rede possui **128 IPs totais**, sendo **126 válidos para hosts**.

---

## O que é Broadcast?

> O **endereço de broadcast** é o último IP de uma sub-rede e serve para enviar mensagens simultaneamente a **todos os dispositivos** da mesma rede. É utilizado por protocolos como **ARP** para descobertas iniciais, como:  
> “Ei, quem tem esse IP?”

---

## Topologia Simulada no Packet Tracer

**Dispositivos utilizados:**
- 1 Roteador
- 2 Switches
- 4 PCs (2 por sub-rede)

### Objetivo da simulação:
Conectar duas sub-redes distintas usando um roteador e testar a comunicação entre elas.

---

## Configuração

**Sub-rede 1:**  
- 2 PCs com IPs da faixa `192.168.100.1 – 192.168.100.126`  
- Gateway: `192.168.100.1`  

**Sub-rede 2:**  
- 2 PCs com IPs da faixa `192.168.100.129 – 192.168.100.254`  
- Gateway: `192.168.100.129`

**Roteador:**  
- 2 interfaces configuradas com IPs das respectivas sub-redes  
- Roteamento direto ativado

---

## Testes Realizados

- Os **PCs de uma sub-rede conseguiram se comunicar** com os da outra após configuração correta do roteador.
- O **ping** entre PCs de redes diferentes foi bem-sucedido, comprovando o funcionamento do roteamento.

---

## Conclusão

O exercício demonstrou na prática:

- A divisão de redes com sub-rede CIDR (`/25`)
- O uso e entendimento do **broadcast**
- O **roteamento entre LANs distintas**
- A importância de gateways e IPs corretamente atribuídos

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
