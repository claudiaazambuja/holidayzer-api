# Holidayzer API
Esta é uma simples API RESTful implementada em Spring Boot para obter informações sobre feriados.

Rotas
1. Obter todos os feriados
Endpoint:

```console
GET /holidays
```

Descrição:
Retorna uma lista de todos os feriados.

Exemplo de Resposta:

```json
{
  "01-01-2024": "Confraternização Mundial",
  "12-02-2024": "Carnaval",
  "13-02-2024": "Carnaval",
  "29-03-2024": "Sexta-feira Santa",
  "21-04-2024": "Tiradentes",
  "01-05-2024": "Dia do Trabalho",
  "30-05-2024": "Corpus Christi",
  "07-09-2024": "Independência do Brasil",
  "12-10-2024": "Nossa Senhora Aparecida",
  "02-11-2024": "Finados",
  "15-11-2024": "Proclamação da República",
  "20-11-2024": "Dia Nacional de Zumbi e da Consciência Negra",
  "25-12-2024": "Natal"
}
```


2. Obter informações sobre um feriado específico
Endpoint:

```console
GET /holidays/{date}
```

Parâmetros:

date (String): A data do feriado no formato dd-MM-yyyy (por exemplo, 01-01-2024).

Descrição:
Retorna informações sobre se a data fornecida é um feriado e, em caso afirmativo, fornece o nome do feriado.

Exemplo de Resposta (Feriado):

```json
{
  "message": "Dia 01-01-2024 é Confraternização Mundial! 🎉"
}
```

Exemplo de Resposta (Não Feriado):

```json
{
  "message": "Dia 05-06-2024 não é feriado 🥲"
}
```