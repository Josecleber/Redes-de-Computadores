# Exercício de Redes – Análise do Protocolo ARP e Conflito de IP

## Objetivo

Observar, por meio de simulação no **Cisco Packet Tracer**, como o **protocolo ARP (Address Resolution Protocol)** é utilizado para mapear endereços IP para endereços MAC em uma rede local. Também foi analisado o impacto causado por **endereços IP duplicados**.

---

## Topologia da Rede

**Dispositivos utilizados:**
- 3 PCs (PC0, PC1, PC2)
- 1 Switch

**Conexões:**
- Cada PC conectado ao switch via **cabo de cobre direto**.

---

## Configuração de IP

| Dispositivo | Endereço IP     | Máscara de Sub-rede   |
|-------------|------------------|------------------------|
| PC0         | 192.168.1.10     | 255.255.255.0          |
| PC1         | 192.168.1.11     | 255.255.255.0          |
| PC2         | 192.168.1.12     | 255.255.255.0          |

---

## Testes Realizados

- **Testes de conectividade** com `ping` entre os PCs foram realizados com sucesso.
- Foi observada a **população das tabelas ARP** à medida que os pacotes eram trocados.

---

## Observações sobre o ARP

- As **tabelas ARP** em cada PC mostraram o mapeamento de IPs para endereços MAC.
- Em **modo simulação**, foi possível acompanhar visualmente como os pacotes ARP são enviados e respondidos.

---

## Impacto de IP Duplicado

Quando dois dispositivos foram configurados com o **mesmo endereço IP**, observou-se:

- **Conflito de endereço IP**, com pacotes sendo enviados para o dispositivo errado.
- **Respostas inconsistentes** ou falhas completas na comunicação.
- **Tabelas ARP instáveis**, dificultando o diagnóstico.
- Em alguns sistemas, ocorreu a exibição de mensagens como: `IP conflict detected`.

---

## Conclusão

O experimento demonstrou na prática:

- A importância do protocolo ARP na resolução de endereços.
- Como conflitos de IP podem prejudicar seriamente a comunicação em redes locais.
- A utilidade do **modo simulação** do Packet Tracer para observar protocolos em tempo real.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
