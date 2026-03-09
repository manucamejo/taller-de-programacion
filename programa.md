---
layout: page
title: Programa
subtitle: Organización de clases (13 semanas)
permalink: /programa/
---

## Objetivo de la materia

El objetivo del taller es que los estudiantes desarrollen una aplicación cliente-servidor en grupos, aplicando principios de programación funcional, concurrencia basada en procesos y comunicación entre sistemas. Se utilizará **Elixir** para el desarrollo del backend concurrente y **React** para la interfaz de usuario. Durante la cursada se introducirán los conceptos necesarios para diseñar sistemas concurrentes y aplicaciones interactivas en tiempo real.

---

## Clase 1 - Presentación del curso

Presentación de la materia, objetivos, modalidad de cursada, herramientas y organización general del taller.

## Clase 2 - Introducción a Elixir y programación funcional

Conceptos básicos del lenguaje, pattern matching, inmutabilidad, funciones y pipes.

```elixir
# Pattern matching
{:ok, resultado} = {:ok, 42}

# Pipes
"hola mundo"
|> String.upcase()
|> String.split(" ")
```

## Clase 3 - Estructuras de datos y proyectos en Elixir

Listas, tuplas, maps y structs. Introducción a Mix, organización de proyectos y testing básico.

```elixir
# Estructuras de datos
persona = %{nombre: "Ana", edad: 25}
%{nombre: nombre} = persona

# Listas
[cabeza | cola] = [1, 2, 3, 4, 5]
```

## Clase 4 - Procesos en Elixir y presentación del TP1

Procesos ligeros, spawn, envío y recepción de mensajes. Presentación del **Trabajo Práctico 1** (individual), orientado a programación funcional y procesos, con aproximadamente dos semanas de entrega.

```elixir
pid = spawn(fn ->
  receive do
    {:saludo, nombre} -> IO.puts("Hola, #{nombre}!")
  end
end)

send(pid, {:saludo, "Elixir"})
```

## Clase 5 - React I

Introducción a React. Componentes, JSX y estructura básica de una aplicación frontend.

## Clase 6 - React II

Manejo de estado, eventos y comunicación con APIs.

## Clase 7 - GenServer

Modelo actor aplicado con GenServer y manejo de estado concurrente.

```elixir
defmodule Contador do
  use GenServer

  def start_link(inicial \\ 0) do
    GenServer.start_link(__MODULE__, inicial, name: __MODULE__)
  end

  def incrementar, do: GenServer.cast(__MODULE__, :incrementar)
  def valor, do: GenServer.call(__MODULE__, :valor)

  @impl true
  def init(valor), do: {:ok, valor}

  @impl true
  def handle_cast(:incrementar, valor), do: {:noreply, valor + 1}

  @impl true
  def handle_call(:valor, _from, valor), do: {:reply, valor, valor}
end
```

## Clase 8 - Supervisión

Supervisores, estrategias de reinicio y tolerancia a fallos.

## Clase 9 - Procesos dinámicos

Registry y DynamicSupervisor para manejo de múltiples procesos.

## Clase 10 - Networking y presentación del TP final

Sockets TCP, modelo cliente-servidor y diseño de protocolos. Presentación formal del **trabajo práctico final**.

## Clase 11 - Networking en tiempo real

WebSockets y diseño de protocolos de comunicación.

## Clase 12 - Arquitectura de backend

Diseño de aplicaciones concurrentes y organización de procesos en sistemas cliente-servidor.

## Clase 13 - Integración cliente-servidor

Comunicación entre frontend React y backend mediante WebSockets e integración completa del sistema.
