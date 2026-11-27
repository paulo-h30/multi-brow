# Changelog — Multi-Brow

Histórico oficial de versões publicadas do Multi-Brow.

---

## v0.1.3 — 2026-11-27
**Extensões do Chrome, Menu Lateral e Grupos de Outros Idles**

### Adicionado
- Novo Menu Lateral recolhível com animação suave (atalho Ctrl+B), favicon real de cada site e grupos expansíveis que exibem as contas abertas, botão + Adicionar conta e menu de opções no botão direito.
- Suporte à criação de novos grupos com até 4 contas isoladas para qualquer outro jogo idle/web, com hibernação por grupo e aviso de consumo de RAM.
- Novo Gerenciador de Extensões do Chrome na barra superior, com carregamento automático e isolado em todas as contas e grupos.
- Aba Recomendadas com instalação em 1 clique da extensão /hunt for PokeIdle (por Liang).
- Chrome Web Store embutida dentro do Multi-Brow com detecção automática da página da extensão e botão + Instalar no Multi-Brow (sem precisar copiar links).
- Aba Importar manual para instalar extensões por link/ID da Chrome Web Store, arquivo .crx/.zip ou pasta descompactada, além de suporte a abertura de popup.

### Alterado
- Barra superior simplificada: abas de contas e botão do menu movidos para o Menu Lateral, deixando um indicador limpo do grupo e conta em foco no topo.
- Janelas de Extensões, Chrome Web Store e Novo/Editar Grupo redesenhadas sem barra de título padrão do Windows, integradas ao tema escuro do aplicativo.
- Redução no uso de memória e CPU em cada tela após a remoção da interceptação de telemetria do antigo /hunt.

### Corrigido
- Garantido que fechar as janelas auxiliares de Extensões, Loja ou Grupos mantenha o foco na janela principal sem minimizar o aplicativo.
- Corrigidos erros de inicialização ao consultar o estado antes do carregamento das extensões e cancelamentos ao hibernar/recarregar abas em carregamento.

### Removido
- Removido o painel /hunt nativo antigo, substituído pelo suporte completo à extensão /hunt for PokeIdle e demais extensões do Chrome.

---

## v0.1.2 — 2026-11-24
**Lives em 2º Plano, Abas Minimalistas e Melhorias no /hunt**

### Adicionado
- Integração Lives (Twitch & Kick) na barra superior com suporte a 1 live da Twitch e 1 da Kick rodando mudas em segundo plano, visualização dividida 1|1, menu lateral recolhível, leitura de pontos no menu, resgate automático do baú de bônus da Twitch e qualidade mínima 160p.
- Indicador compacto de uso de RAM de volta na barra superior para acompanhamento rápido.
- Botão "Ver todas as versões no site" no modal de Novidades, abrindo o histórico completo em multi-brow.pages.dev/changelog.
- Selos "Lendário ×4" e "Sem Shiny" nas linhas do painel /hunt para identificar hunts especiais.

### Alterado
- Abas da barra superior redesenhadas com visual minimalista e compacto, abrindo apenas a Conta 1 por padrão com botão + para adicionar e botão × para fechar/hibernar as demais.
- Modal de Novidades redesenhado sem barra de título padrão, com cabeçalho de destaque, cards por categoria, scrollbar customizada e foco exclusivo na versão atual.
- Atualização automática agora instala de forma silenciosa e reinicia o aplicativo sem exibir a janela do instalador.

### Corrigido
- Corrigido cálculo de XP/ouro por abate, filtro de desbloqueio e multiplicador ×4 de Lendários/Míticos selvagens no painel /hunt.

---

## v0.1.1 — 2026-11-23
**Visual de Abas Reais, Central Compacta e Melhorias no /hunt**

### Adicionado
- Botão de copiar rápido ao lado do nome de cada Pokémon no painel /hunt com transição animada para ícone de Check.
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
- Suporte a até 4 contas isoladas do pokeidle.io (modos 1 Tela, 2 Telas 1|1 e 4 Telas 2×2).
- Central de Controle em gaveta lateral flutuante (FPS, Modo Leve, Zoom, RAM, Plano e Novidades).
- Limitador de FPS individual por tela ou nas 4 telas simultaneamente (15 / 30 / 60 / ∞).
- Painel /hunt flutuante sincronizado passivamente com o jogo e recorte automático de sprites.
- Janela de voto isolada por conta (idlehub.io) e menu de contexto nas abas.
- Planos Brow Free, Brow Trial (7 dias grátis) e Brow Pro (R$ 10/mês via Mercado Pago).
- Atualização automática integrada via Cloudflare R2.

### Corrigido
- Corrigido cálculo de XP/ouro por abate e filtro de desbloqueio no painel /hunt para não recomendar hunts iniciais quando o Pokémon já está em nível alto.
