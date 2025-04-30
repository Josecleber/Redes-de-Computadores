# Projeto de Redes – Roteamento Inter-VLAN no Cisco Packet Tracer

## Descrição
Este projeto tem como objetivo criar e simular um cenário de rede no **Cisco Packet Tracer**, contendo dois setores distintos: **Administrativo** e **Financeiro**. Cada setor utiliza uma sub-rede e VLAN específicas, com comunicação entre eles sendo realizada por meio de **roteamento entre VLANs (Inter-VLAN Routing)**.

---

## Topologia da Rede

- **1 Roteador**
- **1 Switch central**
- **4 PCs**:
  - PC0 e PC1: Setor Administrativo (VLAN 10)
  - PC2 e PC3: Setor Financeiro (VLAN 20)

### Conexões
- Todos os PCs estão conectados ao switch.
- O switch está conectado ao roteador via **porta trunk**.

---

## Configuração de Rede

| Setor         | VLAN | Sub-rede            | Gateway         |
|---------------|------|---------------------|------------------|
| Administrativo| 10   | 192.168.10.0/24     | 192.168.10.1     |
| Financeiro    | 20   | 192.168.20.0/24     | 192.168.20.1     |

> O roteador foi configurado com **subinterfaces** na interface `GigabitEthernet0/0`, utilizando **encapsulamento 802.1Q (dot1Q)**.

### Switch
- **Fa0/1 e Fa0/2** → VLAN 10 (Administrativo)
- **Fa0/3 e Fa0/4** → VLAN 20 (Financeiro)
- **Gig0/1** → Configurada como **trunk**

---

## Testes Realizados

- Ping entre todos os PCs foi bem-sucedido (mesma VLAN e VLANs diferentes).
- O roteamento entre sub-redes funcionou corretamente.
- As VLANs segmentaram corretamente a comunicação.

---

## Análise OSI na Simulação

| Camada | Função Observada                                   |
|--------|----------------------------------------------------|
| 7 - Aplicação | Geração do ping (ICMP)                      |
| 4 - Transporte | Uso direto do ICMP                         |
| 3 - Rede | Endereçamento IP, roteamento entre VLANs         |
| 2 - Enlace | Encapsulamento em quadros, VLANs (802.1Q)      |
| 1 - Física | Transmissão dos bits pelos cabos               |

---

## Protocolos Observados

- **ICMP** – usado nos testes de conectividade (`ping`)
- **ARP** – resolução de endereços MAC na LAN
- **802.1Q** – encapsulamento de VLAN entre switch e roteador

---

## Desafios Enfrentados

- Configuração das **subinterfaces** no roteador com IPs e encapsulamento dot1Q
- Configuração correta da **porta trunk** no switch
- PCs inicialmente sem VLAN configurada corretamente
- Uso do comando `show ip interface brief` para diagnóstico de erros

---

## Conclusão

A simulação foi **bem-sucedida** e demonstrou, na prática:

- A segmentação de rede via VLANs
- O funcionamento do roteamento inter-VLAN
- A aplicação dos conceitos do modelo OSI
- A importância de configuração precisa e testes com comandos de verificação

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
