# Changelog

## 2026-04-04

### Estrutura e identidade

- Renomeação da identidade visual para `PartNest B`.
- Atualização do título da aplicação, marca no cabeçalho, rodapé e documentação.
- Inclusão da página `Sobre` com conteúdo alinhado ao `README.md`.
- Ajuste do rodapé com links para `Sobre` e repositório GitHub.

### Navegação e layout

- Criação da página inicial `Home` em formato de landing page.
- Clique na marca do cabeçalho passando a levar para `Home`.
- Reorganização do cabeçalho para uma linha mais compacta.
- Inclusão de navegação responsiva com dropdown quando o menu não cabe inteiro.
- Inclusão de botão de `Opções` com estado ativo visual.
- Centralização visual do footer.

### Assinaturas

- Cadastro e edição de assinaturas com:
  - nome do serviço
  - valor
  - data de início
  - prazo
  - ciclo
  - pagador
  - participantes
  - status ativo/inativo via checkbox
- Regra para assinaturas inativas não entrarem nos saldos.
- Regra para assinaturas com prazo encerrado aparecerem como `Finalizada`.
- Detalhe da assinatura com clique fora para fechar.
- Ajustes de layout do card de detalhe para mobile.
- Ações de editar e excluir reorganizadas no rodapé do card.

### Pessoas

- Cadastro e edição de pessoas.
- Lista de pessoas enriquecida com:
  - total a receber
  - total a pagar
  - quantidade de assinaturas
  - quantidade gerenciada
  - indicador de pendências
- Cards de pessoas abrindo a `Visão Geral Individual`.

### Dashboard

- Renomeação de `Resumo Mensal Global` para `Resumo Global`.
- Inclusão de `Resumo Anual`.
- Criação da subpágina `Extratos`.
- Matriz anual por pessoa com totais de receber, pagar, saldo e quantidade de assinaturas.
- Cards e listas do dashboard com navegação cruzada entre pessoas e assinaturas.
- Inclusão de status de pendências nas visões do dashboard.

### Pagamentos por participante

- Inclusão do controle de status `Pago` e `Pendente` por participante em cada assinatura.
- Pagador fixado automaticamente como `Pago`.
- Controle desse status dentro da `Divisão de Pagamentos` no detalhe da assinatura.
- Persistência desse status em `localStorage` e no JSON exportado/importado.
- Saldos e totais ajustados para considerar apenas valores ainda pendentes.

### Persistência e backup

- Persistência local automática com `localStorage`.
- Exportação e importação em JSON.
- Sugestão visual de exportação quando há alterações ainda não exportadas.
- Aviso do navegador antes de sair da página com alterações não exportadas.
- Correção para que importar JSON não seja tratado como alteração pendente.
- Feedback de importação bem-sucedida com ícone verde de sucesso.
- Ação `Remover Tudo` para reiniciar o estado local.

### Compartilhamento

- Inclusão de compartilhamento da `Visão Geral Individual`.
- Geração de uma imagem limpa do card, sem botões de ação.
- Uso do compartilhamento nativo quando disponível.
- Fallback para download da imagem quando o compartilhamento nativo não existe.

### UX e consistência visual

- Modais e cards ajustados para:
  - header e footer compactos
  - corpo rolável
  - melhor uso em telas pequenas
- Revisões em botões, bordas, contrastes e fundos.
- Ajustes em feedback visual de menus ativos.

### Organização do projeto

- Criação de `.gitignore` ignorando apenas `.codex`.
- Atualização contínua do `README.md` para refletir a estrutura atual.

