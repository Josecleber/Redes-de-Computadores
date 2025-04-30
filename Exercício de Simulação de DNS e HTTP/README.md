# Exercício de Redes – Simulação de DNS e HTTP no Cisco Packet Tracer

## Objetivo

Simular uma requisição DNS e o acesso via HTTP no **Cisco Packet Tracer**, analisando o **fluxo de protocolos envolvidos** e o impacto quando o **servidor DNS está fora do ar**.

---

## Topologia da Rede

**Dispositivos utilizados:**
- 2 PCs (PC0 e PC1)
- 1 Servidor Web e DNS (integrado)
- 1 Roteador (Router0)

---

## Configuração de Rede

- O roteador (`Router0`) conecta os PCs à rede onde está o servidor.
- O **servidor Web/DNS** está configurado com um IP fixo e responde:
  - Requisições DNS (resolvendo nomes como `site.com`)
  - Requisições HTTP (acesso ao site)

> O IP exato não foi especificado no PDF, mas foi simulado corretamente.

---

## Teste de Acesso

1. Os PCs tentaram acessar o site por **nome de domínio** (ex: `site.com`).
2. O navegador acionou o **servidor DNS** para resolver o nome para um IP.
3. Com o IP obtido, o navegador enviou uma requisição **HTTP** ao servidor.
4. O servidor respondeu com o conteúdo do site.

---

## Captura em Simulation Mode

Durante a simulação passo-a-passo foi observado o uso dos seguintes protocolos:

| Protocolo | Finalidade                 | Camada TCP/IP        |
|-----------|----------------------------|-----------------------|
| DNS       | Resolução de nomes         | Aplicação             |
| HTTP      | Requisição e entrega de site| Aplicação            |
| TCP       | Transporte confiável        | Transporte            |
| IP        | Endereçamento e roteamento | Internet              |
| Ethernet  | Transmissão local           | Acesso à Rede (Link)  |

---

## O que acontece se o DNS estiver fora do ar?

- O navegador **não consegue resolver o nome** (ex: `site.com`) para IP.
- Mesmo que o servidor HTTP esteja ativo, **o site não carrega**.
- A comunicação **falha na etapa de DNS**, impedindo o prosseguimento.

---

## Conclusão

A atividade demonstrou com clareza:

- O papel do **DNS como dependência para acesso web**.
- A ordem dos protocolos usados em uma requisição HTTP.
- O impacto direto da falha de DNS na experiência do usuário.
- A importância de simular situações reais em laboratório.

---

## Autor
José Cleber Alves da Cruz Mendes  
Curso: Engenharia da Computação – Uniube
