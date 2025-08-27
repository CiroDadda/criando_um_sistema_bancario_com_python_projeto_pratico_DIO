# Criando um Sistema Bancário com Python - Projeto Prático DIO
Projeto prático 'Criando um Sistema Bancário com Python' do curso 'Suzano - Python Developer #2' na DIO. 

# Versão 1
O código inicial fornecido já continha uma boa estrutura para o sistema. As implementações a seguir garantem que todas as regras de negócio descritas sejam atendidas:

Depósito: A lógica para aceitar apenas valores positivos já estava presente e correta. Os depósitos são adicionados ao saldo e registrados na variável extrato.

Saque: A implementação verifica três condições antes de permitir o saque:

Saldo suficiente: valor > saldo

Limite por saque: valor > limite (onde limite é R$ 500,00)

Limite diário de saques: numero_saques >= LIMITE_SAQUES (onde LIMITE_SAQUES é 3)

Se qualquer uma dessas condições for verdadeira, a operação falha e uma mensagem específica de erro é exibida. Caso contrário, o valor é subtraído do saldo e a transação é registrada no extrato.

Extrato: A operação de extrato exibe todas as transações (depósitos e saques) registradas. No final, o saldo atual da conta é mostrado, formatado corretamente como "R$ xxx.xx". Foi adicionada a lógica para exibir "Não foram realizadas movimentações." caso a variável extrato esteja vazia.

# Versão 2

Principais Mudanças e Melhorias:
1. Modularização: Todo o código foi reorganizado em funções, cada uma com uma responsabilidade única (depositar, sacar, criar_usuario, etc.), tornando o sistema mais fácil de ler e dar manutenção.

2. Argumentos de Função: As regras de passagem de argumentos (positional-only e keyword-only) foram implementadas conforme solicitado, o que torna o uso das funções mais claro e seguro.

3. Cadastro de Usuários e Contas: Agora é possível cadastrar múltiplos usuários e contas, com validação para não duplicar CPFs. As contas são vinculadas aos usuários, como solicitado.

4. Controle de Transações com Data e Hora:

 - O sistema agora utiliza a biblioteca datetime com pytz para registrar o momento exato de cada transação em UTC.

 - Ao exibir o extrato, a data e hora são convertidas para o fuso horário de São Paulo (America/Sao_Paulo), garantindo que o cliente veja o horário local.

 - Foi implementado um limite de 10 transações diárias, que é verificado antes de cada depósito ou saque.

O sistema está pronto para os próximos desafios. O próximo passo natural seria permitir que o usuário selecione uma conta para realizar as operações, evoluindo para um sistema multi-contas completo.

Todo código foi criado com ajuda de IA.
