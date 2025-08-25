# Projeto_DIO_Criando_um_Sistema_Bancario_com_Python
Projeto prático 'Criando um Sistema Bancário com Python' do curso 'Suzano - Python Developer #2' na DIO. 

O código inicial fornecido já continha uma boa estrutura para o sistema. As implementações a seguir garantem que todas as regras de negócio descritas sejam atendidas:

Depósito: A lógica para aceitar apenas valores positivos já estava presente e correta. Os depósitos são adicionados ao saldo e registrados na variável extrato.

Saque: A implementação verifica três condições antes de permitir o saque:

Saldo suficiente: valor > saldo

Limite por saque: valor > limite (onde limite é R$ 500,00)

Limite diário de saques: numero_saques >= LIMITE_SAQUES (onde LIMITE_SAQUES é 3)

Se qualquer uma dessas condições for verdadeira, a operação falha e uma mensagem específica de erro é exibida. Caso contrário, o valor é subtraído do saldo e a transação é registrada no extrato.

Extrato: A operação de extrato exibe todas as transações (depósitos e saques) registradas. No final, o saldo atual da conta é mostrado, formatado corretamente como "R$ xxx.xx". Foi adicionada a lógica para exibir "Não foram realizadas movimentações." caso a variável extrato esteja vazia.

Todo código foi criado com ajuda de IA.
