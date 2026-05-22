<div align="center">

# ⚔️ SourceCompleta-L2JALN

### *SOURCE · PATCH · PACK · SITE · TOOLS*

[![License](https://img.shields.io/badge/License-Apache%202.0-2b6cb0?style=for-the-badge&logo=apache)](LICENSE)
[![Java](https://img.shields.io/badge/Java-11-ed8b00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![MySQL](https://img.shields.io/badge/MySQL-5.5-4479a1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Ant](https://img.shields.io/badge/Build-Apache%20Ant-a81c07?style=for-the-badge)](build.xml)
[![Geodata](https://img.shields.io/badge/Geodata-L2D%20ATT-6c5ce7?style=for-the-badge)]()

**Ecossistema completo para servidores Lineage II · L2J**  
Desenvolvido e evoluído por **L2JALN** — Team-L2JALN · DeV A.L.N

[📦 Releases](#-o-que-vem-na-release) · [🚀 Build](#-build-rápido) · [🚫 Suporte](#-política-de-suporte) · [⚙️ Config](#️-configuração-padrão-l2jaln) · [🎮 Mods](#-mods-incluídos-build-free)

---

</div>

> 📌 **Este repositório** traz o **código-fonte** e a documentação de compilação.  
> Na secção **Releases** do repositório está o pacote completo: **source**, **patch**, **site**, **pack** e **programas** auxiliares.

---

## 🚫 Política de suporte

> **⚠️ IMPORTANTE — leia antes de abrir issue ou pedir ajuda**

Este projeto é distribuído **como está** (*as-is*), para estudo e uso por conta própria. **Não há suporte oficial** para:

| 🚫 | Não damos suporte para |
|:---:|:---|
| ➕ | **Adicionar mods** — integrar mods novos, voiced, eventos ou sistemas de terceiros |
| 📝 | **Alterar a source** — Java, handlers, core, refatoração ou debug de código |
| ⚙️ | **Configurar a pack** — rates, IP, MySQL, `l2jalnmod`, eventos, drops, spawns, etc. |
| 📘 | **Padrão aCis / L2J genérico** — tutoriais de ACIS retail, “como configurar servidor L2J” do zero |

### ✅ O que este repositório oferece

| ✅ | Incluído |
|:---:|:---|
| 📦 | **Release** com source, patch, pack, site e ferramentas |
| 🔨 | **Build documentado** — `ant jar` (ver secção abaixo) |
| 📖 | **Guias na pack** — `GUIA-RAPIDO.txt`, `GUIA-CONFIG-SERVIDOR.txt`, `MODS-PACK-FREE.txt` *(leitura por sua conta)* |

Cada administrador **adapta, configura e desenvolve** o servidor de forma **independente**. Dúvidas sobre mods, source ou config devem ser resolvidas pela **sua equipa** ou pela **comunidade** — não pelo autor desta release gratuita.

---

## 🌟 Sobre o projeto

<table>
<tr>
<td width="80">📅</td>
<td><strong>2017</strong> — Início a partir de uma base open source L2J: sem <strong>voiced commands</strong>, core instável e quase sem mods.</td>
</tr>
<tr>
<td>🔧</td>
<td><strong>Hoje</strong> — Anos de correções, refatoração e sistemas novos: eventos PvP, zonas, VIP, skins, menu mod, Territory War e dezenas de mods atuais.</td>
</tr>
<tr>
<td>🎯</td>
<td><strong>Objetivo</strong> — Source <strong>madura e gratuita</strong> para montar o seu servidor — <strong>sem suporte</strong> de configuração ou desenvolvimento por parte do autor.</td>
</tr>
</table>

```
  2017          open source L2J          correções + voiced + eventos
    │                    │                         │
    └────────────────────┴─────────────────────────┴──►  PACK L2JALN FREE (2025+)
```

---

## 📦 O que vem na Release

| | Componente | Conteúdo |
|:---:|:---|:---|
| 💻 | **Source** | Código Java completo — `java/`, `build.xml` |
| 🩹 | **Patch** | Ajustes para cliente / servidor |
| 📁 | **Pack** | GameServer + LoginServer prontos — `pack Free/` |
| 🌐 | **Site** | Painel e páginas web — `site/` |
| 🛠️ | **Programas** | Ferramentas auxiliares (editores, conversores) |

> ⬇️ Baixe sempre a **última Release** para o conjunto completo.  
> Clone este repo para **compilar**, **estudar** ou **contribuir**.

---

## 📋 Requisitos

<div align="center">

| ☕ JDK | 🐬 MySQL | 🔨 Ant | 💾 SO | 🗺️ Geodata |
|:---:|:---:|:---:|:---:|:---:|
| **11** | **5.5** | **1.9+** | Win / Linux | **L2D ATT** *(na pack)* |

</div>

---

## 🚀 Build rápido

### 1️⃣ JDK 11

Crie `build.local.properties` na raiz *(ou use `JAVA_HOME`)*:

```properties
local.jdk.home=C:/Program Files/Java/jdk-11.0.4
```

### 2️⃣ Compilar

```bash
ant jar
```

### 3️⃣ Resultado

| 📂 Caminho | 📄 Descrição |
|:---|:---|
| `build/l2jserver.jar` | JAR compilado — modo **FREE** |
| `pack Free/gameserver/libs/l2jserver.jar` | Cópia automática para a pack |
| `pack Free/gameserver/config/` | Configs **L2JALN** sincronizadas |
| `pack Free/gameserver/data/` | HTML, XML, geodata, multisell |

```bash
ant compile   # ⚡ só compilar
ant clean     # 🧹 limpar build/
```

---

## 📂 Estrutura do repositório

```
source-free/
├── 📜 java/              → Código-fonte (GS, Login, mods)
├── ⚙️ config/            → Config desenvolvimento (L2JALN)
├── 📊 data/              → HTML, XML, scripts
├── 📦 pack Free/         → Pack pronta (GS + Login + site)
├── 📚 lib/               → Dependências .jar
├── 🚀 dist/              → Scripts de arranque
└── 🔨 build.xml          → ant jar
```

📖 **Docs na pack:** `MODS-PACK-FREE.txt` · `GUIA-RAPIDO.txt` · `GUIA-CONFIG-SERVIDOR.txt`

---

## 🎮 Mods incluídos (build FREE)

<details>
<summary><strong>📜 Clique para ver a lista completa</strong></summary>

<br>

| Categoria | Mods |
|:---|:---|
| ⚔️ **Eventos PvP** | KTB · TvT · Multi TvT · CTF · Death Match · Last Man · Fortress · PvP Event · Solo Boss · Tournament · Territory War |
| 🌍 **Zonas** | Party Zone · Demon Zone · Bonus Zone |
| 🎨 **Interface** | VIP · Skins DressMe · Menu mod · Startup · `.pack` · Raid command · Auto Farm voiced |

Consulte `pack Free/MODS-PACK-FREE.txt` para o inventário atualizado.

</details>

---

## ⚙️ Configuração padrão L2JALN

| 📄 Ficheiro | 🎯 Função |
|:---|:---|
| `config/l2jaln.properties` | Core ALN — skins, Territory War, itens |
| `config/custom/l2jalnmod.properties` | Mods, donate, augment, flags |
| `config/custom/l2jalnevents.properties` | Zonas farm · Party / Bonus / Demon |
| `config/server.properties` | IP, portas, rates |
| `config/custom/server-mods.properties` | Liga / desliga mods |

> ✏️ Edite em `config/` → execute `ant jar` → sincroniza com `pack Free/`  
> 🚫 **Sem suporte** para dúvidas de configuração — use os guias `.txt` na pack como referência.

---

## 👨‍💻 História e créditos

| | |
|:---|:---|
| 🏁 **Início** | 2017 — fork open source L2J |
| 🔨 **Evolução** | Voiced commands · eventos · zonas · interface · mods |
| 🏷️ **Marca** | **L2JALN** — Team-L2JALN — DeV A.L.N |

Agradecimento à comunidade L2J open source pelo ponto de partida.  
Todo o trabalho de correção, mods e pack é fruto de **anos de desenvolvimento dedicado**.

---

## 📜 Licença

[![License](https://img.shields.io/badge/License-Apache%202.0-blue?style=flat-square)](LICENSE)

Distribuído sob **Apache License 2.0** — ver [LICENSE](LICENSE).

---

## ⚠️ Aviso legal

Este software destina-se a fins **educacionais** e de **estudo** de emulação de servidores privados.  
Lineage II e marcas relacionadas pertencem aos seus titulares.  
Os mantenedores **não se responsabilizam** pelo uso em produção sem licenças e conformidade legal.

**Sem garantia de suporte técnico** — incluindo mods, alterações na source, configuração da pack ou procedimentos padrão aCis/L2J.

---

<div align="center">

### ⚔️ L2JALN

**Team-L2JALN** · **DeV A.L.N**

*Source evoluída desde 2017 — da base open source ao servidor completo de hoje.*

<br>

⭐ Se este projeto te ajudou, deixa uma **estrela** no repositório!

</div>
