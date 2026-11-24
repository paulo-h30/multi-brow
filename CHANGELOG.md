# Changelog — Multi-Brow

Histórico oficial de versões publicadas do Multi-Brow.

---

## v0.1.2 — 2026-11-24
**Lives em 2º Plano, Abas Minimalistas e Melhorias no /hunt**

### Adicionado
- Integração **Lives (Twitch & Kick)** na barra superior com suporte a 1 live da Twitch e 1 da Kick rodando mudas em segundo plano, visualização dividida `1|1`, menu lateral recolhível, leitura de pontos no menu, resgate automático do baú de bônus da Twitch e qualidade mínima `160p`.
- Notificação flutuante de download de atualização no canto inferior direito com barra de progresso, botão minimizar e link direto para as notas da versão.
- Indicador compacto de uso de RAM de volta na barra superior para acompanhamento rápido.
- Botão **"Ver todas as versões no site"** no modal de Novidades, abrindo o histórico completo em `multi-brow.pages.dev/changelog`.
- Selos **"Lendário ×4"** e **"Sem Shiny"** nas linhas do painel `/hunt` para identificar hunts especiais.

### Alterado
- Abas da barra superior redesenhadas com visual minimalista e compacto, abrindo apenas a Conta 1 por padrão com botão `+` para adicionar e botão `×` para fechar/hibernar as demais.
- Modal de Novidades redesenhado sem barra de título padrão, com cabeçalho de destaque, cards por categoria, scrollbar customizada e foco exclusivo na versão atual.
- Atualização automática agora instala de forma silenciosa e reinicia o aplicativo sem exibir a janela do instalador.

### Corrigido
- Corrigido cálculo de XP/ouro por abate, filtro de desbloqueio e multiplicador ×4 de Lendários/Míticos selvagens no painel `/hunt`.

---

## v0.1.1 — 2026-11-23
**Visual de Abas Reais, Central Compacta e Melhorias no /hunt**

### Adicionado
- Botão de copiar rápido ao lado do nome de cada Pokémon no painel `/hunt` com transição animada para ícone de Check.
- Janela de Novidades / Changelog com abertura automática após atualizações.

### Alterado
- Barra superior redesenhada com abas estilo navegador real, liberando mais espaço horizontal.
- Menu Central ajustado automaticamente à altura do conteúdo até o card de Novidades & Versões.
- Janela principal passa a iniciar maximizada por padrão e lembra a preferência do usuário ao reabrir.

### Corrigido
- Corrigido piscar de janelas de fundo sobre o aplicativo ao hibernar uma aba pelo menu de contexto.
- Corrigido texto do plano gratuito temporário para Brow Trial.

### Removido
- Removido o nome e o ícone da marca da barra superior para dar prioridade total às abas.

---

## v0.1.0 — 2026-11-23
**Lançamento Inicial do Multi-Brow**

### Adicionado
- Suporte a até 4 contas isoladas do `pokeidle.io` (modos 1 Tela, 2 Telas `1|1` e 4 Telas `2×2`).
- Central de Controle em gaveta lateral flutuante (FPS, Modo Leve, Zoom, RAM, Plano e Novidades).
- Limitador de FPS individual por tela ou nas 4 telas simultaneamente (`15 / 30 / 60 / ∞`).
- Painel `/hunt` flutuante sincronizado passivamente com o jogo e recorte automático de sprites.
- Janela de voto isolada por conta (`idlehub.io`) e menu de contexto nas abas.
- Planos Brow Free, Brow Trial (7 dias grátis) e Brow Pro (R$ 10/mês via Mercado Pago).
- Atualização automática integrada via Cloudflare R2.

### Corrigido
- Corrigido cálculo de XP/ouro por abate e filtro de desbloqueio no painel `/hunt` para não recomendar hunts iniciais quando o Pokémon já está em nível alto.
