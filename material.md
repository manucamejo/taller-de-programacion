---
layout: page
title: Material
subtitle: Bibliografía y herramientas del curso
permalink: /material/
---

## Bibliografía recomendada

- **Elixir in Action** (3ra edición) — Saša Jurić (Manning Publications)
  La referencia principal del curso. [Ver en Manning](https://www.manning.com/books/elixir-in-action-third-edition)

## Documentación oficial

- [Documentación de Elixir](https://elixir-lang.org/docs.html)
- [HexDocs — Elixir](https://hexdocs.pm/elixir)
- [React — Aprende React](https://es.react.dev/learn)

## Herramientas

### Entorno de desarrollo

| Herramienta | Descripción | Link |
|-------------|-------------|------|
| Elixir | Lenguaje de programación | [elixir-lang.org](https://elixir-lang.org/install.html) |
| Erlang/OTP | Máquina virtual BEAM | [erlang.org](https://www.erlang.org/downloads) |
| Node.js | Para desarrollo React | [nodejs.org](https://nodejs.org/) |
| asdf | Gestor de versiones | [asdf-vm.com](https://asdf-vm.com/) |
| Visual Studio Code | Editor recomendado | [code.visualstudio.com](https://code.visualstudio.com/) |
| ElixirLS | Extension de Elixir para VS Code | [Marketplace](https://marketplace.visualstudio.com/items?itemName=JakeBecker.elixir-ls) |
| Git | Control de versiones | [git-scm.com](https://git-scm.com/) |

### Herramientas de Elixir

| Herramienta | Descripción |
|-------------|-------------|
| `mix` | Herramienta de build y gestión de proyectos |
| `iex` | Shell interactivo de Elixir |
| `hex` | Gestor de paquetes ([hex.pm](https://hex.pm/)) |
| `ExUnit` | Framework de testing incluido |

## Instalación del entorno

### Usando asdf (recomendado)

```bash
# Instalar asdf (macOS con Homebrew)
brew install asdf

# Agregar plugins
asdf plugin add erlang
asdf plugin add elixir
asdf plugin add nodejs

# Instalar versiones
asdf install erlang latest
asdf install elixir latest
asdf install nodejs latest

# Configurar como versiones globales
asdf global erlang latest
asdf global elixir latest
asdf global nodejs latest

# Verificar instalación
elixir --version
node --version
```

## Repositorio del curso

- [github.com/manucamejo/taller-de-programacion](https://github.com/manucamejo/taller-de-programacion)
