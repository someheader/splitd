# Splitdz B

Aplicação web estática para controle de assinaturas compartilhadas, divisão de custos entre pessoas e visualização de balanços mensais.

O projeto foi construído em HTML, CSS e JavaScript puro, com interface baseada em Tailwind via CDN. Não exige backend nem banco de dados para funcionar.

## Visão Geral

O Splitdz B ajuda a:

- cadastrar pessoas participantes
- registrar assinaturas com valor, ciclo, pagador e membros
- calcular automaticamente a divisão por pessoa
- visualizar saldos individuais no dashboard
- acompanhar um cronograma mensal com detalhes por pessoa e por assinatura
- exportar e importar os dados em JSON
- limpar todos os dados e recomeçar do zero

## Funcionalidades

### Home

Página inicial com uma apresentação breve da proposta do sistema.

### Assinaturas

- cadastro de novas assinaturas
- edição e exclusão
- visualização detalhada de cada assinatura
- cálculo automático da cota por participante

### Pessoas

- cadastro de participantes
- remoção de pessoas quando não são pagadoras de assinaturas

### Dashboard

- resumo mensal global
- balanço individual por pessoa
- cronograma mensal com detalhes expansíveis
- acesso direto aos modais de pessoa e assinatura a partir dos cards

### Opções

- importar JSON
- exportar JSON
- remover tudo

## Estrutura de Dados

Os dados são mantidos em memória no navegador e podem ser exportados em JSON. O formato segue esta ideia:

```json
{
  "version": 1,
  "exportedAt": "2026-04-04T12:00:00.000Z",
  "data": {
    "pessoas": [
      { "id": 1, "name": "Maria" }
    ],
    "assinaturas": [
      {
        "id": 1,
        "name": "Netflix",
        "price": 55.9,
        "startDate": "2026-04-01",
        "duration": 0,
        "cycle": "Mensal",
        "payerId": 1,
        "memberIds": [1]
      }
    ]
  }
}
```

## Como Usar

1. Abra o arquivo [index.html](/home/will/projects/Splitd/index.html) em um navegador.
2. Acesse a aba `Pessoas` para cadastrar os participantes.
3. Acesse a aba `Assinaturas` para registrar os serviços.
4. Use o `Dashboard` para acompanhar os saldos e detalhes mensais.
5. Em `Opções`, exporte um backup JSON ou importe dados existentes.

## Arquivos Principais

- [index.html](/home/will/projects/Splitd/index.html): versão principal da aplicação
- [R1/slpitd.html](/home/will/projects/Splitd/R1/slpitd.html): arquivo alternativo / histórico de evolução

## Observações Técnicas

- O projeto usa `Tailwind CSS` por CDN.
- Os dados não persistem automaticamente entre sessões, a menos que sejam exportados e importados manualmente.
- O sistema normaliza os dados importados para manter consistência entre pagador, participantes e cálculos.

## Próximos Passos Sugeridos

- persistência local com `localStorage`
- filtros por período no dashboard
- edição de pessoas
- validações mais avançadas no importador JSON
