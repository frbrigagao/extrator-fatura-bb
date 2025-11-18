# Conversor de Fatura BB para CSV

![100% Local](https://img.shields.io/badge/Processamento-100%25%20Local-green)
![Sem Backend](https://img.shields.io/badge/Backend-N%C3%A3o%20Requerido-blue)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-purple)

Aplicação web que converte faturas do Banco do Brasil (Ourocard) em PDF para CSV editáveis, com processamento 100% local e seguro.

## Utilização

**Acesse:** [https://frbrigagao.github.io/extrator-fatura-bb/](https://frbrigagao.github.io/extrator-fatura-bb/)

## Funcionalidades

- **Upload Simples**: Arraste e solte ou clique para selecionar o arquivo PDF
- **Extraçãoo Automática**: Identifica automaticamente os lançamentos da fatura
- **Editor Interativo**: Edite, adicione ou remova transações diretamente na tabela
- **Inversão de Sinais**: Toggle para inverter débitos/créditos conforme necessário
- **Exportação CSV**: Baixe os dados em formato CSV compatível com Excel e Google Sheets
- **Cálculo Automático**: Visualize o total calculado em tempo real
- **100% Privado**: Seus dados permanecem no seu navegador, nada é enviado para servidores

## Segurança e Privacidade

Esta aplicação funciona **inteiramente no seu navegador**. Nenhum dado é enviado para servidores externos:

-  Processamento local usando JavaScript
-  Sem conexões de rede para processar PDFs
-  Seus dados financeiros permanecem privados
-  Funciona offline após o primeiro carregamento

## Como Usar

1. **Abra a aplicação** no seu navegador
2. **Faça upload** do PDF da sua fatura do Banco do Brasil
3. **Aguarde** o processamento automático (alguns segundos)
4. **Edite** os dados conforme necessário na tabela interativa
5. **Inverta sinais** se necessário usando o toggle "Inverter Sinais"
6. **Baixe o CSV** clicando no botão "Baixar CSV"

## Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Arquivo PDF da fatura do Banco do Brasil (Ourocard)
- Conexão com internet apenas para carregar a aplicação (processamento 100% local)

## Formato de Extração

A aplicação identifica lançamentos no seguinte padrão:

```
DD/MM Descrição da Compra R$ Valor
```

**Exemplo:**
```
15/01 PAGAMENTO PIX R$ 150,00-
20/01 COMPRA SUPERMERCADO R$ 250,50
```

### Colunas do CSV Gerado

| Data | Descrição | Moeda | Valor |
|------|-----------|-------|-------|
| DD/MM | Descrição da transação | R$ | Valor numérico |

## Limitações Conhecidas

- Compatível apenas com faturas do Banco do Brasil (Ourocard)
- PDFs com senha não são suportados
- Não foi testada com lançamentos em moeda estrangeira