# Changelog

## 2026-04-15

### Inteligência Financeira
- **Economia Gerada**: Nova métrica implementada no Dashboard e na lista de Assinaturas que quantifica o valor total poupado pelo grupo através da divisão estratégica de custos.
- **Simplificação de Dívidas**: Integração de algoritmo de liquidação de saldos (Debt Simplification) para sugerir o menor número possível de transferências entre os membros.

### Dashboard
- **Widget de Sugestões de Acerto**: Adição de um novo componente visual que indica exatamente "quem deve pagar quem" para zerar as pendências do período.
- **Refatoração de KPIs**: Substituição da projeção anual no Dashboard principal pelo indicador de Economia do Grupo, focando no valor economizado pelos usuários.

## 2026-04-14

### UX e Onboarding
- **Tour Interativo**: Implementação de um sistema de "Guided Tour" (passo a passo) no Dashboard para facilitar o primeiro contato do usuário com as métricas e funcionalidades.
- **Central de Ajuda**: Adição de modal explicativo detalhando a lógica matemática por trás dos cálculos de saldo, projeções e pendências, acessível via Dashboard.
- **Sistema de Confirmação**: Padronização de modais de confirmação e alertas para ações críticas (exclusões, limpeza de dados), substituindo os diálogos nativos do navegador por uma interface condizente com o design system.

### Dashboard e Filtros
- **Seletor de Período Customizado**: Implementação de um seletor de mês e ano otimizado (Month Picker) com suporte a navegação por anos e visão anual consolidada.
- **Tags de Filtragem**: Visualização dinâmica de filtros ativos (categoria e período) com botões de remoção rápida.
- **Gráfico Comparativo**: Inclusão de visualização de barras comparando o desempenho financeiro do mês anterior com o mês atual para análise de tendência.

### Gestão e Organização
- **Detalhamento de Categorias**: Nova modal de visão detalhada para categorias, permitindo visualizar a soma de custos ativos e a lista de serviços vinculados.
- **Navegação Cruzada**: Melhoria na transição entre detalhes de assinaturas e perfis individuais de pessoas diretamente pelas listas do Dashboard.
- **Aparência Dinâmica**: Implementação de seletores de cores e ícones (FontAwesome) para pessoas e categorias, permitindo maior personalização visual.

### Manutenção
- **Controle de Versão**: Inclusão da pasta `stitch/` no `.gitignore` para evitar o versionamento de rascunhos de design e arquivos temporários de estilo.

## 2026-04-13

### Interface e Navegação
- **Arquitetura de Navegação**: Implementação de Sidebar fixa para Desktop e Bottom Navigation Bar para Mobile, otimizando o espaço de trabalho em diferentes dispositivos.
- **Refinamento Estético (Design System)**: Aplicação de efeitos de Glassmorphism, desfoque de fundo e sombras em camadas para maior profundidade visual, conforme definido no novo Design System.

### Performance e Offline
- **Otimização de Cache PWA**: Service Worker configurado para realizar o pre-caching de bibliotecas críticas (Tailwind, Chart.js) e fontes, garantindo carregamento rápido e suporte offline inicial.

## 2026-04-12

### Funcionalidades e UI

- **Sistema de Lembretes**: Implementação de notificações nativas para alertar sobre vencimentos em 48h.
- **Consolidação de Dashboard**: Dashboard agora conta com 4 visões gráficas (Distribuição, Projeção, Saldos e Categorias).

## 2026-04-11

### Funcionalidades

- **Gestão de Categorias**: Implementação de aba de Configurações para gerenciar categorias de assinaturas e vincular serviços a temas específicos.

## 2026-04-10

### Mobile e PWA

- **Suporte a PWA**: Implementação de `manifest.json` e `sw.js` para permitir a instalação da aplicação como um aplicativo nativo no celular e funcionamento offline.

## 2026-04-09

### Gráficos e Visualização

- **Saldo Líquido**: Implementação de gráfico de barras horizontais no Dashboard para comparação imediata do equilíbrio financeiro entre todos os participantes.

## 2026-04-08

### Funcionalidades

- **Busca de Assinaturas**: Inclusão de filtro de pesquisa na lista de assinaturas para localização rápida por nome.

## 2026-04-07

### UX e Gráficos

- **Tooltips Inteligentes**: Adição de tooltips personalizados nos gráficos do Dashboard.
- **Detalhamento**: O gráfico de rosca agora exibe tanto o valor total da assinatura quanto o valor da cota por pessoa ao passar o mouse.

## 2026-04-06

### Gráficos e Visualização

- **Análise Visual**: Inclusão de gráficos interativos no Dashboard utilizando Chart.js.
- **Distribuição de Gastos**: Gráfico de rosca (Donut) mostrando a proporção de custo por assinatura no mês atual.
- **Projeção Mensal**: Gráfico de barras exibindo a previsão de gastos totais para os próximos 12 meses.
- **Suporte a Temas**: Gráficos ajustam cores de eixos e textos automaticamente entre Modo Claro e Escuro.

## 2026-04-05

### Interface

- **Modo Escuro**: Implementação de botão alternador (toggle) no cabeçalho com persistência no `localStorage`.
- **Refinamento Visual**: Adição de classes `dark:` em cards, modais e tabelas para suporte completo ao tema escuro.
- **Correção de Contraste**: Ajuste nos fundos de modais e elementos dinâmicos para evitar que se misturem ao fundo no modo escuro.

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

## Recursos Futuros (Planejamento)

### Funcionalidades em estudo

- **Categorização**: Tags para agrupar assinaturas (Streaming, Casa, Trabalho).
- **Gráficos e Visualização**: Gráficos de rosca para distribuição de gastos e barras para histórico mensal.
- **Suporte Multi-moeda**: Conversão manual de valores em USD/EUR para BRL.
- **Mobile**: Transformação em PWA para instalação como aplicativo no celular.
- **Pesquisa e Filtros**: Busca rápida na lista de pessoas (assinaturas já implementadas).
- **Notificações Locais**: Lembretes de vencimento baseados na data de início e ciclo.
