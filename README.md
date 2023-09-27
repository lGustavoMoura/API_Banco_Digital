# API_Banco_Digital

Esse repositório é de um projeto de uma API de um banco digital. Esse projeto foi criado com as funções básicas de um banco, como transações, saques e outras funcionalidades. Essa API foi construída com o objetivo de avaliar minhas habilidades, mas abaixo eu explico mais sobre como executar o preojeto.


## Como executar o projeto
<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/7ff54e95-87af-45d4-b9d5-e4d1df56d6a0" width="600px" />
</div>

**listarContas:** Essa função retorna todas as contas do banco se a senha do banco for informada e correta. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.get('/contas')**, no Insomnia usamos essa URL http://localhost:3000/contas?senha_banco=Cubos123Bank como uma rota HTTP GET.

<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/52546b4d-cd37-465c-ac54-105008e7c605" width="600px" />
</div>

**cadastrarContas:** Essa função cria uma nova conta com os dados informados, se não houver outra conta com o mesmo cpf ou email. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.post('/contas')**, no Insomnia usamos essa URL http://localhost:3000/contas?senha_banco=Cubos123Bank como uma rota HTTP POST.

<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/af34d974-9f7a-44fe-b667-e3799a9a775a" width="600px" />
</div>

**atualizarConta:** Essa função atualiza os dados de uma conta existente, se não houver outra conta com o mesmo cpf ou email. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.put('/contas/:numeroConta/usuario')**, no Insomnia usamos essa URL http://localhost:3000/contas/1/usuario como uma rota HTTP PUT. *Os dados da requisição deverão ser enviados no corpo (body).*


<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/382bbf1d-6713-40fb-a303-9fe8197f8462" width="600px" />
</div>

**excluirConta:** Essa função exclui uma conta existente, se o saldo dela for zero. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.delete('/contas/:numeroConta')**, no Insomnia usamos essa http://localhost:3000/contas/1 como uma rota HTTP DELETE.

<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/b8deb477-334b-4d07-bacb-5655c9efa60c" width="600px" />
</div>

**depositarNaConta:** Essa função adiciona um valor ao saldo de uma conta existente, se o valor for positivo. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.post('/transacoes/depositar')**, no Insomnia usamos essa URL http://localhost:3000/transacoes/depositar como uma rota HTTP POST.

<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/fe955c69-ae49-4f51-af90-845c09c82d23" width="600px" />
</div>

**sacarDinheiroDaConta:** Essa função subtrai um valor do saldo de uma conta existente, se a senha e o valor forem corretos. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.post('/transacoes/sacar')**, no Insomnia usamos essa URL http://localhost:3000/transacoes/sacar como uma rota HTTP POST.


<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/9be698cb-ecd6-4202-bb9a-d7e33c2de062" width="600px" />
</div>

**Transacao:** Essa função faz a transferência de dinheiro de uma conta para outra e registra essa operação. Ela precisa dos seguintes dados número da conta de origem, número da conta de destino, valor da transferência e senha da conta de origem. Ela verifica se as contas e a senha são válidas, se há saldo suficiente na conta de origem e atualiza os saldos das contas. Ela retorna uma resposta com o resultado da operação. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.post('/transacoes/transferir')**, no Insomnia usamos essa URL http://localhost:3000/transacoes/transferir como uma rota HTTP POST.


<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/83a175eb-8fd4-49b6-a1d3-a443328f2ef9" width="600px" />
</div>

**saldoDisponivel:** Essa função é usada para consultar o saldo de uma conta bancária. Ela precisa do número da conta e da senha na URL. Ela verifica se a conta e a senha são válidas e retorna o saldo da conta. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.get('/contas/saldo')**, no Insomnia usamos essa URL http://localhost:3000/contas/saldo?numero_conta=2&senha=12345 como uma rota HTTP GET.



<div align="center">
<img src="https://github.com/lGustavoMoura/API_Banco_Digital/assets/140130394/777b96ee-8013-4ec2-8048-909a220051f8" width="600px" />
</div>

**extrato:** Essa função retorna um extrato bancário se o número da conta e a senha forem válidos, se não forem válidos ira mostrar um mensagem de erro. Para usar essa função nos usaremos o programa Insomnia para testar a API. Usamos essa rota **router.get('/contas/extrato')**, no Insomnia usamos essa URL http://localhost:3000/contas/extrato?numero_conta=1&senha=1234 como uma rota HTTP GET.
