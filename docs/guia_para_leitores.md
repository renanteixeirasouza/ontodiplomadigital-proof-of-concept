# Guia para leitura do repositório

Este guia foi escrito para leitores que desejam entender a prova de conceito sem precisar conhecer previamente ontologias, RDF ou SPARQL.

## Ideia geral

A prova de conceito mostra como informações de um diploma digital podem ser transformadas em um grafo de conhecimento. Em vez de tratar os dados apenas como linhas de uma tabela, a ontologia representa cada elemento importante como um recurso identificável: diploma, diplomado, curso, instituição emissora, instituição registradora, registro, assinatura, carimbo de tempo e código de validação.

Esses recursos são ligados entre si por relações explícitas. Por exemplo:

- um diploma tem um titular;
- um diploma está vinculado a um curso;
- um diploma foi emitido por uma instituição;
- um diploma foi registrado por outra instituição;
- um registro possui responsável, data e processo administrativo;
- uma assinatura possui formato, papel e carimbo de tempo.

## Arquivos principais

### 1. Ontologia

A pasta `ontologia/` contém dois arquivos principais:

- `OntoDiplomaDigital_registro_diploma.ttl`: estrutura formal da ontologia, com classes, propriedades, restrições, vocabulários controlados e notas de documentação;
- `ontologia_operacional_individuos_ficticios_registro_diploma_publico.ttl`: conjunto de exemplos fictícios usado para demonstrar a aplicação da ontologia.

Em termos simples, o primeiro arquivo define o modelo; o segundo mostra exemplos de dados representados por esse modelo.

### 2. Dados tabulares

A pasta `dados/` contém arquivos CSV usados para inspeção e apoio à prova de conceito. Eles ajudam o leitor a observar a passagem de uma estrutura tabular para uma representação em RDF.

### 3. Consultas SPARQL

A pasta `consultas_sparql/` contém perguntas executáveis sobre o grafo. Essas consultas mostram quais informações podem ser recuperadas quando os dados são representados semanticamente.

As consultas 01 a 07 estão relacionadas às questões de competência da ontologia. As consultas 08 e 09 são demonstrações de leitura mais direta:

- `08_demo_visao_360_diploma_por_cpf.rq`: retorna uma visão tabular consolidada de um diploma a partir de um CPF fictício;
- `09_demo_grafo_diploma_por_cpf.rq`: gera um grafo visual com as principais relações do diploma.

### 4. Validação

A pasta `validacao/` registra verificações realizadas sobre os arquivos públicos. Ela inclui relatórios que indicam a leitura dos arquivos, a execução das consultas e a verificação de sanitização dos dados.

## Como interpretar o resultado

O resultado não deve ser entendido como um sistema de produção para emissão ou registro de diplomas. A prova de conceito demonstra a capacidade da ontologia de representar e recuperar relações semânticas do subdomínio do Registro do Diploma.

O uso de dados fictícios permite tornar os artefatos públicos sem expor informações pessoais, acadêmicas ou institucionais reais.
