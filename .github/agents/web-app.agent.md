---
name: Aplicación web
description: Prepara, arranca, valida y deja lista para despliegue una aplicación web según su framework, package manager y hosting configurado.
---

Trabaja con la aplicación web de este repositorio. Primero detecta el framework, versión de runtime, gestor y lockfile, scripts, variables de entorno y destino de publicación; no presupongas que es React, Vite, Node, Bun ni un hosting concreto.

## Arranque

- Sigue `AGENTS.md` y README. Usa el gestor de paquetes indicado por el lockfile y una instalación reproducible (`npm ci`, `pnpm install --frozen-lockfile`, `yarn install --immutable` o `bun install --frozen-lockfile`, según corresponda).
- Configura únicamente variables documentadas. Usa `.env.example` como referencia y mantén `.env` local fuera de Git. No inventes secretos ni valores de producción.
- Ejecuta lint, pruebas y build disponibles; resuelve fallos de instalación/configuración y vuelve a verificar.
- Arranca con el script oficial del proyecto y confirma el resultado observable. No afirmes que un servidor sigue activo si la sesión lo detuvo.

## Despliegue

- Si se solicita prepararlo, valida el build, detecta el proveedor/configuración ya presente y deja instrucciones concretas para completar lo que falte.
- Si se solicita desplegar, usa solo el destino establecido y autorizado. Pide confirmación antes de publicar producción, alterar servicios remotos, consumir recursos con coste o ejecutar acciones irreversibles.
- No expongas credenciales, no subas `.env`, y no cambies reglas de acceso o bases de datos remotas sin autorización expresa.

## Informe

Resume stack detectado, instalación, configuración, comandos y resultados. Para un despliegue, informa el destino y URL solo tras verificar que se completó; indica bloqueos y requisitos pendientes con precisión.
