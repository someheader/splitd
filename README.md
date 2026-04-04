# PartNest B

Aplicação web estática para controle de assinaturas compartilhadas, divisão de custos entre pessoas e visualização de balanços mensais.

O projeto foi construído em HTML, CSS e JavaScript puro, com interface baseada em Tailwind via CDN. Não exige backend nem banco de dados para funcionar.

## Nota Sobre o Nome

O projeto anteriormente utilizava o nome `Splitdz B`. Esse nome foi substituído por `PartNest B` porque a nomenclatura anterior já era usada em outro contexto comercial.

`PartNest B` é um nome adotado apenas como identidade deste projeto, de forma alusiva e sem finalidade comercial.

## Nota Sobre a Ideia do Projeto

A ideia do projeto veio da necessidade de ter um controle facil de administrar sem precisar vender a alma e entregar todos os dados para um aplicativo que voce vai usar 2 vezes no ano e depois correr o risco de ver tudo vazado aleatoriamente em algum ataque.

Neste modelo em HTML, os dados ficam com voce. Nao existe troca de dados com a nuvem, nem dependencia de um servico externo para o funcionamento basico da ferramenta.

Ao mesmo tempo, isso traz um custo: pode ser mais dificil administrar os dados, porque tudo fica salvo localmente em JSON, `localStorage` e mecanismos locais do navegador, em vez de existir uma infraestrutura remota cuidando disso para voce.

## Visão Geral

O PartNest B ajuda a:

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

- resumo global
- extratos anuais por pessoa
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

## Observações Técnicas

- O projeto usa `Tailwind CSS` por CDN.
- Os dados persistem localmente no navegador com `localStorage`.
- O export em JSON continua sendo recomendado como backup manual das alterações.
- O sistema normaliza os dados importados para manter consistência entre pagador, participantes e cálculos.

## Próximos Passos Sugeridos

- persistência local com `localStorage`
- filtros por período no dashboard
- edição de pessoas
- validações mais avançadas no importador JSON
