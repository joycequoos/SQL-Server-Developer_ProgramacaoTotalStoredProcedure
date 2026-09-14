# SQL Server Developer — Complete Programming with Stored Procedures

[← Back to Data Engineering](https://github.com/joycequoos/Data_Enginer/blob/main/README.md)

Study material with T-SQL scripts covering everything from language fundamentals (variables, flow control) to more advanced programming objects — Stored Procedures, Views, Functions, Triggers, Transactions, and Error Handling — in SQL Server.

## Table of Contents

- [About T-SQL](#about-t-sql)
- [Language Fundamentals](#language-fundamentals)
- [Variables](#variables)
- [Flow Control](#flow-control)
- [Temporary Tables](#temporary-tables)
- [Transactions](#transactions)
- [Error Handling](#error-handling)
- [Stored Procedures](#stored-procedures)
- [Views](#views)
- [User Defined Functions (UDF)](#user-defined-functions-udf)
- [Triggers](#triggers)
- [Security and Performance](#security-and-performance)
- [Prerequisites](#prerequisites)
- [Next Steps](#next-steps)

---

## About T-SQL

SQL, standardized by ANSI, is the universal language of relational databases (SQL Server, Oracle, MySQL, DB2, PostgreSQL, etc.). Each vendor adds its own extensions — in the case of SQL Server, that extension is **T-SQL (Transact-SQL)**, which adds flow control commands, variables, error handling, and programming objects (procedures, views, functions, triggers) to standard SQL, allowing structured code to be written directly inside the database itself.

## Language Fundamentals

| Script | What It Covers |
| --- | --- |
| [M01 - 01 - 02 - Comentários.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 02 - Coment%C3%A1rios.sql>) | How to comment code in T-SQL |
| [M01 - 01 - 02 - Montagem de scripts.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 02 - Montagem de scripts.sql>) | Structure and organization of a T-SQL script |
| [M01 - 01 - 03 - USE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 03 - USE.sql>) | Selecting the working database with `USE` |
| [M01 - 01 - 04 - Barra invertida.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 04 - Barra invertida.sql>) | Using the backslash (`\`) in scripts |
| [M01 - 01 - 05 - GO.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 05 - GO.sql>) | The `GO` batch separator and how it affects script execution |
| [M01 - 01 - 06 - EXECUTE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 06 - EXECUTE.sql>) | The `EXECUTE`/`EXEC` command |
| [M01 - 01 - 07 - PRINT e RAISERROR.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 07 - PRINT e RAISERROR.sql>) | Displaying messages (`PRINT`) and generating custom errors (`RAISERROR`) |
| [M01 - 01 - 08 - @@ROWCOUNT e ROWCOUNT_BIG().sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 08 - @@ROWCOUNT e ROWCOUNT_BIG().sql>) | Checking how many rows were affected by the last command |
| [M01 - 01 - 09 - SEQUENCE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 09 - SEQUENCE.sql>) | The `SEQUENCE` object, used to generate numeric sequences independent of a table |
| [M01 - 01 - 10 - @@ERROR.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 10 - @@ERROR.sql>) | The `@@ERROR` system variable, used to detect an error in the previous command |
| [M01 - 01 - 11 - SET NOCONT ON.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 01 - 11 - SET NOCONT ON.sql>) | `SET NOCOUNT ON`, used to suppress the affected-row-count message |

## Variables

| Script | What It Covers |
| --- | --- |
| [M01 - 02 - 01 - Definindo uma váriavel.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 01 - Definindo uma v%C3%A1riavel.sql>) | How to declare (`DECLARE`) a variable and its data types |
| [M01 - 02 - 02 - Associando valor.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 02 - Associando valor%20.sql>) | Assigning a value to a variable (`SET` / `SELECT`) |
| [M01 - 02 - 03 - Utilizando variável em instrução DML.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 03 - Utilizando vari%C3%A1vel em instru%C3%A7%C3%A3o DML.sql>) | Using variables inside `INSERT`, `UPDATE`, `DELETE`, and `SELECT` |
| [M01 - 02 - 04 - Erros no uso de variáveis.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 02 - 04 - Erros no uso de vari%C3%A1veis.sql>) | Common mistakes when declaring and using variables |

## Flow Control

| Script | What It Covers |
| --- | --- |
| [M01 - 03 - 01 - Fluxo de Execução.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 01 - Fluxo de Execu%C3%A7%C3%A3o.sql>) | Introduction to flow control in T-SQL |
| [M01 - 03 - 02 - BEGIN END.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 02 - BEGIN END.sql>) | Command blocks with `BEGIN...END` |
| [M01 - 03 - 03 - IF ELSE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 03 - IF ELSE.sql>) | `IF`/`ELSE` conditionals |
| [M01 - 03 - 04 - RETURN.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 04 - RETURN.sql>) | Ending execution and returning a value with `RETURN` |
| [M01 - 03 - 05 - WHILE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 05 - WHILE.sql>) | The `WHILE` loop |
| [M01 - 03 - 06 - TRY CATCH.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 06 - TRY CATCH.sql>) | Basic `TRY...CATCH` structure |
| [M01 - 03 - 07 - BREAK e CONTINUE (next)_.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 07 - BREAK e CONTINUE (next)_.sql>) | Controlling loops with `BREAK` and `CONTINUE` |
| [M01 - 03 - 08 - WAITFOR (Nex).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/M01 - 03 - 08 - WAITFOR (Nex).sql>) | Pausing execution with `WAITFOR` |
| [97 - Utilizando controle de fluxo.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/97 - Utilizando controle de fluxo.sql>) | Additional examples combining flow control commands |
| [99 - BREAK e CONTINUE (Next ).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - BREAK e CONTINUE (Next ).sql>) | Deeper dive into `BREAK` and `CONTINUE` |

## Temporary Tables

| Script | What It Covers |
| --- | --- |
| [01- Tabela Temporária Local.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01- Tabela Tempor%C3%A1ria Local.sql>) | Local temporary tables (`#table`), visible only in the current session |
| [02 -Tabela Temporária Global.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 -Tabela Tempor%C3%A1ria Global.sql>) | Global temporary tables (`##table`), visible to other sessions |
| [03 - Variável tipo Table.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Vari%C3%A1vel tipo Table.sql>) | `TABLE`-type variables, an alternative to temporary tables |
| [04 - Criando um tipo de dado tabela.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Criando um tipo de dado tabela.sql>) | Creating a table data type (`TYPE ... AS TABLE`), used to pass tables as a parameter |
| [17 - Utilizando tabela temporias com procedures.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/17 - Utilizando tabela temporias com procedures.sql>) | Combined use of temporary tables inside Stored Procedures |
| [96 - Utiliza Procedure Temporárias.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/96 - Utiliza Procedure Tempor%C3%A1rias.sql>) | Temporary procedures |

## Transactions

| Script | What It Covers |
| --- | --- |
| [01 - Conceitos e Propriedades.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Conceitos e Propriedades.sql>) | Concepts and ACID properties of a transaction |
| [02 - Comandos de Transação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Comandos de Transa%C3%A7%C3%A3o.sql>) | `BEGIN TRANSACTION`, `COMMIT`, and `ROLLBACK` |
| [03 - Controle da Quantidade de Transações.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Controle da Quantidade de Transa%C3%A7%C3%B5es%20.sql>) | Monitoring how many transactions are open (`@@TRANCOUNT`) |
| [04 - Transações aninhadas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Transa%C3%A7%C3%B5es aninhadas.sql>) | How nested transactions work (and what to watch out for) |
| [05 - Bloqueios.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Bloqueios.sql>) | Locks caused by transactions |
| [06 - Deadlock.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Deadlock.sql>) | How a deadlock happens and how to identify it |
| [07 - Configuração de Bloqueios e Deadlocks.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Configura%C3%A7%C3%A3o de Bloqueios e Deadlocks.sql>) | Settings to prevent/mitigate locks and deadlocks |
| [08 - Utilização do SEQUENCE em transações.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/08 - Utiliza%C3%A7%C3%A3o do SEQUENCE em transa%C3%A7%C3%B5es.sql>) | Using `SEQUENCE` inside transactions |
| [98 - Gerenciando isolamento das transações.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98 - Gerenciando isolamento das transa%C3%A7%C3%B5es.sql>) | Transaction isolation levels |
| [98 - SET XACT_ABORT (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98 - SET XACT_ABORT (Next).sql>) | `SET XACT_ABORT`, to automatically roll back the transaction on error |
| [98- Utilizando controle de transação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98- Utilizando controle de transa%C3%A7%C3%A3o.sql>) | Practical examples of transaction control |
| [99 - Nivel de Isolamento (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - Nivel de Isolamento (Next).sql>) | Deeper dive into isolation levels |
| [99 - SET IMPLICIT_TRANSACTIONS.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - SET IMPLICIT_TRANSACTIONS.sql>) | `SET IMPLICIT_TRANSACTIONS`, which starts transactions implicitly |
| [99 - Utilizando em transações (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - Utilizando em transa%C3%A7%C3%B5es (Next).sql>) | Additional transaction-usage examples |

## Error Handling

| Script | What It Covers |
| --- | --- |
| [01 - Entendendo os erros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Entendendo os erros.sql>) | How SQL Server represents and classifies errors |
| [02 - Severidade dos errros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Severidade dos errros.sql>) | Error severity levels |
| [03 - Encontrando soluções.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Encontrando solu%C3%A7%C3%B5es.sql>) | Strategies for diagnosing and resolving errors |
| [04 - RAISERROR com TRY CATCH.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - RAISERROR com TRY CATCH.sql>) | Combining `RAISERROR` with `TRY...CATCH` |
| [05 - Informações sobre o erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Informa%C3%A7%C3%B5es sobre o erro.sql>) | The `ERROR_MESSAGE()`, `ERROR_NUMBER()`, `ERROR_LINE()`, etc. functions |
| [06 - Armazenando as mensagens de erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Armazenando as mensagens de erro.sql>) | Writing error messages to a log table |
| [07 - Tratamento de erros de transação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Tratamento de erros de transa%C3%A7%C3%A3o.sql>) | Handling errors specifically inside transactions (`ROLLBACK` in the `CATCH` block) |
| [09 - Procedure para tratamento de erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/09 - Procedure para tratamento de erro.sql>) | Centralizing error handling in a reusable procedure |
| [97 - THROW (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/97 - THROW (Next).sql>) | The `THROW` command, a modern alternative to `RAISERROR` |
| [99 - Encontrando erro com Trace (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99 - Encontrando erro com Trace (Next) .sql>) | Using Trace to identify errors |
| [99- Procedure para tratamento de erro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/99- Procedure para tratamento de erro.sql>) | A variation of the central error-handling procedure |

## Stored Procedures

| Script | What It Covers |
| --- | --- |
| [01 - Motivos para usar Stored Procedure.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Motivos para usar Stored Procedure.sql>) | Why use Stored Procedures (reuse, performance, security) |
| [02 - Design de Store Procedure.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Design de Store Procedure .sql>) | How to structure and create a Stored Procedure |
| [03 - Operação com Stored Procedure.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Opera%C3%A7%C3%A3o com Stored Procedure.sql>) | Running and operating an already-created procedure |
| [04 - Retornando um Dataset.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Retornando um Dataset.sql>) | How a procedure returns a result set |
| [05 - Utilizando Parâmetros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Utilizando Par%C3%A2metros.sql>) | Defining input parameters |
| [06 - Valor padrão de parâmetros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Valor padr%C3%A3o de par%C3%A2metros.sql>) | Parameters with a default value (`= NULL`, etc.) |
| [07 - Direção dos Parâmetros.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Dire%C3%A7%C3%A3o dos  Par%C3%A2metros.sql>) | Input vs. output parameters (`OUTPUT`) |
| [08 - Retornando um status.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/08 - Retornando um status.sql>) | Returning an execution status code with `RETURN` |
| [10 - Segurança dos dados.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/10 - Seguran%C3%A7a dos dados.sql>) | How Stored Procedures help protect direct access to data |
| [11 - Procedures Aninhadas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/11 - Procedures Aninhadas.sql>) | Running a procedure inside another and controlling the status of each one |
| [13 - Criptografia vale a pena.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/13 - Criptografia  vale a pena.sql>) | Encrypting (`WITH ENCRYPTION`) a procedure's code — and whether it's worth it |
| [14 - Passando vários dados por um parâmetro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/14 - Passando v%C3%A1rios dados por um par%C3%A2metro.sql>) | Passing multiple values in a single parameter |
| [15 - Passando tabela como parâmetro.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/15 - Passando tabela como par%C3%A2metro.sql>) | Passing an entire table as a parameter (table-valued parameter) |
| [16 - Como retornar vários DataSet.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/16 - Como retornar v%C3%A1rios DataSet.sql>) | Returning multiple result sets in a single call |
| [18 - Criando procedure de sistemas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/18 - Criando procedure de sistemas.sql>) | Creating system procedures (`sp_` in the `master` database) |
| [19 - Procedure na inicialização do SQL Server.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/19 - Procedure na inicializa%C3%A7%C3%A3o do SQL Server.sql>) | Configuring a procedure to run automatically when SQL Server starts (`sp_procoption`) |
| [20 - Compilação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/20 - Compila%C3%A7%C3%A3o.sql>) | How SQL Server compiles and stores a procedure's execution plan |
| [12 - Query dinâmica e SQL Injection.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/12 - Query din%C3%A2mica e SQL Injection.sql>) | SQL Injection risks when building dynamic queries and how to protect against them |

## Views

| Script | What It Covers |
| --- | --- |
| [01 - Motivos para usar Views.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Motivos para usar Views.sql>) | Why use Views (query simplification, security, reuse) |
| [02 - Design de Views.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Design de Views.sql>) | How to create and structure a View |
| [03 - SCHEMABINDING.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - SCHEMABINDING.sql>) | The `SCHEMABINDING` option, which prevents changes to the base table without altering the view |
| [04 - Views Atualizáveis.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Views Atualiz%C3%A1veis.sql>) | Views that accept `INSERT`, `UPDATE`, and `DELETE` |
| [05 - CHECK OPTION.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - CHECK OPTION.sql>) | `WITH CHECK OPTION`, which prevents changes that would violate the view's filter |
| [06 - Erros comuns em Views (Out).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - Erros comuns em Views (Out).sql>) | Common errors and limitations when working with views |
| [07 - Views Indexáveis (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Views Indexáveis (Next).sql>) | Indexed views, to improve access performance |
| [08 - Restrições na instução SELECT (Out).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/08- Restrições na instução SELECT (Out).sql>) | `SELECT` restrictions inside a view |
| [09 - Views Particionadas (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/09 - Views Particionadas (Next).sql>) | Partitioned views, which combine data from similar tables |

## User Defined Functions (UDF)

| Script | What It Covers |
| --- | --- |
| [01 - Design de User Defined Functions.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Design de User Defined Functions.sql>) | Introduction to designing user-defined Functions |
| [02 - Scalar Functions.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Scalar Functions.sql>) | Scalar Functions, which return a single value |
| [03 - Inline Table Valued Function.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Inline Table Valued Function.sql>) | Functions that return a table through a single `SELECT` |
| [04 - Multistatement Table Valued Function.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Multistatement Table Valued Function.sql>) | Functions that return a table built across multiple statements |
| [05 - Quando utilizar as UDF.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/05 - Quando utilizar as UDF.sql>) | When it makes sense to use a function instead of a procedure |

## Triggers

| Script | What It Covers |
| --- | --- |
| [01 - Desgin de Triggers.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/01 - Desgin de Triggers.sql>) | How to create and structure a trigger |
| [02 - Pseudos Tabelas INSERTED e DELETED.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/02 - Pseudos Tabelas INSERTED e DELETED.sql>) | The `INSERTED` and `DELETED` virtual tables, used inside triggers |
| [03 - Controlar execução pelas linhas afetadas.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/03 - Controlar execu%C3%A7%C3%A3o pelas linhas afetadas.sql>) | Controlling the trigger's logic based on how many rows were affected |
| [04 - Controlar a execução pela coluna alterada.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/04 - Controlar a execu%C3%A7%C3%A3o pela coluna alterada.sql>) | Running conditional logic based on which column was changed (`UPDATE()`/`COLUMNS_UPDATED()`) |

## Security and Performance

| Script | What It Covers |
| --- | --- |
| [12 - Query dinâmica e SQL Injection.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/12 - Query din%C3%A2mica e SQL Injection.sql>) | Security risks when building dynamic SQL and best practices to avoid SQL Injection |
| [07 - Topicos de Desempenho.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/07 - Topicos de Desempenho.sql>) | General T-SQL performance best practices |
| [06 - (Preview) Utilizando SEQUENCE.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/06 - (Preview) Utilizando SEQUENCE.sql>) | Advanced use of `SEQUENCE` |
| [98 - Evite o uso de SELECT INTO (Next).sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/98 - Evite o uso de SELECT INTO (Next) .sql>) | Why to avoid `SELECT INTO` in certain scenarios |
| [20 - Compilação.sql](<https://github.com/joycequoos/SQL-Server-Developer_ProgramacaoTotalStoredProcedure/blob/main/20 - Compila%C3%A7%C3%A3o.sql>) | The impact of compilation/recompilation on procedure performance |

## Prerequisites

- [ ] Knowledge of the `SELECT`, `INSERT`, `UPDATE`, `DELETE` commands and table creation.
- [ ] SQL Server installed (e.g., SQL Server Express Edition).
- [ ] Basic understanding of programming logic.

## Next Steps

- Consolidate the numbered scripts without the `M01` prefix into topic-based folders (`Transactions/`, `Procedures/`, `Views/`, `Functions/`, `Triggers/`, `ErrorHandling/`), since today they're all loose at the root of the repository.
- Standardize file naming (remove extra spaces, inconsistent accents, and suffixes like `(Next)`/`(Out)` that look like personal notes).
- Add input/output examples for the more advanced scripts (e.g., nested procedures, table-valued parameters).
- Document the `.ssmssqlproj` files, which group each lesson's scripts as a SQL Server Management Studio project.
