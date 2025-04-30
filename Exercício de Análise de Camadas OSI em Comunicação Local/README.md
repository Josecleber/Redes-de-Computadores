# Exercício de Redes – Análise de Camadas OSI em Comunicação Local

## Objetivo

Analisar os **protocolos envolvidos na comunicação de pacotes entre dois PCs** em um ambiente de rede local simulado no **Cisco Packet Tracer**, com foco na **visualização das camadas OSI** envolvidas.

---

## Topologia da Rede

- **2 PCs** conectados a um **Switch**
- **Switch** conectado a um **Roteador**
- Todos os dispositivos configurados na **mesma sub-rede**

---

## Configuração da Rede

- PCs e roteador foram configurados com endereços IP válidos da mesma sub-rede.
- A configuração do gateway permitiu a comunicação adequada via roteador.
- Não há dados específicos no relatório sobre os IPs usados, mas foi validada a comunicação.

---

## Teste de Comunicação

- Foi utilizado o comando **`ping`** para testar a conectividade entre os PCs.
- A simulação mostrou o envio e recebimento de pacotes ICMP com sucesso.

---

## Visualização das Camadas OSI

Durante a simulação com **modo passo-a-passo (Simulation Mode)**, observou-se:

| Camada OSI | Nome               | Protocolo / Observações              |
|------------|--------------------|--------------------------------------|
| 7          | Aplicação          | ICMP (ping)                          |
| 6          | Apresentação       | - (não usada com ICMP)               |
| 5          | Sessão             | - (não usada com ICMP)               |
| 4          | Transporte         | - (ICMP não usa TCP/UDP)             |
| 3          | Rede               | IP                                   |
| 2          | Enlace de Dados    | Ethernet                             |
| 1          | Física             | Transmissão elétrica via cabos       |

---

## Camada que Detecta Erros de Transmissão

- A **Camada 2 – Enlace de Dados** é responsável por detectar pacotes corrompidos por meio de **FCS (Frame Check Sequence)**.
- Quando um erro é identificado, o pacote é descartado e não chega à camada superior.

---

## Conclusão

A atividade demonstrou na prática:

- Como montar e testar uma rede local no Packet Tracer.
- O papel de cada camada OSI durante a comunicação.
- Como o protocolo ICMP atua diretamente da aplicação até a camada física.
- A importância da camada de enlace na **detecção e tratamento de erros**.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
