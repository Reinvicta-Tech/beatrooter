<p align="center">
  <img src="./assets/beatrooter_logo.svg" width="220" alt="BeatRooter logo">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Educational%20Use-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/platform-Linux%20%7C%20Windows%20%7C%20WSL-lightgrey.svg" alt="Platform">
  <img src="https://img.shields.io/badge/python-3.8%2B-blue.svg" alt="Python">
  <a href="RELEASE_v0.6.0.md">
    <img src="https://img.shields.io/badge/version-v0.6.0-22c55e.svg" alt="Version 0.6.0">
  </a>
  <img src="https://img.shields.io/badge/ui-PyQt6-8b5cf6.svg" alt="PyQt6">
</p>

> **BeatRooter** é uma plataforma visual para mapear, executar, documentar e compreender operações de cibersegurança. Foi criada para Red Team, Blue Team, Purple Team, aulas de Wargaming, laboratórios controlados e equipas que precisam de transformar caos técnico num cenário legível.

<p align="center">
  <strong>Beat roots. Beat them all. Be a BeatRooter.</strong>
</p>

---

## O que é

BeatRooter junta um **canvas operacional**, nós especializados, ferramentas externas, notas, evidências, relatórios, assistentes e um modo experimental de simulação. Em vez de espalhar resultados por terminais, ficheiros soltos e screenshots esquecidos, a aplicação organiza o engagement como um mapa vivo: alvos, serviços, vulnerabilidades, credenciais, observações, decisões, evidências e caminhos de ataque.

O objetivo é simples: ajudar uma equipa a ver o sistema, raciocinar sobre ele e agir com contexto.

<p align="center">
  <img src="./assets/exemploAtaque.png" width="900" alt="Exemplo de canvas BeatRooter">
</p>

---

## Destaques

- **Canvas visual de ataque e defesa** com nós, ligações dinâmicas, stackers, painel de detalhe e organização por cenários.
- **Biblioteca rica de nós** para assets, hosts, IPs, domínios, web apps, portas, serviços, vulnerabilidades, credenciais, evidências, notas, timelines, incidentes, TTPs, findings e planos de remediação.
- **Attack Path Builder** para estruturar cadeias de ataque, payloads, pivots, resultados e relatórios.
- **Tool Nodes** para executar ferramentas diretamente a partir do grafo e devolver resultados para o canvas.
- **BeatNote** para notas técnicas, categorias, contexto de trabalho e documentação dentro da aplicação.
- **Gnarl** como assistente/personagem do ecossistema BeatRooter, com painel, sprites e comportamento contextual.
- **CVSS v4 Calculator** integrado para avaliação rápida de severidade.
- **Wordlists** com presets, importação e ligação a ferramentas que precisam de listas.
- **Custom Nodes** para adaptar o grafo ao tipo de operação, laboratório ou metodologia da equipa.
- **Onboarding e preferências** para primeira configuração, idioma, aparência, atalhos e fluxo de trabalho.
- **UI bilingue** em Inglês e Português, com catálogo estruturado e camada de tradução para texto legado.

---

## Funcionalidades

### Canvas BeatRooter

O canvas é o centro da aplicação. Nele podes construir o mapa completo de uma operação:

- adicionar, editar, ligar, duplicar e organizar nós;
- representar infraestrutura, aplicações, endpoints, utilizadores, artefactos e findings;
- criar relações semânticas entre assets, observações, evidências e ações;
- usar stackers para agrupar máquinas, ambientes ou subconjuntos de investigação;
- guardar e restaurar projetos `.brt`;
- gerar snapshots e relatórios a partir da estrutura montada.

### Nós e relações

BeatRooter não trata tudo como uma nota genérica. O sistema tem tipos de nós para domínios diferentes:

| Família | Exemplos |
|---|---|
| Assets | IP, Host, Domain, Web Application, User, Credential, Infra Asset |
| Observações | Port/Service, Endpoint, DNS, Dynamic Trace, Behavior Analysis |
| Ataque | Attack, Attack Chain, Exploit, Payload, Lateral Movement, Privilege Escalation |
| Defesa | Control Gap, Containment Action, Hardening Task, Remediation Plan |
| Evidência | Screenshot, Forensic Artifact, Script, Binary Sample, Configuration File |
| Investigação | Investigation Note, Hypothesis, Incident Timeline, Triage Decision, Ticket |
| Especializados | Mobile Finding, Crypto Finding, Malware Sample, YARA Rules, Compliance Requirement |

### Attack paths e relatórios

O sistema de attack paths ajuda a transformar descobertas soltas numa narrativa operacional:

