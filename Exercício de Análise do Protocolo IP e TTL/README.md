# Exercício de Redes – Análise do Protocolo IP e TTL

## Objetivo

Investigar o funcionamento do **protocolo IP** e, em especial, o papel do campo **TTL (Time To Live)** no controle do tempo de vida dos pacotes IP durante a comunicação em uma rede.

---

## Topologia da Rede

**Dispositivos utilizados:**

- 3 PCs (PC0, PC1 e PC2)  
- 1 Switch

Todos os dispositivos estavam na mesma sub-rede, conectados ao switch.

---

## Endereçamento IP

- PC0: 192.168.1.1  
- PC1: 192.168.1.2  
- (IP do PC2 não especificado, mas não utilizado diretamente na simulação principal)

---

## Análise do Protocolo IP

Durante o teste com **ping de PC0 para PC1** no **modo Simulation** do Cisco Packet Tracer, foi possível observar o cabeçalho IP nos pacotes ICMP.

### Informações observadas:

- **IP de origem:** 192.168.1.1  
- **IP de destino:** 192.168.1.2  
- **TTL (Time To Live):** 128  
- **Protocolo:** 1 (ICMP)

---

## Testes com TTL Reduzido

### Cenário:

- O valor do **TTL foi manualmente configurado como 1**.
- O pacote chegou ao destino normalmente porque **a rede continha apenas switches**.

### Observação:

- **Switches operam na camada 2** do modelo OSI, portanto **não decrementam o TTL**.
- Para ver o TTL sendo decrementado e expirando, **um roteador seria necessário**.

---

## Conclusão

O exercício demonstrou:

- A estrutura básica do **cabeçalho IP**, com destaque para o campo TTL.
- A função do **TTL** como mecanismo de controle para evitar **loops infinitos**.
- Que **em redes somente com switches**, o TTL permanece inalterado.
- A necessidade de **roteadores (camada 3)** para simulações mais completas de TTL.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
