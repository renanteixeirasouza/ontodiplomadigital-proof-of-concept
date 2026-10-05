# Validação e sanitização

Esta pasta contém relatórios auxiliares da prova de conceito.

| Arquivo | Função |
|---|---|
| `relatorio_sanitizacao.json` | Registra o processo de substituição de dados sensíveis por valores fictícios. |
| `verificacao_pos_sanitizacao.json` | Registra a verificação final de ausência de CPFs/CNPJs válidos, e-mails e nomes pessoais originais nos arquivos públicos. |
| `validacao_local_tbox_abox_publica.json` | Registra a leitura local da TBox e da ABox pública. |
| `validacao_local_consultas_publicas.json` | Registra a execução local das consultas SPARQL públicas. |
| `validacao_graphdb_consulta_federada_dbpedia.json` | Registra a execução da consulta federada demonstrativa no GraphDB, combinando dados locais com DBpedia. |
| `validacao_graphdb_consulta_federada_qlever_wikidata_ibge.json` | Registra a execução da consulta federada demonstrativa no GraphDB, combinando código IBGE local com município e país no Wikidata via QLever. |

Esses relatórios servem como evidências auxiliares. Eles não representam validação externa ou institucional do Diploma Digital Brasileiro.

## Versão atual e histórico

O [lote synthetic de 2026-10-04](synthetic_20261004/README.md) reúne a comparação antes/depois no GraphDB, resultados completos das consultas 01 a 09 e checksums dos arquivos públicos. A comparação dos arquivos públicos sem inferência está em `validacao_local_consultas_publicas_synthetic_20261004.json`. Os relatórios anteriores são históricos; valores com o marcador antigo não pertencem aos dados atuais. As consultas federadas não foram reexecutadas neste lote.
