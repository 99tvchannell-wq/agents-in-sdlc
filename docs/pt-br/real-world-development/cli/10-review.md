---
title: "Lição 10 - Revisão e próximos passos"
description: "Recapitule o fluxo de trabalho do Copilot CLI, as duas pull requests, as personalizações reutilizáveis e outros recursos."
authors:
  - geektrainer
lastUpdated: 2026-09-29
---

Você usou o GitHub Copilot CLI em um fluxo de trabalho contínuo no Tailspin Toys. Neste workshop, você:

- Preparou um Codespace, instalou o Copilot CLI, explorou o projeto e encontrou o issue de filtragem preparado.
- Adicionou avaliações com estrelas, revisou o resultado em um navegador encaminhado e fez o merge manual da primeira pull request (PR).
- Começou pelo issue de filtragem, definiu a abordagem no modo Plan, implementou no modo Autopilot e revisou no modo Interactive.
- Orientou o agente com instruções personalizadas, personalizou a skill `quality-checks` existente e usou-a para executar testes unitários, lint e verificações de tipos.
- Adicionou o servidor Model Context Protocol (MCP) do Playwright e usou-o para explorar a filtragem em um navegador real.
- Criou e selecionou um agente personalizado de garantia de qualidade (QA) para avaliar requisitos, cobertura, resultados da skill e evidências do navegador.
- Revisou toda a alteração de filtragem e autorizou o Agent Merge para a PR correspondente.
- Explorou comandos de barra para contexto, modelos, compartilhamento e delegação opcional ao agente de nuvem.

## O que você entregou

O workshop tem dois marcos de PR, cada um em sua própria branch criada a partir de `main` atualizada:

1. **Avaliações com estrelas:** exibe o `starRating` existente e um estado explícito para jogos sem avaliação nos cartões.
2. **Filtragem e fluxo de qualidade:** implementa a filtragem, atualiza as instruções e as aplica ao recurso, personaliza o relatório de `quality-checks`, cria um perfil de QA e inclui os testes associados.

Do planejamento da filtragem até a abertura da PR, você usou a mesma conversa e branch. Para simplificar o workshop, reunimos esse trabalho em uma única PR.

## Diferentes formas de verificação

Você verificou o código de várias maneiras: testes automatizados, inspeção no navegador e exploração do navegador pelo Copilot usando MCP. A skill `quality-checks` executou testes unitários, lint e verificações de tipos e apresentou os resultados no novo formato. Antes da PR, o QA reuniu esses resultados com uma revisão dos requisitos e da cobertura de testes.

Os testes adicionados devem preencher lacunas reais; uma execução de QA que não exija novos testes também pode estar correta. Revise o código e as evidências antes de autorizar o merge e atualize as evidências afetadas depois de qualquer alteração.

## Práticas recomendadas

O contexto e as ferramentas que você fornece ao Copilot influenciam o trabalho. Neste workshop, você atualizou instruções, personalizou uma skill, criou um perfil de QA e configurou um servidor MCP. Reutilize essas personalizações entre conversas e ajuste-as conforme as necessidades da equipe. Instruções definem padrões, skills descrevem tarefas repetíveis, agentes personalizados definem funções especializadas e servidores MCP conectam ferramentas externas. Revise as alterações e os resultados reais das ferramentas, não apenas o resumo do agente.

Escolha o **modo e o modelo** de acordo com a tarefa. Use **Plan** para pensar em uma abordagem antes de construir, **Interactive** para acompanhar alterações bem delimitadas e **Autopilot** para delegar tarefas com escopo claro. Escolha um modelo mais rápido para edições rotineiras e um modelo mais avançado para tarefas complexas.

O contexto é tão importante quanto a infraestrutura. Descrever com clareza *o que* você quer criar, *por que* e *como* muda bastante o resultado.

## Mais recursos para explorar

Você concluiu o fluxo de trabalho principal. Confira outros recursos do Copilot CLI:

- Use `/review` para pedir que o agente de revisão de código analise as alterações.
- Use `/rubber-duck` para conversar sobre um problema e obter outra perspectiva.
- Use `/fleet` para coordenar subtarefas independentes em paralelo.
- Use `/worktree` para isolar uma tarefa separada.
- Use `/delegate` para enviar uma tarefa ao agente de nuvem do Copilot.

## Próximos passos

A melhor maneira de melhorar no uso de qualquer ferramenta é continuar usando-a. Experimente em código de produção, em projetos pessoais ou naquele pequeno aplicativo que você pensa em criar há anos. Compartilhe o que aprendeu com a equipe e aprenda com a experiência de outras pessoas. E, como sempre, explore a documentação.

Se quiser ampliar o Tailspin Toys pelo terminal, continue com a série opcional [Foundry Backer Concierge][foundry]. Para comparar outros ambientes, explore o [workshop do VS Code][vscode], o [workshop do aplicativo GitHub Copilot][app] ou o [workshop do agente de nuvem do Copilot][cloud].

## Recursos

- [Sobre o GitHub Copilot CLI][about-cli]
- [Referência de comandos do Copilot CLI][cli-reference]
- [Personalize o Copilot CLI][customize-cli]
- [Gerencie pull requests com o Copilot CLI][manage-prs]

[previous-lesson]: ../9-cli-power-tools/
[foundry]: ../8-foundry-agent/
[vscode]: ../../vscode/
[app]: ../../app/
[cloud]: ../../cloud/
[about-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
[customize-cli]: https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
