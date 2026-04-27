# PartNest B

Aplicação web estática para controle de assinaturas compartilhadas, divisão de custos entre pessoas, acompanhamento de pagamentos e visualização de balanços mensais.

O projeto foi construído em HTML, CSS e JavaScript puro, com interface baseada em Tailwind via CDN. Não exige backend nem banco de dados para funcionar.

## Nota Sobre o Nome

O projeto anteriormente utilizava o nome `Splitdz B`. Esse nome foi substituído por `PartNest B` porque a nomenclatura anterior já era usada em outro contexto comercial.

`PartNest B` é um nome adotado apenas como identidade deste projeto, de forma alusiva e sem finalidade comercial.

## Nota Sobre a Ideia do Projeto

A ideia do projeto veio da necessidade de ter um controle facil de administrar sem precisar vender a alma e entregar todos os dados para um aplicativo que voce vai usar 2 vezes no ano e depois correr o risco de ver tudo vazado aleatoriamente em algum ataque.

Neste modelo em HTML, os dados ficam com você. Não existe troca de dados com a nuvem, nem dependência de um serviço externo para o funcionamento básico da ferramenta.

Ao mesmo tempo, isso traz um custo: pode ser mais dificil administrar os dados, porque tudo fica salvo localmente em JSON, `localStorage` e mecanismos locais do navegador, em vez de existir uma infraestrutura remota cuidando disso para voce.

## Visão Geral

O PartNest B ajuda a:

- cadastrar pessoas participantes
- registrar assinaturas com valor, ciclo, pagador, membros e status ativo/inativo
- acompanhar status de pagamento por participante em cada assinatura
- calcular automaticamente a divisão por pessoa
- visualizar saldos individuais no dashboard
- acompanhar um cronograma mensal com detalhes por pessoa e por assinatura
- compartilhar a visão geral individual como imagem
- exportar e importar os dados em JSON
- limpar todos os dados e recomeçar do zero

## Funcionalidades

### Home

Página inicial em formato de landing page com apresentação da proposta do sistema e indicadores rápidos de funcionamento.

### Sobre

- página institucional com contexto do projeto
- resumo das motivações
- link para o repositório GitHub

### Assinaturas

- cadastro de novas assinaturas
- edição e exclusão
- visualização detalhada de cada assinatura
- cálculo automático da cota por participante
- status ativo/inativo da assinatura
- status `Pago` ou `Pendente` por participante
- assinaturas finalizadas por prazo aparecem como `Finalizada`

### Pessoas

- cadastro de participantes
- edição e remoção de pessoas
- lista com resumo de receber, pagar, assinaturas e pendências
- acesso à visão geral individual

### Dashboard

- resumo global
- resumo anual
- extratos anuais por pessoa
- balanço individual por pessoa com indicadores de saldo
- cronograma mensal com detalhes expansíveis
- acesso direto aos modais de pessoa e assinatura a partir dos cards
- visões gráficas: distribuição mensal, categorias, saldo líquido e projeção de 12 meses

### Perfil Individual

- total a receber
- total a pagar
- assinaturas gerenciadas
- participações em divisões
- status de pagamento por assinatura
- compartilhamento como imagem

### Configurações e Backup

- gerenciamento de categorias (ícones e cores)
- importação e exportação de backups em JSON
- limpeza total de dados locais
- ativação de notificações nativas

## Persistência

O PartNest B funciona em modo local-first:

- os dados ficam salvos localmente no navegador com `localStorage`
- o JSON exportado serve como backup manual e portável
- o sistema avisa quando existem alterações ainda não exportadas
- a importação de um backup não é tratada como alteração pendente

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
        "memberIds": [1],
        "paymentStatus": {
          "1": "paid"
        },
        "enabled": true
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
5. Em `Dashboard`, acompanhe saldos, cronogramas e extratos.
6. Na `Visão Geral Individual`, compartilhe o cartão como imagem quando quiser.
7. Em `Opções`, exporte um backup JSON ou importe dados existentes.

## Arquivos Principais

- [index.html](/home/will/projects/Splitd/index.html): versão principal da aplicação
- [CHANGELOG.md](/home/will/projects/Splitd/CHANGELOG.md): histórico resumido das alterações do projeto
- [README.md](/home/will/projects/Splitd/README.md): visão geral e documentação do projeto

## Observações Técnicas

- O projeto usa `Tailwind CSS` por CDN.
- Os dados persistem localmente no navegador com `localStorage`.
- O export em JSON continua sendo recomendado como backup manual das alterações.
- O sistema normaliza os dados importados para manter consistência entre pagador, participantes e cálculos.
- O status de pagamento por participante também é normalizado e preservado no JSON.
- O compartilhamento da visão individual usa geração local de imagem no navegador.

## Próximos Passos Sugeridos

- filtros por período no dashboard
- validações mais avançadas no importador JSON
- relatórios adicionais por assinatura
- agrupamentos e filtros por status de pagamento
