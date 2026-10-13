<div align="center">

# 🎮 PCSTOP

### *Um PC Linux ARM64 no seu bolso.*

**Containers Ubuntu com OpenGL acelerado, direto no Android.**
**Sem root. Sem Termux. Sem PC.**

[![Status](https://img.shields.io/badge/status-v1.0--funcional-success)](https://github.com/gamessa/PCSTOP)
[![Licença](https://img.shields.io/badge/licen%C3%A7a-GPL--3.0-blue)](LICENSE)
[![Plataforma](https://img.shields.io/badge/Android-ARM64-green)](https://www.android.com/)

![glxinfo mostrando Gladio](docs/screenshots/glxinfo.png)

</div>

---

## 🌟 O que é o PCSTOP?

**PCSTOP transforma seu celular Android num servidor Linux gráfico portátil.**

Ele roda **containers Ubuntu 24.04 ARM64 completos** dentro do Android usando 
`proot` (sem precisar de root nem de Termux), e vai além: **integra o Gladio** 
— o lendário tradutor de OpenGL/GLX para OpenGL ES do [Winlator](https://github.com/brunodev85/winlator) — 
fazendo com que binários Linux gráficos rodem de verdade na tela do celular.

Na prática: **você abre o app, toca em "Iniciar", e tem um Ubuntu com X11, 
VNC, e OpenGL funcionando** — tudo dentro de um APK só.

---

## 🎯 Pra que serve?

### Hoje (v1.0) — provado funcionando

| Caso de uso | Exemplo |
|---|---|
| 🧪 **Rodar ferramentas Linux** | `glxinfo`, `glxgears`, `glxdemo`, `xterm` |
| 🎮 **Jogos Linux simples** | SuperTux, Tux Racer, Pingus |
| 📝 **Dev no celular** | Editor de texto, Python, gcc, apt |
| 🔬 **Testar código Linux ARM64** | Sem precisar de PC ou VM |
| 🎨 **Aprender Linux** | Ambiente X11 completo, icewm, terminal |

### Amanhã — o que tá vindo

| Ideia | Status |
|---|---|
| 🍷 **Wine + jogos Windows** | ⏳ quando a renderização real estiver pronta |
| 🎬 **Blender, GIMP, Inkscape** | ⏳ idem |
| 🕹️ **Emuladores** | ⏳ idem |
| 🖥️ **VNC externo** | ✅ já funciona via rede |
| 📦 **Múltiplos containers** | ✅ já funciona |

---

## ✨ Recursos

- 📦 **Container Ubuntu 24.04 ARM64** — base oficial, tudo via `apt`
- 🖥️ **X11 completo** — Xvfb + x11vnc + icewm rodando sozinhos
- 📱 **Cliente VNC nativo** — desenha no app, sem app externo
- 🎨 **OpenGL acelerado** — pipeline gladio completo
- 🐍 **Bridge X11 em Python** — handshake + envio de FDs via `SCM_RIGHTS`
- ⚡ **Ring buffer compartilhado** — cliente C ↔ servidor Kotlin
- 🔧 **Zero root, zero Termux** — 100% dentro do APK
- 🎹 **Teclado flutuante** — atalhos Ctrl, Alt, Shift, setas, Esc
- 📋 **Copiar log** — botão que salva logs de crash em `/sdcard/`
- 🖼️ **UI moderna** — drawer lateral, botões circulares, tema escuro

---

## 🏗️ Como funciona por dentro

### Diagrama geral
