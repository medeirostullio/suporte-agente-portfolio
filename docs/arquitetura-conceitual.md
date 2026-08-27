# Arquitetura conceitual

## Visão geral

O Suporte Agente utiliza uma interface Windows Forms desenvolvida em Windows PowerShell 5.1 para centralizar rotinas administrativas recorrentes.

## Fluxo conceitual

Usuário autorizado

↓  

Interface Windows Forms

↓  

Camada de validação

↓  

Provedores administrativos

- Gerenciamento de computadores
- Active Directory
- Microsoft Configuration Manager

↓  

Logs técnicos e auditoria

## Componentes

### Interface

Responsável por:

- entrada dos dados;
- apresentação dos resultados;
- mensagens de status;
- confirmação das ações;
- seleção dos registros.

### Validação

Responsável por:

- verificar campos obrigatórios;
- validar nomes;
- limitar quantidade de consultas;
- impedir ações inconsistentes;
- restringir operações críticas.

### Active Directory

Responsável conceitualmente por:

- pesquisa de computadores;
- identificação da localização;
- movimentação entre destinos permitidos;
- consulta de informações autorizadas;
- exclusão validada.

### Microsoft Configuration Manager

Responsável conceitualmente por:

- pesquisa por equipamento;
- pesquisa por usuário;
- pesquisa por número de série;
- consolidação dos resultados;
- exclusão controlada de registros.

### Logs e auditoria

Responsáveis por registrar:

- data e hora;
- versão da aplicação;
- operação executada;
- resultado;
- identidade utilizada;
- equipamento relacionado;
- identificador da operação.

## Configuração

As informações do ambiente são carregadas a partir de uma configuração externa.

O repositório público não contém a configuração utilizada em produção.

## Segurança

As credenciais são solicitadas durante as operações administrativas e não são armazenadas pela aplicação.

As ações críticas exigem confirmação e são submetidas a validação posterior.

## Limitações

A aplicação depende da disponibilidade, conectividade e permissões dos serviços administrativos utilizados.

Este documento apresenta apenas a arquitetura conceitual e não contém detalhes operacionais do ambiente.
