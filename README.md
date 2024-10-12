Modificações na Classe ContaCorrente e no Método nova_conta

Durante o desenvolvimento do sistema bancário, identifiquei um problema relacionado à criação de contas, mais especificamente ao tentar passar os parâmetros limite e limite_saques ao método nova_conta. O erro ocorria porque o método nova_conta da classe Conta, herdada pela classe ContaCorrente, não estava preparado para receber esses argumentos adicionais.

Para resolver essa questão, foi necessário sobrescrever o método nova_conta dentro da classe ContaCorrente, de modo que ele aceitasse os parâmetros limite e limite_saques. Esse ajuste foi essencial, pois as contas correntes possuem um limite de crédito e um número máximo de saques diários, características que não estão presentes na classe base Conta.

Além disso, fiz ajustes no construtor (__init__) de ContaCorrente, garantindo que os valores de limite e limite_saques fossem devidamente atribuídos ao criar uma nova conta. Agora, ao chamar o método nova_conta, o sistema consegue definir essas características de forma clara e específica para cada conta corrente criada.

Essas modificações tornaram o código mais flexível e coerente com a lógica de negócios, permitindo a criação de contas correntes personalizadas e corrigindo o erro identificado anteriormente.
