# Case Técnico PicPay

## Input
O [python notebook](manipulacao-de-dados.ipynb) criado nesse projeto lê um dataset em formato CSV com registros de transações financeiras, contendo os seguintes atributos:

| Campo                   | Descrição                                                                                                            |
|-------------------------|----------------------------------------------------------------------------------------------------------------------|
| transaction_id          | Identificador único da transação                                                                                   |
| transaction_date        | Data da transação                                                                                                   |
| transaction_type        | Produto utilizado para realizar a transação                                                                         |
| transaction_value       | Valor original da transação, sem aplicação de taxa                                                                  |
| receiver_used_cc_limit  | Valor recebido via P2P no cartão de crédito no mês para o usuário recebedor da transação                           |
| payment_method          | Método de pagamento                                                                                                 |
| installments            | Quantidade de parcelas no cartão de crédito                                                                         |
| p2p_surcharge_rate      | Taxa adicional para transações P2P quando o recebedor excedeu o limite de R$800 recebido com o produto P2P cartão de crédito |
| bills_surcharge_rate    | Taxa adicional para transações BILLS quando o usuário realiza o pagamento de um boleto utilizando o cartão de crédito |
| installment_rate        | Taxa mensal de juros por parcelamento                                                                               |

## Processamento
As etapas aplicadas nesse projeto forem de:
1. Importação e inspeção dos dados
2. Cálculos do dataset "transactions"
3. Criação do dataset "transactions_installments"
4. Criação e exportação dos arquivos finais em CSV

## Output
O resultado final foram dois datasets em CSV contendo as informações completas de cada transação ([transactions_complete](transactions_complete.csv)) e com informações referentes a cada parcela em transações com parcelamento ([transactions_installments](transactions_installments.csv)), respeitando o ID da transação previamente definido.

O dicionário de dados completo para os datasets criados pode ser conferido [aqui](material_de_apoio/Dicionario.xlsx).

## Requisitos
- Python 3.12+: Linguagem usada para análise e manipulação de dados.
- Pandas 2.2.0+: Manipulação de tabelas e dados estruturados.
- NumPy 1.26.3+: Operações matemáticas e com arrays.
- os: Acesso a funcionalidades do sistema operacional.