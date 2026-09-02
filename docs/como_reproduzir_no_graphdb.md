# Como reproduzir a prova de conceito no GraphDB

Este roteiro descreve uma forma simples de carregar os arquivos no GraphDB e executar as consultas SPARQL.

## 1. Criar ou selecionar um repositório

No GraphDB, crie um repositório RDF ou selecione um repositório já existente. Na dissertação, o repositório usado na demonstração recebeu o nome `diplomaDB`.

## 2. Carregar a TBox

Carregue primeiro o arquivo:

```text
ontologia/OntoDiplomaDigital_registro_diploma.ttl
```

Esse arquivo contém a estrutura formal da ontologia.

## 3. Carregar a ABox pública

Depois, carregue o arquivo:

```text
ontologia/ontologia_operacional_individuos_ficticios_registro_diploma_publico.ttl
```

Esse arquivo contém as instâncias fictícias usadas na prova de conceito.

## 4. Executar as consultas SPARQL

Abra a área de consultas do GraphDB e execute os arquivos da pasta:

```text
consultas_sparql/
```

Para uma verificação rápida, recomenda-se começar por:

- `08_demo_visao_360_diploma_por_cpf.rq`;
- `09_demo_grafo_diploma_por_cpf.rq`.

## 5. Gerar o grafo visual

Para gerar o grafo visual, use a consulta:

```text
consultas_sparql/09_demo_grafo_diploma_por_cpf.rq
```

No GraphDB, execute essa consulta no modo de visualização gráfica. Ela foi escrita em `CONSTRUCT`, retornando relações RDF entre recursos e rótulos curtos para facilitar a leitura do diagrama.

## Resultado esperado

A consulta 08 deve retornar uma linha consolidando dados fictícios de um diploma, incluindo titular, curso, instituições, registro, assinatura, código de validação e plataforma de acesso.

A consulta 09 deve gerar um grafo visual centrado em um diploma fictício, ligado aos principais recursos relacionados ao Registro do Diploma.

## Limites da reprodução

A reprodução confirma a leitura e consulta dos dados fictícios da prova de conceito. Ela não valida assinaturas criptográficas reais, não consulta plataformas governamentais reais e não testa implantação em ambiente institucional de produção.
