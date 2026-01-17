# Changelog

Todas as mudanças notáveis neste projeto serão documentadas neste arquivo.

O formato é baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/),
e este projeto adere a [Semantic Versioning](https://semver.org/lang/pt-BR/).

## [Não Lançado]

### Adicionado
- Documentação inicial do projeto

### Corrigido
- Placeholder

### Removido
- Placeholder

---

## [1.0.0] - 2026-01-17

### Adicionado
- Versão inicial do Expert Advisor
- Suporte a múltiplas estratégias de trading
- Análise técnica com indicadores principais (MA, RSI, MACD, Bollinger Bands)
- Gerenciamento automático de risco com Stop Loss e Take Profit
- Trailing Stop dinâmico
- Controle de posições máximas simultâneas
- Logging detalhado de operações
- Compatibilidade com Backtesting
- Parâmetros ajustáveis para otimização
- Restrição de horários de operação
- Suporte para diferentes pares de moedas
- Documentação completa (README, LICENSE, CHANGELOG)
- Arquivo .gitignore para controle de versão
- Guia de contribuição

### Segurança
- Implementação de Stop Loss obrigatório
- Limite de risco por operação
- Validação de parâmetros de entrada
- Proteção contra operações inválidas

---

## Versionamento

As versões seguem o padrão MAJOR.MINOR.PATCH:

- **MAJOR**: Mudanças incompatíveis na API
- **MINOR**: Novas funcionalidades compatíveis
- **PATCH**: Correções de bugs

## Como Relatar Mudanças

Ao enviar um pull request, inclua:

1. **Tipo de mudança**: 
   - `Adicionado` para novas funcionalidades
   - `Corrigido` para correções de bugs
   - `Removido` para funcionalidades removidas
   - `Alterado` para mudanças em funcionalidades existentes
   - `Segurança` para correções de vulnerabilidades

2. **Descrição clara** do que foi feito
3. **Referência** a issues relacionadas
4. **Teste realizado** (demo, backtest, etc)

---

**Data de Última Atualização**: 2026-01-17