- liga etapas de ataque com contexto;
- acompanha evidências e resultados;
- estrutura payloads e transições;
- suporta relatórios de caminho de ataque;
- torna a progressão mais fácil de explicar a uma equipa técnica ou a uma audiência defensiva.

### Ferramentas integradas

BeatRooter inclui uma camada de execução e gestão de ferramentas. Os tool nodes podem receber contexto do canvas, executar comandos e anexar resultados.

| Área | Ferramentas |
|---|---|
| Network / Infra | Nmap, Masscan, Enum4linux, RPCClient, Netcat, Hydra |
| Web / DNS | Gobuster, WhatWeb, SQLMap, DNS Utils, Subfinder, Amass, Whois |
| File / Reverse / Forensics | ExifTool, Binwalk, Strings, Steghide, John the Ripper, Hashcat, Ghidra |
| Capture / Traffic | TShark |
| Research / Search | Searchsploit |
| Generation / Wordlists | CUPP |

> As ferramentas devem ser usadas apenas em ambientes próprios, laboratórios, CTFs ou sistemas onde exista autorização explícita.

### BeatNote

BeatNote é o bloco de notas operacional do BeatRooter:

- notas por categoria;
- painel integrado no workspace;
- diálogo dedicado para escrita e revisão;
- serviço próprio para gerir conteúdo;
- ligação natural a nós, findings e documentação do engagement.

### Gnarl

Gnarl é a presença assistiva e visual do BeatRooter. O módulo inclui:

- painel flutuante;
- sprites e estados visuais;
- interação contextual;
- integração com cenários;
- base para assistência mais inteligente dentro do workspace.

### CVSS v4

A calculadora CVSS v4 permite avaliar severidade sem sair do fluxo de trabalho. É útil para triagem, priorização e documentação de findings técnicos.

### Idiomas

BeatRooter mantém Inglês e Português em paralelo. A camada de idioma combina:

- catálogos JSON estruturados;
- gestor de idioma;
- compatibilidade para texto Qt legado;
- seleção de idioma em preferências.

---

## Em desenvolvimento

### BeatBox / Sandbox

**BeatBox** é a linha experimental do BeatRooter para simulação e treino. A ideia é criar ambientes controlados onde o utilizador possa montar, observar e testar cenários sem tocar em produção.

O trabalho atual está dividido em três caixas:

| BeatBox | Objetivo |
|---|---|
| `NETWORK-BB` | simulação e composição de redes, ligações e tráfego |
| `OS-BB` | representação de sistemas, estados, processos e superfícies locais |
| `WEB-BB` | simulação de aplicações web, endpoints e caminhos de exploração |

Dentro da aplicação, o módulo `features/sandbox` já contém a base visual e funcional para:

- workspaces de rede, sistema operativo e web;
- objetos de sandbox;
- ligações entre objetos;
- toolbox dedicada;
- painel de detalhe;
- ações de undo/redo;
- motor de estado e tracing de rede.

BeatBox ainda é uma frente em evolução, mas aponta para um futuro forte: aprender, treinar, demonstrar e validar cenários dentro de um laboratório visual.

### Roadmap técnico próximo

- melhorar integração entre resultados de ferramentas e nós especializados;
- consolidar relatórios por cenário;
- expandir custom nodes e templates;
- amadurecer BeatBox/Sandbox;
- fortalecer testes automatizados de UI e core;
- melhorar instalação e deteção de ferramentas em Linux, Windows e WSL.

---

## Estrutura do projeto

```text
BeatRooter/
  main.py                         # entrada PyQt6
  features/
    beatroot_canvas/              # workspace visual principal
      core/                       # grafo, storage, templates, attack paths, validação
      models/                     # modelos de graph/node/edge
      ui/                         # janela, canvas, toolbox, painéis, dialogs, pintura
    beatnote/                     # notas e documentação operacional
      core/
      ui/
    tools/                        # gestão, execução e parsing de ferramentas externas
      core/
      contexts/
      docker/
      integrations/
      parsers/
      agents/
    gnarl/                        # assistente visual e integrações
    cvss/                         # calculadora CVSS v4
    wordlists/                    # presets e importação de wordlists
    onboarding/                   # wizard inicial e preferências
    language/                     # catálogos EN/PT e tradução legada
    sandbox/                      # BeatBox/Sandbox experimental
assets/                           # logos, imagens e assets visuais
docs/                             # documentação técnica
tests/projects/                   # testes por feature
BeatBox/                          # protótipos NETWORK-BB, OS-BB e WEB-BB
```

---

## Instalação

### Requisitos

- Python 3.8+
- PyQt6
- Linux, Windows ou WSL
- Ferramentas externas opcionais conforme o tipo de operação

