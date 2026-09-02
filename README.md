# OntoDiplomaDigital — Prova de Conceito

Este repositório reúne os artefatos públicos da prova de conceito da **OntoDiplomaDigital**, ontologia operacional desenvolvida na dissertação de mestrado para representar semanticamente o subdomínio do Registro do Diploma Digital de Instituições de Ensino Superior brasileiras.

O objetivo deste material é permitir que o leitor consulte, inspecione e reproduza parcialmente a demonstração operacional apresentada na dissertação. Os arquivos aqui disponibilizados mostram como dados tabulares fictícios foram representados em RDF, carregados com a TBox da ontologia e consultados por meio de SPARQL.

## Para começar

Se você não tem familiaridade com ontologias, RDF ou SPARQL, comece por:

1. [Guia para leitura do repositório](docs/guia_para_leitores.md)
2. [Fluxo da prova de conceito](graficos/fluxo_prova_conceito.svg)
3. [Consulta 08 — visão 360 do diploma por CPF](consultas_sparql/08_demo_visao_360_diploma_por_cpf.rq)
4. [Consulta 09 — grafo visual do diploma por CPF](consultas_sparql/09_demo_grafo_diploma_por_cpf.rq)

## Estrutura do repositório

```text
.
├── README.md
├── ontologia/
│   ├── OntoDiplomaDigital_registro_diploma.ttl
│   └── ontologia_operacional_individuos_ficticios_registro_diploma_publico.ttl
├── dados/
│   ├── dados_diplomas_pratica_mapeamento_publico.csv
│   ├── ontologia_operacional_individuos_ficticios_registro_diploma_amigavel_publico.csv
│   ├── ontologia_operacional_individuos_ficticios_registro_diploma_wide_publico.csv
│   └── tabela_individuos_registro_diploma_publico.csv
├── fontes_oficiais_mec/
│   ├── README.md
│   ├── checksums_sha256.txt
│   └── xsd_v1_05/
│       └── arquivos XSD oficiais do Diploma Digital Brasileiro
├── consultas_sparql/
│   ├── 01_qc1_instituicoes_emissao_registro.rq
│   ├── 02_qc2_autenticidade_assinatura_registro_validacao.rq
│   ├── 03_qc3_diplomas_ies_periodo_modalidade.rq
│   ├── 04_qc4_diplomado_curso_concluido.rq
│   ├── 05_qc5_valores_controlados.rq
│   ├── 06_qc6_proveniencia_registro.rq
│   ├── 07_qc7_acesso_por_cpf_plataforma.rq
│   ├── 08_demo_visao_360_diploma_por_cpf.rq
│   ├── 09_demo_grafo_diploma_por_cpf.rq
│   ├── 10_demo_consulta_federada_dbpedia_brasil.rq
│   └── 11_demo_consulta_federada_qlever_wikidata_municipio_ibge.rq
├── graficos/
│   └── fluxo_prova_conceito.svg
├── graficos_dissertacao/
│   ├── README.md
│   ├── indice_graficos.md
│   ├── manifesto_imagens_extraidas.csv
│   ├── preview_imagens_extraidas.jpg
│   └── imagens_extraidas_docx/
├── validacao/
│   ├── relatorio_sanitizacao.json
│   ├── verificacao_pos_sanitizacao.json
│   ├── validacao_local_tbox_abox_publica.json
│   └── validacao_local_consultas_publicas.json
└── docs/
    ├── guia_para_leitores.md
    ├── como_reproduzir_no_graphdb.md
    └── texto_apendice_dissertacao.md
```

## O que cada pasta contém

| Pasta | Função |
|---|---|
| `ontologia/` | Arquivos Turtle da ontologia: TBox e ABox pública fictícia. |
| `dados/` | Arquivos tabulares usados como base da demonstração e versões auxiliares para inspeção. |
| `fontes_oficiais_mec/` | Cópias dos schemas XSD v1.05 do Ministério da Educação utilizados como fontes técnicas da modelagem. |
| `consultas_sparql/` | Consultas SPARQL ligadas às questões de competência e às demonstrações visuais. |
| `graficos/` | Representações visuais de apoio à leitura da prova de conceito. |
| `graficos_dissertacao/` | Imagens e diagramas extraídos do documento canônico da dissertação para consulta e rastreabilidade. |
| `validacao/` | Relatórios de verificação da sanitização, leitura dos arquivos e execução das consultas. |
| `docs/` | Documentação explicativa para leitores, banca e interessados em reproduzir a demonstração. |

## Dados fictícios e limites da prova de conceito

Os dados deste repositório são **fictícios e sanitizados**. CPFs, CNPJs, nomes pessoais, códigos de validação e registros acadêmicos foram substituídos por valores artificiais, como `CPF-FICTICIO-0012`, `Pessoa Fictícia-0012` e `CODIGO-VALIDACAO-FICTICIO-0006`.

Este repositório não contém dados reais de estudantes, instituições, diplomas ou processos acadêmicos. A prova de conceito também não realiza validação criptográfica de assinaturas digitais, não consulta sistemas governamentais reais e não demonstra implantação institucional em produção.

## Resultado demonstrado

A prova de conceito demonstra que a OntoDiplomaDigital permite:

- representar diplomas, diplomados, cursos, instituições, registros, assinaturas e mecanismos de validação como recursos RDF;
- recuperar informações por consultas SPARQL;
- relacionar o diploma ao titular, curso, instituições emissora e registradora, registro, assinatura, carimbo de tempo, código de validação e plataforma de acesso;
- visualizar uma parte do grafo de conhecimento gerado a partir de um CPF fictício.
- executar uma consulta federada demonstrativa, combinando dados locais fictícios com uma fonte externa de dados ligados.

## Consulta federada

A consulta `10_demo_consulta_federada_dbpedia_brasil.rq` usa `SERVICE` para combinar dados locais da ABox pública com dados externos da DBpedia sobre o recurso `Brazil`. A consulta `11_demo_consulta_federada_qlever_wikidata_municipio_ibge.rq` usa `SERVICE` para combinar a contagem local de diplomados fictícios por código IBGE de naturalidade com dados externos do Wikidata, consultados por meio do QLever. As duas consultas têm finalidade demonstrativa e dependem da disponibilidade dos endpoints externos. Não se trata de integração real com sistemas do MEC, e-MEC, IBGE ou Gov.br.

## Licença

Salvo indicação em contrário, os artefatos autorais deste repositório são disponibilizados sob a licença [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE.md).

Os arquivos XSD preservados em `fontes_oficiais_mec/` são fontes oficiais externas do Ministério da Educação e foram incluídos apenas para fins de rastreabilidade acadêmica.

## Referência acadêmica

Este repositório acompanha a dissertação de mestrado sobre a OntoDiplomaDigital. Na dissertação, ele deve ser citado como apêndice técnico da prova de conceito.

Consulte também: [texto sugerido para o apêndice](docs/texto_apendice_dissertacao.md).
