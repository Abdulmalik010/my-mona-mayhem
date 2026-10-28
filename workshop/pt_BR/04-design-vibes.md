<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização com Foco no Design

---

Nesta parte, você vai usar os fluxos de planejamento e implementação do Copilot para projetar uma transformação visual completa. Isso é desenvolvimento orientado a design: comece com a visão, itere nos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o Tema Retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> I want to transform this page into a full retro arcade experience. Plan a comprehensive visual overhaul that includes: CRT scanline effects on the background, neon glow on the title that pulses like a neon sign, animated VS badge with gradient color shifts, shine/shimmer overlay on the user result cards, float-in animations for input fields, color-shifting loading text between green and purple, and hover glow effects on contribution squares. Keep the dark background (`#0a0a1a`) with green (`#5fed83`) and purple (`#8a2be2`) accent colors. Use a dark theme with the Press Start 2P retro gaming font from Google Fonts.

O Copilot vai gerar um plano de implementação detalhado que cobre todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e itere:

- Sugira ajustes no timing das animações (ex.: "Make the neon pulse slower, around 3 seconds")
- Pergunte sobre efeitos específicos (ex.: "How will the shimmer overlay work on the cards?")
- Solicite mudanças na abordagem se algo não parecer correto

Quando estiver satisfeito com o plano:

<!-- track:vscode:start -->
- Mude para o modo **Agent** e peça ao Copilot para implementá-lo.
<!-- track:vscode:end -->

<!-- track:cli:start -->
- Peça ao Copilot CLI para implementá-lo.
- Depois, revise as alterações de estilo com `/diff` antes de aprová-las.
<!-- track:cli:end -->

## Tarefa 2: Implemente o Tema

<!-- track:vscode:start -->
Mude para o modo **Agent** e peça ao Copilot para implementar o plano:
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI para implementar o plano:
<!-- track:cli:end -->

> Implement the retro arcade theme plan we just designed.

O Copilot vai adicionar múltiplas animações CSS, pseudo-elementos e transições na sua folha de estilos. Isso pode incluir:

- `@keyframes` para scanlines, pulso neon, shimmer e efeitos de float-in
- Pseudo-elementos (`::before`, `::after`) para efeitos de sobreposição
- CSS custom properties para as cores do tema
- Estados de transição e hover para elementos interativos

<!-- track:cli:start -->
Depois que as alterações forem aplicadas, revise o estilo com `/diff` antes de aprová-lo.
<!-- track:cli:end -->

## Tarefa 3: Ajuste Fino das Vibes

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize a página à força (`Ctrl+Shift+R`).

Mantenha a pré-visualização do navegador aberta e itere no design. Tente prompts como:

> The scanline effect is too strong, reduce opacity to 0.03

> Add a subtle electrical flicker to the title text

> The VS badge should pulse more dramatically

Isso é **desenvolvimento orientado a design** — você está iterando na saída visual em tempo real. Cada prompt refina a experiência até que fique perfeita. Não se contente com "bom o suficiente" — aperfeiçoe as vibes até que a página pareça pertencer a um gabinete de arcade.

## Tarefa 4: Atualize as Instruções

Suas instruções devem refletir as principais decisões de design para manter os próximos prompts alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Add a design guide section to copilot-instructions.md describing our retro arcade theme: colors, fonts, animation style
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Update our repository instructions with a short design guide for the retro arcade theme: colors, fonts, animation style, and the rule that new UI should keep the neon aesthetic.
<!-- track:cli:end -->

Faça commit das instruções atualizadas e das alterações de design quando a página estiver como você quer.

## ✅ Parte 4 Concluída

**O que você aprendeu:**

- **Plan Mode para sistemas de design** — esboce uma reformulação visual completa antes de escrever qualquer código
- **Iterar na saída visual** — use prompts rápidos de acompanhamento para ajustar animações, cores e efeitos
- **Manter as instruções atualizadas com decisões de design** — documente seu tema para que o Copilot mantenha a consistência
- **Fluxo de desenvolvimento orientado a design** — comece com a visão, implemente com IA, refine até ficar perfeito
