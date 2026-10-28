<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construa o Jogo com Fluxos de Trabalho Agênticos

---

Nesta parte, o Copilot passa de planejador a implementador. Em vez de escrever código linha por linha, você descreve o que deseja e deixa o Copilot trabalhar nos arquivos necessários.

## Tarefa 1: Conecte a Batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat (selecione "Agent" no menu dropdown de modo).
2. Insira este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Retorne ao fluxo de programação padrão do Copilot CLI (ou continue no autopilot se quiser que o Copilot prossiga até você pará-lo).
2. Se for útil, forneça mais contexto indicando o arquivo: `@src/pages/index.astro`.
3. Insira este prompt:
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
3. Deixe o Agent Mode implementar as alterações em vários arquivos, incluindo `index.astro`.
4. Revise as alterações na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI trabalhar em `src/pages/index.astro` e nos demais arquivos necessários.
5. Inspecione as alterações geradas com `/diff` e aprove-as.
<!-- track:cli:end -->

## Tarefa 2: Teste a Batalha

1. Insira `octocat` e `torvalds` como os dois nomes de usuário e clique em **Battle**.
2. Você deve ver ambos os gráficos de contribuição renderizados lado a lado com grids coloridos.
3. Teste os casos de erro:
   - Deixe um ou ambos os campos vazios e clique em Battle — você deve ver um erro de validação.
   - Insira um nome de usuário inválido — o app deve exibir um erro da API.
4. Teste pressionando **Enter** em qualquer campo de entrada — deve disparar a batalha assim como clicar no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver totalmente correto, dê feedback ao Copilot diretamente. Por exemplo:

- *"The contribution squares are too large, make them 12x12px"*
- *"Add a hover tooltip showing the date and contribution count"*
- *"The loading state needs a pulse animation"*

<!-- track:vscode:start -->
O Agent Mode lida naturalmente com alterações em vários arquivos e iterações. Cada prompt de acompanhamento se baseia na conversa anterior, permitindo melhorar a implementação aos poucos sem recomeçar do zero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento se baseia nos anteriores. Use `/session` ou `/context` para inspecionar o contexto que o Copilot está mantendo e `/review` após uma iteração maior para procurar bugs ou melhorias.
<!-- track:cli:end -->

## Dicas para esta parte

- **Seja específico sobre o que você quer** — requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitar** — use a visualização de diff para entender o que foi modificado.
- **Teste o aplicativo logo após cada etapa de implementação** para localizar os problemas rapidamente.

## ✅ Parte 3 Concluída

Você aprendeu a:

- Usar o Copilot para **implementar alterações em vários arquivos**
- **Iterar nos resultados** com feedback direcionado
- Conduzir o **ciclo completo de um recurso** — implementação, revisão, testes e refinamento
