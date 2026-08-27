# Suporte Agente

Projeto de automação para centralização de rotinas de suporte técnico, Active Directory e Microsoft Configuration Manager.

> [!IMPORTANT]
> Este repositório apresenta exclusivamente documentação, arquitetura conceitual e imagens demonstrativas do projeto.
>
> O código-fonte operacional e as configurações corporativas não estão disponíveis publicamente por questões de segurança, confidencialidade e governança.
>
> Todos os nomes, domínios, servidores, usuários, equipamentos, identificadores e resultados apresentados são fictícios.

## Sobre o projeto

O Suporte Agente surgiu da necessidade de reduzir atividades manuais e repetitivas realizadas durante atendimentos de suporte técnico.

A primeira funcionalidade foi desenvolvida para facilitar a renomeação de computadores sem a necessidade de copiar, adaptar e executar manualmente comandos PowerShell para cada equipamento.

A solução evoluiu para centralizar atividades relacionadas ao Active Directory, Microsoft Configuration Manager, BitLocker, logs e auditoria.

## Objetivo

Centralizar rotinas administrativas recorrentes em uma única interface, buscando melhorar:

- produtividade;
- padronização dos processos;
- segurança operacional;
- rastreabilidade;
- tratamento de erros;
- experiência do profissional de suporte;
- validação das operações executadas.

## Tecnologias utilizadas

- Windows PowerShell 5.1
- Windows Forms
- Active Directory
- Microsoft Configuration Manager
- WMI
- JSON
- CSV
- Logs estruturados
- SHA-256

## Funcionalidades desenvolvidas

### Renomeação

- Renomeação simultânea de até três computadores
- Validação dos nomes informados
- Processamento individualizado
- Grade de resultados
- Logs técnicos

### Active Directory

- Pesquisa exata e parcial de computadores
- Identificação da localização do objeto
- Movimentação controlada entre unidades organizacionais
- Consulta das recuperações BitLocker visíveis
- Exclusão validada de objetos

### Microsoft Configuration Manager

- Pesquisa por nome completo ou parcial
- Pesquisa por usuário conectado
- Pesquisa por número de série
- Consolidação dos resultados pelo ResourceId
- Exclusão controlada e validada

### Logs e auditoria

- Logs técnicos por módulo
- Registros de auditoria
- Identificação do operador
- Registro dos resultados das operações
- Separação entre consultas e ações administrativas
- Controle de tamanho e retenção dos arquivos

## Segurança e governança

A ferramenta foi desenvolvida considerando os seguintes controles:

- credenciais solicitadas somente quando necessárias;
- nenhuma senha armazenada pela aplicação;
- confirmação adicional para ações críticas;
- restrição das movimentações às OUs autorizadas;
- validação após movimentações e exclusões;
- proteção das recuperações BitLocker visíveis;
- exclusão no SCCM vinculada ao ResourceId selecionado;
- registros de auditoria;
- configuração externa em JSON;
- preservação de uma baseline homologada.

## Minha participação

Atuei nas seguintes etapas:

- identificação do problema;
- levantamento e refinamento dos requisitos;
- desenho dos fluxos funcionais;
- definição de regras operacionais;
- testes funcionais;
- identificação de regressões;
- análise de riscos;
- revisão da experiência do usuário;
- documentação técnica;
- controle de versões;
- validação e homologação das entregas.

O desenvolvimento foi realizado com apoio de inteligência artificial como ferramenta para geração, revisão e refinamento do código.

As decisões funcionais, os testes, a análise dos resultados e a homologação foram conduzidos com base em cenários reais de suporte e infraestrutura.

## Principais aprendizados

- Automatizar não significa apenas executar uma tarefa mais rapidamente.
- Ações administrativas precisam de confirmação e validação posterior.
- Credenciais e informações sensíveis não devem ser armazenadas.
- Uma melhoria pode gerar regressões em funcionalidades estáveis.
- Versões homologadas precisam ser preservadas como baseline.
- Logs técnicos e auditorias possuem finalidades diferentes.
- Código, configuração e dados operacionais devem ser separados.
- Uma versão deve ser descartada quando o risco supera o benefício.

## Processo de evolução

O projeto evoluiu de forma incremental:

1. Criação do módulo de renomeação
2. Inclusão das consultas ao Active Directory
3. Pesquisa parcial de computadores
4. Identificação e movimentação entre OUs
5. Tratamento das recuperações BitLocker visíveis
6. Integração com o Microsoft Configuration Manager
7. Pesquisa unificada por máquina, usuário e número de série
8. Implementação de logs e auditoria
9. Aprimoramento da interface
10. Homologação de uma baseline funcional

## Confidencialidade

Este projeto foi desenvolvido em um contexto corporativo.

Por esse motivo, este repositório não contém:

- código-fonte operacional;
- configurações reais;
- nomes de servidores;
- domínios corporativos;
- estruturas reais do Active Directory;
- identificadores do Configuration Manager;
- logs corporativos;
- credenciais;
- informações BitLocker;
- dados de equipamentos ou usuários;
- procedimentos administrativos internos.

## Status

O projeto possui uma baseline funcional e homologada para utilização controlada no ambiente em que foi desenvolvido.

Este repositório tem finalidade exclusivamente demonstrativa e profissional.

## Autor

**Tullio da Silva Medeiros Gomes**

Analista de TI com experiência em suporte corporativo, infraestrutura, Microsoft 365, Active Directory, SCCM, segurança da informação e automação com PowerShell.

## Aviso sobre marcas

Microsoft, Windows, PowerShell, Active Directory e Configuration Manager são marcas de seus respectivos titulares.

Este projeto é independente e não possui afiliação ou endosso da Microsoft.
