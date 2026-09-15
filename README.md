# FitFlow

App de treino pessoal — acompanhamento de treinos, exercícios e histórico, direto no navegador.

🔗 **Acesse em:** https://timelesswitch.github.io/treinos/

## O que faz

- Organiza treinos em programas (ex: Treino A, B, C…) com séries, repetições e observações por exercício.
- Execução guiada do treino, com ajuste de carga e opção de marcar exercícios como não feitos.
- Histórico editável: data, calorias, humor e o que foi feito ou não em cada sessão.
- Catálogo de exercícios com distribuição por grupo muscular.

## Onde ficam os dados

Tudo é salvo no **localStorage do navegador** — não tem servidor nem banco de dados. Isso significa:

- Os dados ficam só nesse navegador/aparelho; não sincronizam entre dispositivos.
- Limpar os dados do navegador apaga o progresso.
- Use os botões **Exportar/Importar** (na aba Home) pra fazer backup em arquivo `.json` sempre que quiser.

## Rodando localmente

É um único arquivo HTML autocontido (sem build, sem dependências). Basta abrir `index.html` no navegador.
