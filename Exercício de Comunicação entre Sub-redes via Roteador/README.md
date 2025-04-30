# Exercício de Redes – Comunicação entre Sub-redes via Roteador

## Objetivo

Compreender como um **roteador** permite a **comunicação entre redes diferentes**, cada uma com **sub-redes distintas**, e como configurações incorretas (como máscaras erradas) podem afetar essa comunicação.

---

## Topologia da Rede

- Dois PCs (**PC0** e **PC1**)
- Um **roteador** interligando os dois PCs
- Cada PC configurado em uma **sub-rede diferente**
- Conexões realizadas diretamente ao roteador ou via switches intermediários (não especificado)

---

## Configuração dos Dispositivos

Embora os IPs não tenham sido especificados no relatório, os testes foram feitos com **endereçamentos de sub-redes diferentes**, o que requer um roteador para permitir a comunicação.

---

## Testes de Comunicação

- Foi utilizado **ping** entre os PCs.
- A comunicação funcionou **somente** quando:
  - O roteador estava corretamente configurado.
  - As **máscaras de sub-rede estavam corretas**.
- Em caso de erro (ex: máscara mal configurada ou roteador desconectado), o ping **falhou**.

---

## Análise: Máscara de Sub-rede Incorreta

- Quando a **máscara de sub-rede está errada**, os dispositivos acreditam estar na mesma rede, mesmo estando em redes diferentes.
- Isso faz com que **o PC tente enviar pacotes diretamente para o outro**, sem passar pelo roteador.
- Resultado: **o pacote não chega ao destino** e ocorre **falha na comunicação**.

---

## Conclusão

A atividade demonstrou:

- A importância de um **roteador** para a comunicação entre sub-redes distintas.
- O papel fundamental da **máscara de sub-rede correta** para o roteamento.
- Como erros simples de configuração impedem a entrega de pacotes.
- A utilidade do **ping** como ferramenta de diagnóstico de rede.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
