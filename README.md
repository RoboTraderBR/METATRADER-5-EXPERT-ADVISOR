# MetaTrader 5 Expert Advisor

Um robô de trading automatizado desenvolvido para a plataforma MetaTrader 5, implementando estratégias de negociação algorítmica com análise técnica avançada.

## 📋 Sumário

- [Visão Geral](#visão-geral)
- [Funcionalidades](#funcionalidades)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Configuração](#configuração)
- [Uso](#uso)
- [Gerenciamento de Risco](#gerenciamento-de-risco)
- [Troubleshooting](#troubleshooting)
- [Contribuição](#contribuição)
- [Licença](#licença)

## 🎯 Visão Geral

Este Expert Advisor (EA) é um sistema de trading automatizado que executa operações no mercado cambial e de commodities baseado em sinais técnicos e análise de mercado. O EA foi desenvolvido em MQL5 e oferece múltiplas estratégias de negociação com gerenciamento automático de risco.

## ✨ Funcionalidades

- **Múltiplas Estratégias**: Implementação de diferentes estratégias de trading
- **Análise Técnica**: Uso de indicadores técnicos como Moving Average, RSI, MACD, Bollinger Bands
- **Gerenciamento de Risco**: Stop Loss e Take Profit automáticos
- **Trailing Stop**: Acompanhamento dinâmico de lucros
- **Controle de Posição**: Limite de operações simultâneas e lotes
- **Logging Detalhado**: Registro completo de operações e sinais
- **Backtesting**: Compatível com Strategy Tester do MetaTrader 5
- **Otimização**: Parâmetros ajustáveis para diferentes pares e timeframes

## 🔧 Requisitos

- **MetaTrader 5** (versão 5.0 ou superior)
- Conhecimento básico de trading e análise técnica
- Conta demo ou real com broker compatível
- Conexão com internet estável

## 📥 Instalação

### Passo 1: Preparar o Arquivo

1. Copie o arquivo `.mq5` do Expert Advisor
2. Cole na pasta de Experts do MetaTrader 5:
   - Windows: `C:\Users\[User]\AppData\Roaming\MetaQuotes\Terminal\[Account]\MQL5\Experts\`
   - macOS: `~/Library/Application Support/MetaQuotes/Terminal/[Account]/MQL5/Experts/`
   - Linux: `~/.wine/drive_c/users/[User]/AppData/Roaming/MetaQuotes/Terminal/[Account]/MQL5/Experts/`

### Passo 2: Compilar

1. Abra o MetaEditor (F4 no MetaTrader 5)
2. Navegue até o arquivo do EA
3. Clique em Compilar (ou pressione F5)
4. Verifique se não há erros

### Passo 3: Ativar no Chart

1. Abra um chart no MetaTrader 5
2. Arraste o EA compilado para o chart
3. Configure os parâmetros (veja seção Configuração)
4. Clique em OK

## ⚙️ Configuração

### Parâmetros Principais

```
Gerais:
- MagicNumber: Identificador único para as ordens (padrão: 123456)
- Comentário: Descrição das ordens (padrão: "Expert Advisor")

Volume da Posição:
- TamanhoLote: Tamanho fixo de lote (padrão: 0.1)
- ControleRiscoPercentual: Percentual de risco do capital (padrão: 2%)

Gerenciamento de Risco:
- StopLossPips: Stop Loss em pontos (padrão: 50)
- TakeProfitPips: Take Profit em pontos (padrão: 100)
- TrailingStopPips: Trailing Stop em pontos (padrão: 0 - desativado)

Indicadores Técnicos:
- PeriodoMA: Período da Média Móvel (padrão: 20)
- PeriodoRSI: Período do RSI (padrão: 14)
- PeriodoMACD: Período do MACD (padrão: 12,26,9)

Controle:
- MaxPosicoes: Número máximo de posições abertas (padrão: 1)
- TempoOperacaInicio: Hora de início (padrão: 09:00)
- TempoOperacaoFim: Hora de término (padrão: 17:00)
- ApenasSegundaAVeneca: Operar apenas segunda a sexta (padrão: true)
```

## 🚀 Uso

### Modo Demo (Recomendado)

1. Use uma conta demo para testar antes de usar dinheiro real
2. Teste em diferentes pares e timeframes
3. Acompanhe os resultados por pelo menos 2-4 semanas

### Backtesting

1. Abra o Strategy Tester (Ctrl+R)
2. Selecione o EA
3. Configure o período de teste
4. Clique em Start
5. Analise os resultados (Drawdown, Win Rate, Fator de Lucro)

### Modo Ao Vivo

1. **Inicie pequeno**: Use lotes pequenos inicialmente
2. **Monitore regularmente**: Acompanhe o performance do EA
3. **Ajuste conforme necessário**: Modifique parâmetros se necessário
4. **Backup**: Mantenha backup dos logs e resultados

## ️ Gerenciamento de Risco

### Boas Práticas Implementadas

- **Stop Loss Obrigatório**: Toda operação possui stop loss
- **Take Profit**: Retirada de lucros predefinida
- **Trailing Stop**: Proteção dinâmica de ganhos
- **Limite de Posições**: Máximo de operações simultâneas
- **Drawdown Máximo**: Parada automática após perda limite
- **Horário de Operação**: Restrição a horários específicos

### Cálculo do Lote com Risco

```
Lote = (Capital × Risco%) / (Stop Loss × Valor do Ponto)
```

## 🔍 Troubleshooting

### Problema: EA não está abrindo operações
- Verifique se o EA está ativado (botão de play azul)
- Confirme os parâmetros de entrada
- Verifique os sinais de trading (logs)
- Confirme que não há limite de posições atingido

### Problema: Erro "Conexão Recusada"
- Verifique a conexão com internet
- Reinicie o MetaTrader 5
- Verifique as credenciais da conta

### Problema: Drawdown alto
- Reduza o tamanho do lote
- Aumente o Stop Loss
- Implemente filtros adicionais de entrada
- Reduza a frequência de operações

### Problema: EA congelado
- Reinicie o MetaTrader 5
- Recompile o EA
- Verifique se há erro no código dos logs

## 🤝 Contribuição

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

## ⚠️ Aviso Legal

**IMPORTANTE**: Trading com robôs envolve risco financeiro significativo. 

- Este EA é fornecido "como está" sem garantias
- Não há garantias de lucro
- Perdas são possíveis
- Sempre use modo demo antes de real
- Comece com capital pequeno
- Monitore regularmente as operações
- Consulte um consultor financeiro se necessário

**Disclaimer**: O autor não se responsabiliza por perdas decorrentes do uso deste EA.

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo LICENSE para detalhes.

---

**Desenvolvido com ❤️ por Adriano Borba**

Para dúvidas ou sugestões, abra uma Issue no repositório.
