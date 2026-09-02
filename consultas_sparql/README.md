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

As consultas foram preparadas para a ABox pública sanitizada. O CPF de demonstração usado nas consultas 07, 08 e 09 é `CPF-FICTICIO-0012`.
