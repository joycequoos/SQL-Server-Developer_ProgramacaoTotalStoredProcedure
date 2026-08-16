
# SQL Server Developer — Programação Total com Stored Procedure

[← Voltar a SQL](https://github.com/joycequoos/SQL/blob/main/README.md)

Material de estudo com scripts T-SQL cobrindo desde os fundamentos da linguagem (variáveis, controle de fluxo) até objetos de programação mais avançados — Stored Procedures, Views, Functions, Triggers, Transações e Tratamento de Erros — no SQL Server.

## Índice

- [Sobre o T-SQL](#sobre-o-t-sql)
- [Fundamentos da linguagem](#fundamentos-da-linguagem)
- [Variáveis](#variáveis)
- [Controle de fluxo](#controle-de-fluxo)
- [Tabelas temporárias](#tabelas-temporárias)
- [Transações](#transações)
- [Tratamento de erros](#tratamento-de-erros)
- [Stored Procedures](#stored-procedures)
- [Views](#views)
- [User Defined Functions (UDF)](#user-defined-functions-udf)
- [Triggers](#triggers)
- [Segurança e performance](#segurança-e-performance)
- [Pré-requisitos](#pré-requisitos)
- [Próximos passos](#próximos-passos)

---

## Sobre o T-SQL

O SQL, padronizado pela ANSI, é a linguagem universal dos bancos de dados relacionais (SQL Server, Oracle, MySQL, DB2, PostgreSQL, etc.). Cada fornecedor adiciona suas próprias extensões — no caso do SQL Server, essa extensão é o **T-SQL (Transact-SQL)**, que acrescenta ao SQL padrão comandos de controle de fluxo, variáveis, tratamento de erros e objetos de programação (procedures, views, functions, triggers), permitindo escrever código estruturado dentro do próprio banco de dados.

## Fundamentos da linguagem

| Script | O que cobre |
| --- | --- |
| [M01 - 01 - 02 - Comentários.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 02 - Coment%C3%A1rios.sql>) | Como comentar código em T-SQL |
| [M01 - 01 - 02 - Montagem de scripts.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 02 - Montagem de scripts.sql>) | Estrutura e organização de um script T-SQL |
| [M01 - 01 - 03 - USE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 03 - USE.sql>) | Selecionar o banco de dados de trabalho com `USE` |
| [M01 - 01 - 04 - Barra invertida.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 04 - Barra invertida.sql>) | Uso da barra invertida (`\`) em scripts |
| [M01 - 01 - 05 - GO.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 05 - GO.sql>) | O separador de lote `GO` e como ele afeta a execução do script |
| [M01 - 01 - 06 - EXECUTE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 06 - EXECUTE.sql>) | O comando `EXECUTE`/`EXEC` |
| [M01 - 01 - 07 - PRINT e RAISERROR.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 07 - PRINT e RAISERROR.sql>) | Exibir mensagens (`PRINT`) e gerar erros customizados (`RAISERROR`) |
| [M01 - 01 - 08 - @@ROWCOUNT e ROWCOUNT_BIG().sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 08 - @@ROWCOUNT e ROWCOUNT_BIG().sql>) | Verificar a quantidade de linhas afetadas pelo último comando |
| [M01 - 01 - 09 - SEQUENCE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 09 - SEQUENCE.sql>) | Objeto `SEQUENCE`, usado para gerar sequências numéricas independentes de uma tabela |
| [M01 - 01 - 10 - @@ERROR.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 10 - @@ERROR.sql>) | A variável de sistema `@@ERROR`, usada para detectar erro no comando anterior |
| [M01 - 01 - 11 - SET NOCONT ON.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 11 - SET NOCONT ON.sql>) | `SET NOCOUNT ON`, usado para suprimir a mensagem de contagem de linhas afetadas |

## Variáveis

| Script | O que cobre |
| --- | --- |
| [M01 - 02 - 01 - Definindo uma váriavel.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 01 - Definindo uma v%C3%A1riavel.sql>) | Como declarar (`DECLARE`) uma variável e seus tipos de dados |
| [M01 - 02 - 02 - Associando valor.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 02 - Associando valor%20.sql>) | Atribuir valor a uma variável (`SET` / `SELECT`) |
| [M01 - 02 - 03 - Utilizando variável em instrução DML.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 03 - Utilizando vari%C3%A1vel em instru%C3%A7%C3%A3o DML.sql>) | Usar variáveis dentro de `INSERT`, `UPDATE`, `DELETE` e `SELECT` |
| [M01 - 02 - 04 - Erros no uso de variáveis.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 04 - Erros no uso de vari%C3%A1veis.sql>) | Erros comuns ao declarar e usar variáveis |

## Controle de fluxo

| Script | O que cobre |
| --- | --- |
| [M01 - 03 - 01 - Fluxo de Execução.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 01 - Fluxo de Execu%C3%A7%C3%A3o.sql>) | Introdução ao controle de fluxo em T-SQL |
| [M01 - 03 - 02 - BEGIN END.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 02 - BEGIN END.sql>) | Blocos de comando com `BEGIN...END` |
| [M01 - 03 - 03 - IF ELSE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 03 - IF ELSE.sql>) | Condicionais `IF`/`ELSE` |
| [M01 - 03 - 04 - RETURN.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 04 - RETURN.sql>) | Encerrar a execução e retornar um valor com `RETURN` |
| [M01 - 03 - 05 - WHILE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 05 - WHILE.sql>) | Laço de repetição `WHILE` |
| [M01 - 03 - 06 - TRY CATCH.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 06 - TRY CATCH.sql>) | Estrutura básica de `TRY...CATCH` |
| [M01 - 03 - 07 - BREAK e CONTINUE (next)_.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 07 - BREAK e CONTINUE (next)_.sql>) | Controlar laços com `BREAK` e `CONTINUE` |
| [M01 - 03 - 08 - WAITFOR (Nex).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 08 - WAITFOR (Nex).sql>) | Pausar a execução com `WAITFOR` |
| [97 - Utilizando controle de fluxo.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/97 - Utilizando controle de fluxo.sql>) | Exemplos adicionais combinando os comandos de controle de fluxo |
| [99 - BREAK e CONTINUE (Next ).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - BREAK e CONTINUE (Next ).sql>) | Aprofundamento de `BREAK` e `CONTINUE` |

## Tabelas temporárias

| Script | O que cobre |
| --- | --- |
| [01- Tabela Temporária Local.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01- Tabela Tempor%C3%A1ria Local.sql>) | Tabelas temporárias locais (`#tabela`), visíveis apenas na sessão atual |
| [02 -Tabela Temporária Global.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 -Tabela Tempor%C3%A1ria Global.sql>) | Tabelas temporárias globais (`##tabela`), visíveis para outras sessões |
| [03 - Variável tipo Table.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Vari%C3%A1vel tipo Table.sql>) | Variáveis do tipo `TABLE`, alternativa às tabelas temporárias |
| [04 - Criando um tipo de dado tabela.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Criando um tipo de dado tabela.sql>) | Criação de um tipo de dado tabela (`TYPE ... AS TABLE`), usado para passar tabelas como parâmetro |
| [17 - Utilizando tabela temporias com procedures.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/17 - Utilizando tabela temporias com procedures.sql>) | Uso combinado de tabelas temporárias dentro de Stored Procedures |
| [96 - Utiliza Procedure Temporárias.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/96 - Utiliza Procedure Tempor%C3%A1rias.sql>) | Procedures temporárias |

## Transações

| Script | O que cobre |
| --- | --- |
| [01 - Conceitos e Propriedades.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Conceitos e Propriedades.sql>) | Conceitos e propriedades ACID de uma transação |
| [02 - Comandos de Transação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Comandos de Transa%C3%A7%C3%A3o.sql>) | `BEGIN TRANSACTION`, `COMMIT` e `ROLLBACK` |
| [03 - Controle da Quantidade de Transações.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Controle da Quantidade de Transa%C3%A7%C3%B5es%20.sql>) | Monitorar quantas transações estão abertas (`@@TRANCOUNT`) |
| [04 - Transações aninhadas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Transa%C3%A7%C3%B5es aninhadas.sql>) | Como funcionam (e os cuidados com) transações aninhadas |
| [05 - Bloqueios.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Bloqueios.sql>) | Bloqueios (locks) causados por transações |
| [06 - Deadlock.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Deadlock.sql>) | Como um deadlock acontece e como identificá-lo |
| [07 - Configuração de Bloqueios e Deadlocks.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Configura%C3%A7%C3%A3o de Bloqueios e Deadlocks.sql>) | Configurações para prevenir/mitigar bloqueios e deadlocks |
| [08 - Utilização do SEQUENCE em transações.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/08 - Utiliza%C3%A7%C3%A3o do SEQUENCE em transa%C3%A7%C3%B5es.sql>) | Uso de `SEQUENCE` dentro de transações |
| [98 - Gerenciando isolamento das transações.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98 - Gerenciando isolamento das transa%C3%A7%C3%B5es.sql>) | Níveis de isolamento de transação |
| [98 - SET XACT_ABORT (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98 - SET XACT_ABORT (Next).sql>) | `SET XACT_ABORT`, para desfazer a transação automaticamente em caso de erro |
| [98- Utilizando controle de transação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98- Utilizando controle de transa%C3%A7%C3%A3o.sql>) | Exemplos práticos de controle transacional |
| [99 - Nivel de Isolamento (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - Nivel de Isolamento (Next).sql>) | Aprofundamento nos níveis de isolamento |
| [99 - SET IMPLICIT_TRANSACTIONS.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - SET IMPLICIT_TRANSACTIONS.sql>) | `SET IMPLICIT_TRANSACTIONS`, que inicia transações implicitamente |
| [99 - Utilizando em transações (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - Utilizando em transa%C3%A7%C3%B5es (Next).sql>) | Exemplos adicionais de uso de transações |

## Tratamento de erros

| Script | O que cobre |
| --- | --- |
| [01 - Entendendo os erros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Entendendo os erros.sql>) | Como o SQL Server representa e classifica erros |
| [02 - Severidade dos errros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Severidade dos errros.sql>) | Níveis de severidade de um erro |
| [03 - Encontrando soluções.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Encontrando solu%C3%A7%C3%B5es.sql>) | Estratégias para diagnosticar e resolver erros |
| [04 - RAISERROR com TRY CATCH.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - RAISERROR com TRY CATCH.sql>) | Combinando `RAISERROR` com `TRY...CATCH` |
| [05 - Informações sobre o erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Informa%C3%A7%C3%B5es sobre o erro.sql>) | Funções `ERROR_MESSAGE()`, `ERROR_NUMBER()`, `ERROR_LINE()`, etc. |
| [06 - Armazenando as mensagens de erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Armazenando as mensagens de erro.sql>) | Gravar mensagens de erro em uma tabela de log |
| [07 - Tratamento de erros de transação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Tratamento de erros de transa%C3%A7%C3%A3o.sql>) | Tratar erros especificamente dentro de transações (`ROLLBACK` no `CATCH`) |
| [09 - Procedure para tratamento de erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/09 - Procedure para tratamento de erro.sql>) | Centralizar o tratamento de erro em uma procedure reutilizável |
| [97 - THROW (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/97 - THROW (Next).sql>) | O comando `THROW`, alternativa moderna ao `RAISERROR` |
| [99 - Encontrando erro com Trace (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - Encontrando erro com Trace (Next) .sql>) | Uso de Trace para identificar erros |
| [99- Procedure para tratamento de erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99- Procedure para tratamento de erro.sql>) | Variação da procedure central de tratamento de erro |

## Stored Procedures

| Script | O que cobre |
| --- | --- |
| [01 - Motivos para usar Stored Procedure.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Motivos para usar Stored Procedure.sql>) | Por que usar Stored Procedures (reuso, performance, segurança) |
| [02 - Design de Store Procedure.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Design de Store Procedure .sql>) | Como estruturar e criar uma Stored Procedure |
| [03 - Operação com Stored Procedure.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Opera%C3%A7%C3%A3o com Stored Procedure.sql>) | Executando e operando uma procedure já criada |
| [04 - Retornando um Dataset.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Retornando um Dataset.sql>) | Como uma procedure retorna um conjunto de resultados |
| [05 - Utilizando Parâmetros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Utilizando Par%C3%A2metros.sql>) | Definindo parâmetros de entrada |
| [06 - Valor padrão de parâmetros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Valor padr%C3%A3o de par%C3%A2metros.sql>) | Parâmetros com valor padrão (`= NULL`, etc.) |
| [07 - Direção dos Parâmetros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Dire%C3%A7%C3%A3o dos  Par%C3%A2metros.sql>) | Parâmetros de entrada vs. saída (`OUTPUT`) |
| [08 - Retornando um status.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/08 - Retornando um status.sql>) | Retornar um código de status de execução com `RETURN` |
| [10 - Segurança dos dados.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/10 - Seguran%C3%A7a dos dados.sql>) | Como Stored Procedures ajudam a proteger o acesso direto aos dados |
| [11 - Procedures Aninhadas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/11 - Procedures Aninhadas.sql>) | Executar uma procedure dentro de outra e controlar o status de cada uma |
| [13 - Criptografia vale a pena.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/13 - Criptografia  vale a pena.sql>) | Criptografar (`WITH ENCRYPTION`) o código de uma procedure — e se vale a pena |
| [14 - Passando vários dados por um parâmetro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/14 - Passando v%C3%A1rios dados por um par%C3%A2metro.sql>) | Passar múltiplos valores em um único parâmetro |
| [15 - Passando tabela como parâmetro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/15 - Passando tabela como par%C3%A2metro.sql>) | Passar uma tabela inteira como parâmetro (table-valued parameter) |
| [16 - Como retornar vários DataSet.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/16 - Como retornar v%C3%A1rios DataSet.sql>) | Retornar múltiplos conjuntos de resultados em uma única chamada |
| [18 - Criando procedure de sistemas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/18 - Criando procedure de sistemas.sql>) | Criar procedures de sistema (`sp_` no banco `master`) |
| [19 - Procedure na inicialização do SQL Server.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/19 - Procedure na inicializa%C3%A7%C3%A3o do SQL Server.sql>) | Configurar uma procedure para rodar automaticamente ao iniciar o SQL Server (`sp_procoption`) |
| [20 - Compilação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/20 - Compila%C3%A7%C3%A3o.sql>) | Como o SQL Server compila e armazena o plano de execução de uma procedure |
| [12 - Query dinâmica e SQL Injection.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/12 - Query din%C3%A2mica e SQL Injection.sql>) | Riscos de SQL Injection ao montar queries dinâmicas e como se proteger |

## Views

| Script | O que cobre |
| --- | --- |
| [01 - Motivos para usar Views.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Motivos para usar Views.sql>) | Por que usar Views (simplificação de consultas, segurança, reuso) |
| [02 - Design de Views.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Design de Views.sql>) | Como criar e estruturar uma View |
| [03 - SCHEMABINDING.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - SCHEMABINDING.sql>) | Opção `SCHEMABINDING`, que impede alterações na tabela base sem alterar a view |
| [04 - Views Atualizáveis.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Views Atualiz%C3%A1veis.sql>) | Views que aceitam `INSERT`, `UPDATE` e `DELETE` |
| [05 - CHECK OPTION.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - CHECK OPTION.sql>) | `WITH CHECK OPTION`, que impede alterações que violem o filtro da view |
| [06 - Erros comuns em Views (Out).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Erros comuns em Views (Out).sql>) | Erros e limitações comuns ao trabalhar com views |
| [07 - Views Indexáveis (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Views Indexáveis (Next).sql>) | Views indexadas, para melhorar a performance de acesso |
| [08 - Restrições na instução SELECT (Out).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/08- Restrições na instução SELECT (Out).sql>) | Restrições do `SELECT` dentro de uma view |
| [09 - Views Particionadas (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/09 - Views Particionadas (Next).sql>) | Views particionadas, que combinam dados de tabelas semelhantes |

## User Defined Functions (UDF)

| Script | O que cobre |
| --- | --- |
| [01 - Design de User Defined Functions.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Design de User Defined Functions.sql>) | Introdução ao design de Functions definidas pelo usuário |
| [02 - Scalar Functions.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Scalar Functions.sql>) | Functions escalares, que retornam um único valor |
| [03 - Inline Table Valued Function.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Inline Table Valued Function.sql>) | Functions que retornam uma tabela através de um único `SELECT` |
| [04 - Multistatement Table Valued Function.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Multistatement Table Valued Function.sql>) | Functions que retornam uma tabela construída em múltiplas instruções |
| [05 - Quando utilizar as UDF.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Quando utilizar as UDF.sql>) | Quando faz sentido usar uma function em vez de uma procedure |

## Triggers

| Script | O que cobre |
| --- | --- |
| [01 - Desgin de Triggers.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Desgin de Triggers.sql>) | Como criar e estruturar uma trigger |
| [02 - Pseudos Tabelas INSERTED e DELETED.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Pseudos Tabelas INSERTED e DELETED.sql>) | As tabelas virtuais `INSERTED` e `DELETED`, usadas dentro de triggers |
| [03 - Controlar execução pelas linhas afetadas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Controlar execu%C3%A7%C3%A3o pelas linhas afetadas.sql>) | Controlar a lógica da trigger com base em quantas linhas foram afetadas |
| [04 - Controlar a execução pela coluna alterada.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Controlar a execu%C3%A7%C3%A3o pela coluna alterada.sql>) | Executar lógica condicional com base em qual coluna foi alterada (`UPDATE()`/`COLUMNS_UPDATED()`) |

## Segurança e performance

| Script | O que cobre |
| --- | --- |
| [12 - Query dinâmica e SQL Injection.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/12 - Query din%C3%A2mica e SQL Injection.sql>) | Riscos de segurança ao montar SQL dinâmico e boas práticas para evitar SQL Injection |
| [07 - Topicos de Desempenho.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Topicos de Desempenho.sql>) | Boas práticas gerais de performance em T-SQL |
| [06 - (Preview) Utilizando SEQUENCE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - (Preview) Utilizando SEQUENCE.sql>) | Uso avançado de `SEQUENCE` |
| [98 - Evite o uso de SELECT INTO (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98 - Evite o uso de SELECT INTO (Next) .sql>) | Por que evitar `SELECT INTO` em determinados cenários |
| [20 - Compilação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/20 - Compila%C3%A7%C3%A3o.sql>) | Impacto da compilação/recompilação no desempenho de procedures |

## Pré-requisitos

- [ ] Conhecimento dos comandos `SELECT`, `INSERT`, `UPDATE`, `DELETE` e criação de tabelas.
- [ ] SQL Server instalado (ex.: SQL Server Express Edition).
- [ ] Noções básicas de lógica de programação.

## Próximos passos

- Consolidar os scripts numerados sem prefixo `M01` em pastas por tópico (`Transacoes/`, `Procedures/`, `Views/`, `Functions/`, `Triggers/`, `ErroTratamento/`), já que hoje todos ficam soltos na raiz do repositório.
- Padronizar a nomenclatura dos arquivos (remover espaços extras, acentos inconsistentes e sufixos como `(Next)`/`(Out)` que parecem anotações pessoais).
- Adicionar exemplos de entrada/saída para os scripts mais avançados (ex.: procedures aninhadas, table-valued parameters).
- Documentar os arquivos `.ssmssqlproj`, que agrupam os scripts de cada lição como projeto do SQL Server Management Studio.