### Ambiente local

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python BeatRooter/main.py
```

Em Windows, ativa o ambiente virtual com:

```powershell
.\.venv\Scripts\activate
python BeatRooter\main.py
```

### Testes

```bash
QT_QPA_PLATFORM=offscreen python -m unittest discover -s tests/projects -p "test_*.py"
QT_QPA_PLATFORM=offscreen python -m unittest tests.projects.beatnote.test_beatnote_service
QT_QPA_PLATFORM=offscreen python -m unittest tests.projects.language.test_language_manager
```

---

## Fluxo de trabalho

1. Cria ou abre um projeto `.brt`.
2. Adiciona assets, serviços, observações e evidências ao canvas.
3. Liga nós para representar relações reais: origem, alvo, serviço, vulnerabilidade, credencial, exploração, contenção.
4. Executa ferramentas quando precisares de dados novos.
5. Usa BeatNote para registar decisões, hipóteses e notas técnicas.
6. Constrói attack paths para explicar progressão, impacto e recomendações.
7. Exporta ou apresenta o cenário como documentação viva.

---

## Casos de uso

### Red Team

- reconhecimento de redes e aplicações;
- mapeamento de superfície de ataque;
- organização de vulnerabilidades e credenciais;
- documentação de exploração e pós-exploração;
- geração de narrativas técnicas para relatório.

### Blue Team

- inventário visual de infraestrutura;
- análise de exposição;
- triagem de findings;
- planeamento de hardening;
- simulação de resposta a incidentes.

### Purple Team

- alinhar ataque, deteção e remediação no mesmo mapa;
- validar hipóteses de deteção;
- identificar falhas de cobertura;
- repetir cenários com evidência comparável.

### Educação, CTF e Wargaming

- treinar pensamento adversarial;
- criar laboratórios visuais;
- explicar cadeias técnicas a estudantes;
- transformar exercícios em mapas reutilizáveis.

---

## Pequeno manifesto

<table>
<tr>
<td valign="top" width="50%">

**`canvas/operation.brt`** &nbsp; <sub><i>map it</i></sub>

```text
Target
  -> Host
  -> Port / Service
  -> Finding
  -> Exploit
  -> Credential
  -> Lateral Movement
  -> Evidence
  -> Report
```

</td>
<td valign="top" width="50%">

**`beatrooter/method.md`** &nbsp; <sub><i>beat it</i></sub>

```markdown
1. See the system.
2. Connect the facts.
3. Test with permission.
4. Keep the evidence.
5. Explain the path.
6. Improve the defense.
```

</td>
</tr>
</table>

---

## Segurança e uso responsável

BeatRooter foi criado para aprendizagem, investigação, laboratórios e trabalho autorizado. Muitas ferramentas integradas podem produzir tráfego ofensivo, executar enumeração agressiva ou manipular artefactos sensíveis.

Usa apenas em:

- sistemas teus;
- ambientes de laboratório;
- CTFs e wargames;
- auditorias com autorização explícita;
- atividades defensivas dentro do teu âmbito.

Não uses BeatRooter para atacar, testar ou enumerar sistemas de terceiros sem permissão.

---

## Contribuir

Contribuições são bem-vindas, especialmente nas áreas de:

- templates de nós;
- parsers de resultados;
- integração de ferramentas;
- melhorias de UI/UX;
- testes automatizados;
- documentação;
- BeatBox/Sandbox.

Guidelines rápidas:

- mantém alterações focadas;
- evita credenciais, paths pessoais e ficheiros `.brt` acidentais;
- adiciona testes quando mexeres em comportamento partilhado;
- quando mudares texto visível na UI, atualiza Inglês e Português;
- usa mensagens de commit curtas e imperativas.

---

## Equipa de desenvolvimento

<div align="center">
  <a href="https://github.com/Samucahub/BeatRooter/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=Samucahub/BeatRooter" alt="BeatRooter contributors">
  </a>
</div>

---

## Agradecimentos

- **ISTEC** e o contexto de Wargaming que deu origem ao projeto.
- **Comunidade Open Source**, pelos projetos, ferramentas e conhecimento partilhado.
- **MITRE ATT&CK**, pela linguagem comum sobre táticas, técnicas e procedimentos.
- **OWASP**, pelas metodologias e referências de segurança aplicacional.
- Todas as pessoas que testam, partem, corrigem e melhoram o BeatRooter.

---

## Licença

Este projeto está disponibilizado para fins educacionais. Redistribuição, uso comercial ou uso fora desse contexto deve respeitar a autorização dos autores e a legislação aplicável.

---

<div align="center">

**Visualiza. Mapeia. Ataca. Defende.**

Made with coffee by the BeatRooter team.

</div>
