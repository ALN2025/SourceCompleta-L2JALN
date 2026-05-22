# SourceCompleta-L2JALN

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

**SOURCE + PATCH + PACK** — ecossistema completo para servidores Lineage II baseados em L2J, desenvolvido e evoluído pela **L2JALN** (Team-L2JALN / DeV A.L.N).

> Este repositório contém o **código-fonte** e a documentação de build.  
> Na secção **Releases** deste repositório você encontra o pacote pronto para uso: **source**, **patch**, **site**, **pack** e **programas** auxiliares.

---

## Sobre o projeto

Em **2017**, este trabalho começou a partir de uma base open source de servidor L2J — na época, sem estrutura moderna de **voiced commands**, sem o ecossistema de mods que existe hoje e com diversos pontos instáveis no core. Desde então, o foco foi **corrigir**, **refatorar** e **evoluir** o projeto de forma contínua:

- Correções de bugs e compatibilidade no GameServer e LoginServer  
- Sistemas de comandos voiced (`.menu`, `.vip`, `.skin`, eventos, donate, raid, auto farm, entre outros)  
- Eventos PvP e instanciados (TvT, CTF, KTB, Tournament, Territory War, Solo Boss, etc.)  
- Zonas custom (Party, Demon, Bonus), VIP, skins DressMe, startup de personagem, Community Board  
- Configuração unificada no padrão **L2JALN** (`l2jaln.properties`, `l2jalnmod.properties`, `l2jalnevents.properties`)  
- **Geodata L2D (ATT)** já integrada na pack  
- Build simplificada com **Apache Ant** e perfil **FREE** para distribuição aberta  

O resultado é uma source **madura e atual**, pensada para quem monta servidor próprio e quer adaptar rates, mods e conteúdo — cada administrador configura o seu mundo.

---

## O que vem na Release

| Componente | Descrição |
|------------|-----------|
| **Source** | Código Java completo (`java/`, `build.xml`) |
| **Patch** | Ajustes e diffs aplicáveis ao cliente/servidor conforme a release |
| **Pack** | GameServer + LoginServer prontos (`pack Free/`) |
| **Site** | Painel / páginas web (`site/`) |
| **Programas** | Ferramentas auxiliares (editores, conversores, utilitários) |

> Baixe sempre a **última release** para obter o conjunto completo. O clone deste repositório é indicado para quem vai **compilar**, **estudar** ou **contribuir** com o código.

---

## Requisitos

| Requisito | Versão recomendada |
|-----------|-------------------|
| **JDK** | 11 |
| **MySQL** | 5.5 |
| **Apache Ant** | 1.9+ |
| **Sistema** | Windows ou Linux |

Geodata **L2D (ATT)** já incluída na estrutura da pack — não é necessário baixar geodata separadamente para o perfil distribuído.

---

## Build rápido

1. Instale o **JDK 11** e configure `JAVA_HOME` (ou crie `build.local.properties`):

```properties
local.jdk.home=C:/Program Files/Java/jdk-11.0.4
```

2. Na raiz do projeto:

```bash
ant jar
```

3. Saída:

- `build/l2jserver.jar` — JAR compilado (modo **FREE**)  
- `pack Free/gameserver/libs/l2jserver.jar` — cópia para a pack  
- `pack Free/gameserver/config/` — configs sincronizadas (padrão L2JALN)  
- `pack Free/gameserver/data/` — HTML, XML, geodata, multisell  

Outros alvos úteis:

```bash
ant compile   # apenas compilar
ant clean     # limpar build/
```

---

## Estrutura do repositório

```
source-free/
├── java/                 # Código-fonte GameServer / Login / mods
├── config/               # Configuração de desenvolvimento (padrão L2JALN)
├── data/                 # HTML, XML, scripts, geodata
├── pack Free/            # Pack pronta (gameserver, login, site)
├── lib/                  # Dependências (.jar)
├── dist/                 # Scripts de arranque
├── build.xml             # Build Ant (ant jar)
└── README.md
```

Documentação adicional na pack:

- `pack Free/MODS-PACK-FREE.txt` — lista de mods incluídos nesta build FREE  
- `pack Free/GUIA-RAPIDO.txt` / `GUIA-CONFIG-SERVIDOR.txt` — configuração do servidor  

---

## Mods incluídos (build FREE)

Eventos PvP, zonas custom, VIP, skins, menu mod, startup, Territory War, Tournament, comandos voiced e muito mais. Consulte `MODS-PACK-FREE.txt` para o inventário atualizado.

Mods premium (ex.: roleta avançada, sistemas comerciais específicos) foram removidos ou desativados nesta distribuição FREE — cada administrador pode evoluir a source conforme a sua necessidade.

---

## Configuração (padrão L2JALN)

| Ficheiro | Função |
|----------|--------|
| `config/l2jaln.properties` | Core ALN — skins, Territory War, itens especiais |
| `config/custom/l2jalnmod.properties` | Mods, donate, augment, flags gerais |
| `config/custom/l2jalnevents.properties` | Zonas farm, Party / Bonus / Demon Zone |
| `config/server.properties` | IP, portas, rates base |
| `config/custom/server-mods.properties` | Liga/desliga mods no runtime |

Edite em `config/` e execute `ant jar` para sincronizar com `pack Free/`.

---

## História e créditos

- **Início:** 2017 — fork e evolução de base open source L2J  
- **Desenvolvimento contínuo:** correções, voiced commands, eventos, zonas, interface e dezenas de mods  
- **Marca:** L2JALN — Team-L2JALN — DeV A.L.N  

Agradecimento à comunidade L2J open source que possibilitou o ponto de partida; todo o trabalho posterior de correção, mods e pack é fruto de anos de desenvolvimento dedicado.

---

## Licença

Distribuído sob a licença **Apache License 2.0**. Ver [LICENSE](LICENSE) para o texto completo.

---

## Aviso legal

Este software é fornecido para fins **educacionais** e de **estudo** de emulação de servidores privados. O uso de Lineage II e marcas relacionadas é propriedade dos seus respectivos titulares. Os mantenedores não se responsabilizam pelo uso em produção sem as devidas licenças e conformidade legal.

---

<p align="center">
  <strong>L2JALN</strong> — Team-L2JALN · DeV A.L.N<br>
  <em>Source evoluída desde 2017 — da base open source ao servidor completo de hoje.</em>
</p>
