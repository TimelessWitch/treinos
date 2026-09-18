# FitFlow

App de treino pessoal — acompanhamento de treinos, exercícios e histórico, direto no navegador.

🔗 **Acesse em:** https://timelesswitch.github.io/treinos/

## O que faz

- Organiza treinos em programas (ex: Treino A, B, C…) com séries, repetições e observações por exercício, navegáveis por abas dentro da própria lista de Treinos.
- Execução guiada do treino, com ajuste de carga e botão de pular exercício (marcar como não feito).
- Histórico editável: data, calorias, humor e o que foi feito ou não em cada sessão.
- Catálogo de exercícios com distribuição por grupo muscular.
- Home com visão geral: próximo treino, estatísticas, evolução de carga por exercício, humor ao longo das sessões e mapa de atividade.
- Tema claro e escuro (alternável em Configurações), backup exportar/importar.

## Onde ficam os dados

Tudo é salvo no **localStorage do navegador** — não tem servidor nem banco de dados. Isso significa:

- Os dados ficam só nesse navegador/aparelho; não sincronizam entre dispositivos.
- Limpar os dados do navegador apaga o progresso.
- Use os botões **Exportar/Importar** (em Configurações, ícone de engrenagem na Home) pra fazer backup em arquivo `.json` sempre que quiser.

## Rodando localmente

É um único arquivo HTML autocontido (sem build, sem dependências). Basta abrir `index.html` no navegador.

## Histórico de versões

Cada versão publicada fica marcada com uma tag no repositório — dá pra voltar a qualquer uma delas (`git checkout v1.0.0`, por exemplo) se algo quebrar.

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
