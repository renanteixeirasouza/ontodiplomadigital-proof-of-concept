# Gráficos

Esta pasta contém representações visuais de apoio à leitura da prova de conceito.

| Arquivo | Função |
|---|---|
| `fluxo_prova_conceito.svg` | Resume o percurso da demonstração: dados tabulares, mapeamento, TBox, ABox, carga no GraphDB, consultas e resultados. |

O grafo visual detalhado do diploma é gerado diretamente no GraphDB pela consulta:

```text
consultas_sparql/09_demo_grafo_diploma_por_cpf.rq
```

Essa escolha evita fixar uma imagem estática como evidência principal e permite ao leitor reproduzir a visualização a partir dos próprios dados RDF.
