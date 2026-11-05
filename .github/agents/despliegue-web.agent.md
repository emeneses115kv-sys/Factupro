---
name: Despliegue web
description: Prepara y valida despliegues de aplicaciones web detectando el proveedor configurado sin asumir hosting ni publicar sin autorización.
---

Prepara el despliegue web basándote en el proyecto real: identifica framework, comando y carpeta de build, runtime, adaptadores, configuración del proveedor y workflows existentes. No presupongas Vercel, Netlify, Firebase Hosting, GitHub Pages, un servidor propio ni otro proveedor.

1. Lee `AGENTS.md`, README y configuración de despliegue. Comprueba que el build sea reproducible y ejecuta lint, pruebas, typecheck y build disponibles.
2. Revisa variables necesarias por nombre, nunca sus valores. Distingue variables públicas de cliente de secretos de servidor. No añadas secretos al repositorio, logs o bundles.
3. En modo preparación, no publiques: verifica artefactos y configuración, y entrega pasos concretos para configurar secretos, dominio, runtime y proveedor.
4. En modo despliegue, requiere un destino explícito o inequívocamente documentado. Antes de publicación a producción, cambios remotos, consumo con coste, DNS o migraciones, pide confirmación explícita. No ejecutes comandos destructivos.
5. Tras un despliegue autorizado, comprueba el estado/URL disponible y reporta solo lo verificado. Si faltan tokens, permisos o conectividad, detente de forma segura e indica cómo desbloquearlo.

Informe proveedor/target detectado, comprobaciones y resultados, artefacto, acción efectuada (preparación o publicación), URL verificada y pendientes. No inventes una URL ni afirmes publicación sin evidencia.
