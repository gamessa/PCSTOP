<div align="center">

# 🎮 PCSTOP

### *Um PC Linux no seu bolso.*

**Containers Debian ARM64 com Interface Gráfica, Áudio e Gerenciamento de Arquivos, direto no Android.**
**Sem root. Sem Termux. Sem PC.**

[![Status](https://img.shields.io/badge/status-v1.2--funcional-success)](https://github.com/gamessa/PCSTOP)
[![Licença](https://img.shields.io/badge/licen%C3%A7a-GPL--3.0-blue)](LICENSE)
[![Plataforma](https://img.shields.io/badge/Android-ARM64-green)](https://www.android.com/)

</div>

---

## 🌟 O que é o PCSTOP?

**PCSTOP transforma seu celular Android num ambiente Linux gráfico portátil.**

Ele roda **containers Debian 12 ARM64 completos** dentro do Android usando `proot` (sem precisar de root nem de Termux). Na prática: **você abre o app, cria seu container, toca em "Play", e tem um Linux com interface gráfica (IceWM), terminal, áudio e gerenciador de arquivos** — tudo dentro de um APK só.

---

## 🎯 Pra que serve?

### Hoje (v1.2) — provado funcionando

| Caso de uso | Exemplo |
|---|---|
| 🧪 **Rodar ferramentas Linux** | `htop`, `nano`, `python3`, `wget` |
| 📝 **Dev no celular** | Editar código, compilar scripts |
| 📂 **Gerenciar arquivos** | Transferir arquivos entre Android e Linux (Thunar) |
| 📦 **Instalar programas** | GDebi (instalador de pacotes `.deb` nativo) |
| 🎨 **Aprender Linux** | Ambiente X11 completo, terminal, interface visual |
| 🔊 **Áudio** | PulseAudio configurado (som no alto-falante do celular) |

### O que está pronto para a Versão 2.0

| Ideia | Status |
|---|---|
| 🎮 **Renderização 3D Nativa** | 🟡 Gladio integrado, aguardando XServer (X11) |
| 🍷 **Wine + jogos Windows** | ⏳ dependente do item acima |
| 🕹️ **Emuladores** | ⏳ futuro |

---

## ✨ Recursos

- 📦 **Container Debian 12 ARM64** — rootfs customizado de ~200MB
- 🖥️ **Interface Gráfica (IceWM)** — rodando via VNC nativo no app
- 📱 **Cliente VNC nativo** — desenha na tela sem apps externos
- 🔊 **Áudio Funcional** — PulseAudio injetado direto no APK
- 📂 **Thunar (Gerenciador de Arquivos)** — com download automático caso não instalado
- 🔧 **GDebi (Instalador de .deb)** — instale programas com 2 cliques
- 🎨 **Gladio Integrado** — O motor OpenGL do Winlator está presente no APK, pronto para a próxima fase.
- 🔒 **Segurança** — roda como usuário comum (`pcstop`), sem root exposto
- 🎹 **Teclado flutuante** — atalhos Ctrl, Alt, Shift, setas, Esc
- 🖼️ **UI moderna** — drawer lateral, botões circulares, tema escuro
- 📋 **Crash Logger** — logs salvos em `/sdcard/pcstop-backup/`

---

## 🎉 Release v1.2 — Debian + Áudio + Arquivos

### ✨ O que funciona
- ✅ Criação de containers com resolução personalizada
- ✅ Inicialização automática do VNC + IceWM
- ✅ Áudio via PulseAudio (configurável on/off)
- ✅ Instalação automática do gerenciador de arquivos (Thunar)
- ✅ Instalação de pacotes `.deb` via GDebi (com interface gráfica)
- ✅ Usuário comum `pcstop` configurado (sem root exposto)

### ⚠️ Limitações Conhecidas
- 🎨 **Renderização 3D (Gladio):** O Gladio está integrado e operante, mas a exibição atual usa **VNC**, que captura apenas a tela 2D. Isso faz com que os elementos 3D (linhas, polígonos) não sejam desenhados nas coordenadas corretas.
  - *Solução em andamento:* Migração para um XServer nativo (Termux-X11/Xlorie) para permitir que o Gladio desenhe direto na GPU, liberando o 3D real.
- ❌ Wine / jogos Windows (dependente da correção do Gladio acima).

### 📦 Como usar
1. Baixe o `.apk` na aba **[Releases](../../releases)**
2. Habilite "instalar de fontes desconhecidas" no Android
3. Instale → abra → toque em **+** pra criar seu ambiente (escolha nome e resolução)
4. Aguarde o boot (~20 segundos)
5. No Linux, abra o menu lateral e clique em **📥 Instalar / Abrir Arquivos** para gerenciar seus arquivos!

> **Aviso:** É necessário ter pelo menos **1.5 GB de espaço livre** para extrair o sistema e os pacotes.