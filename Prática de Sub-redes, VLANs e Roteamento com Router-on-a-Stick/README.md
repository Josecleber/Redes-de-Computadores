# Prática de Redes – Sub-redes, VLANs e Roteamento com Router-on-a-Stick

## Objetivo

Criar e configurar uma rede com **4 PCs** e **1 switch**, dividida em **4 sub-redes** derivadas da rede base **192.168.10.0/24** usando **máscara /26**. Simular a comunicação entre os dispositivos **sem** e **com roteador**, aplicando o conceito de **Router-on-a-Stick**.

---

## Topologia da Rede

- **4 PCs:** PC0, PC1, PC2, PC3  
- **1 Switch**  
- **1 Roteador** (adicionado posteriormente)

---

## Sub-redes Criadas (Máscara /26)

| Sub-rede | IPs Válidos                    | Broadcast          |
|----------|--------------------------------|--------------------|
| 1        | 192.168.10.1 – 192.168.10.62    | 192.168.10.63      |
| 2        | 192.168.10.65 – 192.168.10.126  | 192.168.10.127     |
| 3        | 192.168.10.129 – 192.168.10.190 | 192.168.10.191     |
| 4        | 192.168.10.193 – 192.168.10.254 | 192.168.10.255     |

Cada PC foi configurado manualmente com um IP de uma dessas sub-redes.

---

## Teste de Conectividade

### Sem Roteador
- PCs conectados ao mesmo switch **não conseguiram se comunicar**.
- Isso ocorre porque **switches não realizam roteamento** (operam na camada 2 do modelo OSI).

### Com Roteador (Router-on-a-Stick)
- Adicionou-se um roteador com **subinterfaces** configuradas na interface `G0/0` (uma por VLAN).
- O switch foi configurado com:
  - **Portas trunk** (ligação com o roteador)
  - **Portas access** (ligação com os PCs)
- Com a configuração correta:
  - **Todos os PCs passaram a se comunicar** entre si, mesmo em sub-redes diferentes.

---

## Conceitos Aplicados

- **Segmentação de redes com sub-redes (subnetting)**
- **VLANs** para separar logicamente os dispositivos
- **Router-on-a-Stick** para roteamento entre VLANs
- **Switch como dispositivo de camada 2**
- **Subinterfaces e encapsulamento 802.1Q (dot1Q)**

---

## Conclusão

Esta prática demonstrou:

- Como redes físicas podem ser logicamente segmentadas com VLANs.
- Que a comunicação entre sub-redes/VLANs exige um roteador.
- O uso de **Router-on-a-Stick** como solução prática e econômica.
- O papel de cada camada do modelo OSI em uma topologia realista.
- A importância de IPs, gateways e VLANs corretamente configurados.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
