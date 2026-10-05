# Lote synthetic — 2026-10-04

Este lote substitui o marcador `fake` por `synthetic` nos identificadores dos dados sintéticos e atualiza as consultas 01, 02 e 04. Exemplos atuais: `urn:synthetic:diploma:001` e `PROC-SYNTHETIC-2027-0001`. As classes, propriedades, recursos RDF e quantidades da base foram preservados. A ABox pública mantém 25.553 triplas.

## Evidências atuais

- `../validacao_local_consultas_publicas_synthetic_20261004.json`: comparação das consultas públicas com RDFLib, sem inferência. As consultas 01 a 08 mantiveram respostas equivalentes após a troca do marcador; a consulta 09 excedeu o tempo de execução nesse ambiente e não foi validada por esse relatório.
- `comparacao_graphdb.json`: comparação antes/depois no repositório de demonstração `diplomaDB`, com o regime de inferência padrão do servidor. As consultas 01 a 08 retornaram, respectivamente, 2, 1, 1, 1, 20, 303, 1 e 1 linhas. A consulta 09 produziu 37 triplas antes e depois. Os arquivos `*_resultado.json` e `*_resultado.ttl` preservam as respostas completas dessa execução.
- `checksums_sha256.txt`: identifica os arquivos públicos de dados, ontologia e consultas integrantes deste lote.

A comparação no GraphDB usa o próprio estado anterior do repositório como referência. Ele contém 28.562 triplas explícitas (TBox e ABox). Há diferenças de representação anteriores à migração em 252 valores de `workloadHours` e 24 valores de `skos:notation`, em relação aos arquivos públicos; elas foram preservadas e estão registradas no relatório. Portanto, os resultados do GraphDB documentam esse ambiente de demonstração e não garantem equivalência literal com uma carga nova dos arquivos públicos. A comparação com RDFLib verifica separadamente os arquivos públicos.

As consultas federadas 10 e 11 não foram reexecutadas neste lote. Seus relatórios anteriores permanecem como evidências históricas, dependentes dos serviços externos e da data de execução. Os relatórios anteriores à migração, inclusive `validacao_local_consultas_publicas.json`, também são históricos e podem conter o marcador antigo. Não devem ser usados como resultados da versão atual.

## Reprodução

Use os arquivos atuais de `ontologia/`, `dados/` e `consultas_sparql/`. Em uma carga nova, importe TBox e ABox em um repositório vazio; não acrescente a ABox nova à base antiga, pois os valores anteriores poderiam permanecer. Consulte `../../docs/como_reproduzir_no_graphdb.md`. Os resultados limitam-se à prova de conceito com dados sintéticos; não representam validação institucional ou criptográfica.
