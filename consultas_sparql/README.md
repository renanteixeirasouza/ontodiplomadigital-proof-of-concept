# Consultas SPARQL

Esta pasta contém as consultas usadas para verificar a OntoDiplomaDigital na prova de conceito.

| Arquivo | Finalidade |
|---|---|
| `01_qc1_instituicoes_emissao_registro.rq` | Recupera instituições emissoras e registradoras relacionadas a diplomas digitais. |
| `02_qc2_autenticidade_assinatura_registro_validacao.rq` | Recupera elementos associados a registro, assinatura, carimbo de tempo e código de validação. |
| `03_qc3_diplomas_ies_periodo_modalidade.rq` | Consulta diplomas por instituição, período e modalidade de oferta. |
| `04_qc4_diplomado_curso_concluido.rq` | Recupera titular, curso concluído, grau e título conferidos. |
| `05_qc5_valores_controlados.rq` | Lista valores controlados representados na ontologia. |
| `06_qc6_proveniencia_registro.rq` | Recupera dados de proveniência do registro. |
| `07_qc7_acesso_por_cpf_plataforma.rq` | Demonstra a recuperação de plataforma de acesso associada a um CPF fictício. |
| `08_demo_visao_360_diploma_por_cpf.rq` | Consolida uma visão tabular de um diploma fictício a partir de CPF. |
| `09_demo_grafo_diploma_por_cpf.rq` | Gera um grafo visual das principais relações de um diploma fictício. |
| `10_demo_consulta_federada_dbpedia_brasil.rq` | Demonstra consulta federada com `SERVICE`, combinando dados locais fictícios com dados externos da DBpedia sobre o Brasil. |
| `11_demo_consulta_federada_qlever_wikidata_municipio_ibge.rq` | Demonstra consulta federada com `SERVICE`, combinando código IBGE de naturalidade presente no `diplomaDB` com município e país recuperados no Wikidata via QLever. |

As consultas foram preparadas para a ABox pública sanitizada. O CPF de demonstração usado nas consultas 07, 08, 09 e 10 é `CPF-FICTICIO-0012`. A consulta 11 utiliza o código IBGE `3550308`, correspondente ao município de São Paulo na fonte externa consultada.

As consultas federadas dependem da disponibilidade dos endpoints públicos utilizados. Elas não representam integração real com sistemas do MEC, e-MEC, IBGE ou Gov.br.
