# Prática de Redes – Análise do Three-Way Handshake TCP

## Objetivo

Demonstrar como ocorre a **inicialização de uma conexão TCP** entre duas máquinas reais, por meio do **Three-Way Handshake**, utilizando:

- `netcat` para simular cliente e servidor TCP
- `tcpdump` para capturar e analisar os pacotes da conexão

---

## Ambiente Utilizado

- **2 VMs Xubuntu** rodando no **VirtualBox**
- Ambas configuradas em **rede Host-Only**
- Ferramentas instaladas:
  - `netcat`
  - `tcpdump`

---

## Configuração

- **VM1** atua como **servidor TCP** com `netcat`
- **VM2** atua como **cliente TCP**, conectando-se ao IP da VM1
- A comunicação foi testada com envio de uma mensagem simples

---

## Captura dos Pacotes TCP

Durante a execução, o `tcpdump` foi utilizado para capturar os pacotes da conexão.

### Pacotes observados:
- **SYN** – Início da conexão pelo cliente
- **SYN-ACK** – Resposta do servidor
- **ACK** – Confirmação final do cliente

Esse processo constitui o **Three-Way Handshake**, fundamental para a confiabilidade do protocolo TCP.

---

## Conclusão

O exercício comprovou:

- O funcionamento do processo de **handshake TCP** entre cliente e servidor
- A importância do protocolo TCP para conexões **confiáveis e ordenadas**
- A aplicação prática da **Camada 4 – Transporte** do modelo OSI
- O uso de ferramentas reais como `netcat` e `tcpdump` para visualização e análise de tráfego

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
