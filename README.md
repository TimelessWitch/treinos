# FitFlow

App de treino pessoal — acompanhamento de treinos, exercícios e histórico, direto no navegador.

🔗 **Acesse em:** https://timelesswitch.github.io/treinos/

## O que faz

- Organiza treinos em programas (ex: Treino A, B, C…) com séries, repetições e observações por exercício, navegáveis por abas dentro da própria lista de Treinos.
- Execução guiada do treino, com ajuste de carga, checkbox de pular exercício e estimativa de 1RM.
- Histórico editável: data, calorias, humor e o que foi feito ou não em cada sessão.
- Catálogo de exercícios com distribuição por grupo muscular.
- Home com visão geral: próximo treino (com o foco muscular do dia), estatísticas da meta semanal, humor ao longo das sessões e gráfico de dias treinados por mês.
- Aba Progresso com evolução do corpo, das cargas por exercício e o histórico de treinos.
- Tema claro e escuro e backup exportar/importar, dentro da aba Perfil (seção Configurações).

## Onde ficam os dados

Tudo é salvo no **localStorage do navegador** — não tem servidor nem banco de dados. Isso significa:

- Os dados ficam só nesse navegador/aparelho; não sincronizam entre dispositivos.
- Limpar os dados do navegador apaga o progresso.
- Use os botões **Exportar/Importar** (aba Perfil > Configurações) pra fazer backup em arquivo `.json` sempre que quiser.

## Rodando localmente

É um único arquivo HTML autocontido (sem build, sem dependências). Basta abrir `index.html` no navegador.

## Histórico de versões

Cada versão publicada fica marcada com uma tag no repositório — dá pra voltar a qualquer uma delas (`git checkout v1.0.0`, por exemplo) se algo quebrar.

- **v2.0.0 — 2026-10-19**
  - **Navegação:** 5 abas — Home, Treinos, Exercícios, Progresso e Perfil. O Histórico virou uma sub-aba de Progresso e as Configurações (tema, exportar/importar) passaram para uma seção recolhível no fim do Perfil; a engrenagem foi removida.
  - **Aba Progresso** com abas em formato de pílula:
    - **Corpo:** gráficos de peso, % de gordura e massa muscular a partir dos check-ins.
    - **Cargas:** filtro por grupo muscular, cards de cada exercício com histórico em grade de 2 colunas, gráfico de evolução e filtro por esquema de repetições quando há mais de um.
    - **Histórico:** lista de treinos; tocar em um treino abre a edição.
  - **Home:**
    - Evolução de peso removida da Home (agora vive em Progresso).
    - Visão geral nova: treinos feitos/meta da semana (com confete ao bater a meta), dias treinados no mês com comparação ▲/▼ ao mês anterior no mesmo período, dias treinados no ano, treinos feitos no programa (soma de todas as letras) e semanas treinando (sequência de semanas que bateram a meta).
    - Atividade agora é um gráfico de barras com dias treinados nos últimos 3 meses mais o atual.
    - O card do treino de hoje mostra o foco muscular (ex.: "Inferior frontal e core") e conta só exercícios ativos.
    - Corrigido erro que impedia os cards de humor e atividade de aparecer quando havia meta semanal definida.
  - **Editar treino:**
    - Exercícios podem ser **inativados** com um switch: ficam apagados, não aparecem nem são cobrados na execução, mas o histórico é preservado. A lixeira remove o exercício com confirmação.
    - Cada exercício mostra série, aumento e peso inicial (ex.: "3×15 • aumento 5kg • inicial 20kg").
    - Tocar no nome do exercício abre o modal para editar repetições, peso inicial e incremento.
    - Botão **+ Adicionar** dentro do cartão da lista; o campo de nome fica com o switch de treino ativo ao lado.
    - Dois gráficos de distribuição muscular: do treino inteiro e do dia selecionado (ignoram exercícios inativos).
  - **Execução do treino:**
    - O botão de pular saiu da barra inferior e virou um checkbox no card do exercício, que pode ser desmarcado depois.
    - A barra de progresso agora chega a 100% no último exercício.
    - No modal de concluir: botão Concluir sempre verde, embaixo; Voltar em cima, e fechar tocando fora.
  - **Visual:** botões Editar, "+" e Voltar com fundo e texto na cor do tema; ícones Material Symbols (lixeira, setas de ordenar, voltar); chips de letra do treino em formato de pílula; acordeão de Configurações unido ao conteúdo; filtros de grupo muscular preenchem a linha toda; bolinha dos gráficos de linha sempre redonda.
- **v1.5.0 — 2026-10-05**
  - Evolução de peso na Home agora mostra todos os treinos do programa (A, B, C…), agrupados por letra, em vez de só o treino ativo.
  - Card "Dias ativos no mês" exibe comparação com o mês anterior (▲/▼).
  - Sequência: se configurada uma meta de treinos por semana, passa a contar semanas consecutivas em que a meta foi batida — em vez de dias seguidos. Semana atual em andamento não quebra a sequência.
  - Perfil > Metas: novo campo **Treinos/semana** para definir a meta semanal.
- **v1.4.0 — 2026-09-17**
  - Corrige tela de editar registro do Histórico, que quebrava (campos e lista de exercícios apareciam lado a lado em vez de empilhados).
  - Nas telas de editar treino e editar histórico, o scroll agora é único: data, calorias, humor e a lista de exercícios rolam juntos, em vez de só a lista rolar separada.
- **v1.3.0 — 2026-09-17**
  - Puxar a tela pra baixo no topo de qualquer aba recarrega o app na hora (pull-to-refresh), como um aplicativo nativo.
  - Gavetas com campo de texto (ex: novo registro de peso) agora se ajustam pra ficar sempre visíveis acima do teclado, mesmo em telas menores.
  - Menu inferior (mobile) com visual de vidro fosco, e diálogos de confirmação ("Sair sem salvar?") com fundo branco sólido.
  - Botão de voltar na tela de adicionar exercício a um treino.
  - Correção de nome de exercício no catálogo padrão.
- **v1.2.0 — 2026-09-17**
  - Layout dedicado para desktop (telas a partir de 960px): menu de navegação no topo em formato de pílula, gavetas viram diálogos centralizados, e as abas Treinos/Histórico/Perfil passam a ser lista + detalhe lado a lado, sem tela cheia.
  - Novo fluxo "Marcar treino feito" no desktop: registra um treino concluído vendo todos os exercícios de uma vez (pesos, humor, calorias), sem passar pelo carrossel de execução guiada — que continua exclusivo do mobile/academia.
  - Dashboard da Home reorganizado em grid de 6 colunas no desktop.
  - Mobile (celular) permanece pixel-idêntico ao de antes; nada muda abaixo de 960px de largura.
- **v1.1.0 — 2026-09-15**
  - Visual novo: tema claro (cards brancos, sombra suave, botões em pílula, fonte Poppins) e modo escuro com vidro fosco e destaque âmbar, alternáveis em Configurações.
  - Aba Treinos: navegação dos treinos A/B/C… por chips, direto na lista, sem precisar abrir a edição.
  - Botão de pular exercício na execução do treino.
  - Card "Como você se sentiu": evolução do humor nas últimas sessões.
  - Card de evolução de peso por exercício (do treino atual), com mini-gráfico de tendência.
  - Painel de Configurações (engrenagem na Home): backup e alternância de tema.
  - Ajustes de layout mobile (menu inferior, tela de editar treino) e correções visuais.
- **v1.0.0 — 2026-09-15**
  - Primeira versão publicada: treinos A–E, execução guiada, histórico editável, backup exportar/importar.
