# Indicador de Produtividade

Dashboard HTML da Berzerk para a máquina **TAG 2**, equipe **Elias e Rafael**.

Site: https://eliasnrodrigues.github.io/indicador-produtividade/

Abra `index.html` diretamente; sem dependências ou compilação.

## Funcionalidades

- Meta de **5.000 peças passadas por dia**, compartilhada pela equipe da máquina.
- Visões diária, semanal, mensal e intervalo personalizado. Produtividade = peças no período / (5.000 × dias planejados) × 100. Ajuste os dias planejados para descontar folgas. O valor inicial é a duração em dias corridos.
- Seletor suspenso com marcação múltipla de responsáveis: nenhuma seleção mostra geral; apenas Elias ou Rafael mostra registros individuais; ambos mostram registros conjuntos. Não há divisão fictícia da produção. Os registros originais são associados à equipe, com responsável editável na tabela.
- Data por registro e atribuição em lote a linhas filtradas sem data. Não foram inventadas datas a partir das anotações ambíguas.
- Filtros por lote, tamanho, cor e conferência; gráficos e exportação CSV.
- Indicadores de defeitos e taxa de defeitos. Anotações `/ N` de até 20 significam defeitos. Sem anotação = não informado, nunca zero presumido.
- Taxa calculada somente sobre registros com quantidade e defeitos informados. O total de defeitos inclui anotações em linhas cuja quantidade está pendente; essas linhas não entram na taxa. A meta considera peças passadas incluindo defeitos.
- Códigos provisórios de quatro dígitos para lotes ilegíveis, identificados explicitamente como gerados.

## Dados e persistência

Transcrição parcial de duas fotos. Com a interpretação de defeitos informada pelo usuário, a base inicial tem 11.740 peças legíveis, 36 defeitos anotados e 7 registros com quantidade a conferir. A taxa inicial de 1,14% usa 33 defeitos em 2.883 peças nos mesmos registros; não representa a taxa de toda a produção.

Datas ainda precisam ser preenchidas para calcular períodos. As alterações em quantidades, defeitos, datas e responsáveis são salvas apenas neste navegador (localStorage), sem sincronização com GitHub ou outros dispositivos. O CSV inclui esses campos.

O filtro de responsáveis afeta todo o painel. A área de metas usa todos os lotes e cores dentro do período; os demais filtros afetam os totais gerais, a área de qualidade e a tabela.

Logo oficial pendente: o cabeçalho usa identificação tipográfica provisória.

Hospedagem: GitHub Pages, branch `main`, pasta raiz.
