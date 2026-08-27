# Aprendizados do projeto

## Identificação do problema

O projeto começou com a identificação de uma atividade recorrente que exigia a execução manual de comandos PowerShell para renomear computadores.

A primeira automação foi desenvolvida para padronizar esse processo e reduzir erros de digitação e adaptação dos comandos.

## Evolução incremental

Após a implementação da renomeação, foram identificadas oportunidades para centralizar outras rotinas relacionadas ao Active Directory e ao Microsoft Configuration Manager.

Cada funcionalidade foi incorporada gradualmente e validada em cenários práticos.

## Controle de versões

Durante o desenvolvimento, diferentes versões foram criadas para incorporar melhorias e correções.

A experiência demonstrou a importância de:

- preservar uma baseline homologada;
- testar mudanças separadamente;
- documentar o objetivo de cada versão;
- descartar versões que apresentem regressões;
- evitar alterações simultâneas em módulos estáveis.

## Regressões

Durante uma tentativa de aprimorar a pesquisa no Configuration Manager, uma alteração aumentou a complexidade e prejudicou o desempenho da consulta.

A versão foi rejeitada e o projeto retornou à baseline homologada.

Essa experiência reforçou que uma melhoria técnica deve ser avaliada pelo seu impacto real, e não apenas pela presença de uma nova funcionalidade.

## Segurança

As principais preocupações de segurança consideradas foram:

- não armazenar senhas;
- solicitar credenciais somente quando necessário;
- proteger informações sensíveis;
- confirmar ações destrutivas;
- validar o resultado das operações;
- registrar ações administrativas;
- restringir movimentações a destinos autorizados;
- preservar rastreabilidade.

## Experiência do usuário

A interface precisa informar claramente:

- quando uma operação está em andamento;
- quando uma ação foi concluída;
- quando existe uma limitação;
- quando uma operação falhou;
- quando um resultado precisa ser validado;
- quando uma ação foi cancelada.

## Uso de inteligência artificial

A inteligência artificial foi utilizada como ferramenta de apoio para geração, revisão e evolução do código.

A definição do problema, os requisitos, os testes, a análise de riscos, a identificação das regressões e a homologação foram conduzidos a partir do conhecimento do ambiente e das atividades de suporte.

## Conclusão

O principal aprendizado foi compreender que automatizar não significa apenas executar uma tarefa mais rapidamente.

Uma automação sustentável também precisa considerar segurança, governança, experiência do usuário, manutenção, tratamento de erros, rastreabilidade e possibilidade de reversão.
