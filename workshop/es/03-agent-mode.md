<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Crear el Juego con Flujos de Trabajo Agénticos

---

En esta parte, Copilot pasa de planificar a implementar. En lugar de escribir código línea por línea, describes lo que quieres y dejas que Copilot trabaje en los archivos necesarios.

## Tarea 1: Conecta la Batalla

<!-- track:vscode:start -->
1. Cambia a modo **Agent** en Copilot Chat (selecciona "Agent" en el menú desplegable de modo).
2. Ingresa este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Vuelve al flujo de programación estándar de Copilot CLI (o mantén el modo autopilot si quieres que Copilot siga trabajando hasta que lo detengas).
2. Si te resulta útil, añade contexto indicando el archivo: `@src/pages/index.astro`.
3. Ingresa este prompt:
<!-- track:cli:end -->

   > Add client-side JavaScript to the battle page that:
   > 1. When the Battle button is clicked, gets both usernames from the inputs
   > 2. Validates both are filled (show error if not)
   > 3. Fetches both users' contribution data in parallel from our API
   > 4. Renders contribution graphs as colored grids — each day is a colored square using GitHub's color palette
   > 5. Shows a VS badge between the two users
   > 6. Displays username, total contributions, and date range for each user
   > 7. Handles loading states and errors
   > 8. Also triggers on Enter key in input fields.
   > 9. Simple UI for now that is already scaffolded.
   >
   > Use TypeScript interfaces for the contribution data structure.

<!-- track:vscode:start -->
3. Deja que Agent Mode implemente los cambios en varios archivos, incluido `index.astro`.
4. Antes de aceptar los cambios, revísalos en la vista de diferencias.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deja que Copilot CLI trabaje en `src/pages/index.astro` y en los demás archivos necesarios.
5. Inspecciona los cambios generados con `/diff` y apruébalos.
<!-- track:cli:end -->

## Tarea 2: Prueba la Batalla

1. Ingresa `octocat` y `torvalds` como los dos nombres de usuario, luego haz clic en **Battle**.
2. Deberías ver ambos gráficos de contribuciones renderizados lado a lado con cuadrículas de colores.
3. Prueba los casos de error:
   - Deja uno o ambos campos vacíos y haz clic en Battle — deberías ver un error de validación.
   - Ingresa un nombre de usuario inválido — la app debería mostrar un error de la API.
4. Prueba presionar **Enter** en cualquier campo de entrada — debería activar la batalla igual que al hacer clic en el botón.

## Tarea 3: Itera con Copilot

Si algo no está del todo bien, dale comentarios directamente a Copilot. Por ejemplo:

- *"The contribution squares are too large, make them 12x12px"*
- *"Add a hover tooltip showing the date and contribution count"*
- *"The loading state needs a pulse animation"*

<!-- track:vscode:start -->
Agent Mode gestiona de forma natural los cambios en varios archivos y las iteraciones. Cada prompt de seguimiento se basa en la conversación anterior, así que puedes mejorar la implementación poco a poco sin empezar de cero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Las sesiones de Copilot CLI conservan el historial, por lo que cada prompt de seguimiento se basa en los anteriores. Usa `/session` o `/context` para inspeccionar el contexto que Copilot mantiene, y `/review` después de una iteración importante para buscar errores o mejoras.
<!-- track:cli:end -->

## Consejos para esta parte

- **Sé específico sobre lo que quieres** — requisitos claros producen mejores resultados.
- **Divide las tareas grandes en prompts más pequeños** si Copilot se desvía.
- **Revisa los cambios antes de aceptar** — usa la vista de diferencias para entender qué se modificó.
- **Prueba la aplicación justo después de cada implementación** para localizar rápidamente los problemas.

## ✅ Parte 3 Completa

Has aprendido a:

- Usar Copilot para **implementar cambios en varios archivos**
- **Iterar sobre los resultados** con retroalimentación dirigida
- Gestionar el **ciclo completo de una funcionalidad** — implementación, revisión, pruebas y mejoras
