# Leitor de Extratos Bancários

Aplicação desktop em Python para extrair informações de extratos bancários em PDF e exportar os resultados para Excel.

## Funcionalidades

- Interface única com seleção da pasta raiz.
- Botões independentes: `Processar Correntes` e `Processar Aplicações`.
- Barra de progresso e acompanhamento dos arquivos.
- Abertura da planilha após o processamento.
- Registro de falhas na aba `Erros de leitura`.
- Temas claro e escuro.

## Bancos e modelos suportados

### Contas correntes

Caixa Econômica Federal, Banco do Brasil, Banco ABC, Itaú, Sicredi, XP, Bradesco e Safra.

Informações exportadas: arquivo, cliente, banco, conta, conta formatada, data do extrato e saldo.

### Aplicações

| Banco | Modelos |
|---|---|
| Caixa Econômica Federal | Extrato padrão de aplicações |
| Banco do Brasil | Fundos mensal e Resumo do mês |
| Bradesco | Extrato de investimentos com blocos Total |
| Sicredi | Poupança e Depósito a Prazo |
| XP | Resumo de investimentos |
| Itaú | Aplicações padrão e Fundos de Investimento |
| Safra | Investimentos — Resumo Composição |

Informações exportadas: arquivo, cliente, banco, conta, mês, saldo anterior, aplicações, resgates, rendimento bruto, IRRF, IOF, saldo bruto e conferência (`Check`).

## Organização das pastas

Selecione a pasta raiz que contém as pastas dos bancos:

```text
Extratos/
├── 001. Caixa Econômica/
│   ├── 001. Conta Corrente/
│   └── Aplicação/
├── BB/
│   ├── Corrente/
│   └── Aplicação/
├── Itau/
│   ├── Corrente/
│   └── Aplicação/
└── Outros bancos/
    ├── Corrente/
    └── Aplicação/
```

## Como usar

1. Abra o programa.
2. Selecione a pasta raiz dos extratos.
3. Clique em `Processar Correntes` ou `Processar Aplicações`.
4. Confira a planilha gerada e a aba de erros.

Arquivos de saída:

- `extratos_corrente.xlsx`
- `extratos_aplicacao.xlsx`

## Tecnologias

Python, CustomTkinter, PyMuPDF, OpenPyXL e Pillow.

## Limitações

O leitor reconhece os layouts já mapeados no código, não todos os modelos disponíveis de cada banco. PDFs sem texto extraível precisam de OCR, que não está integrado à versão atual.

## Uso

**Uso interno e licenciado. Distribuição proibida.**
