# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE
Constarão a seguir os detalhamentos dos requisitos do sistema.

## 3.1 Objetivos deste documento
Descrever e especificar as necessidades da Agência de Viagens que devem ser atendidas pelo projeto  SAV - Sistema de Agência de Viagens .

## 3.2 Escopo do produto

### 3.2.1 Nome do produto e seus componentes principais
O produto será denominado SAV – Sistema de Agência de Viagens. Ele terá somente um componente (módulo) com os devidos elementos necessários à gestão de agências de viagens

### 3.2.2 Missão do produto
A missão do SAV – Sistema de Agência de Viagens é centralizar e otimizar a gestão de uma agência de viagens, oferecendo uma plataforma única e eficiente que permita o controle de todos os processos operacionais. O objetivo é facilitar a administração de pacotes de viagens, cadastro de clientes, reservas e transações financeiras de maneira integrada e segura.

Além disso, o SAV visa proporcionar uma interface de fácil utilização tanto para os gestores da agência quanto para os clientes, garantindo que a experiência de reserva e compra seja simples, ágil e confiável. Ao promover a automação de tarefas repetitivas e o controle preciso de dados, o sistema busca aumentar a eficiência operacional da agência, reduzir erros e melhorar a satisfação do cliente, entregando uma solução completa e segura para a gestão de viagens.

### 3.2.3 Limites do produto
O SAV pode vender pacotes e fornecer informações, mas não oferece acompanhamento físico durante a viagem. Para questões como passeios guiados ou suporte local imediato, o viajante ainda pode precisar recorrer a serviços ou guias locais.

### 3.2.4 Benefícios do produto

| # | Benefício | Valor para o Cliente |
|--------------------|------------------------------------|----------------------------------------|
|1	| Facilidade no cadastro de dados |	Essencial |
|2 | Facilidade na recuperação de informações | Essencial | 
|3 | Segurança no cadastro de dados | Essencial | 
|4 | Segurança na contratação de serviço | Essencial | 
|5	| Melhoria na comunicação entre agencias	| Essencial | 
|6	| Segurança na compra e venda de pacotes	| Essencial | 
|7	| Ajude na comunicação entre agencias	| Recomendável | 

## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| RF1 | Gerenciar Minhas Viagens | Processamento de Inclusão, Alteração, Exclusão e Consulta de viagens (criadas pelo usuário) |
| RF2 | Pesquisar Viagem | Pesquisar pacote de viagem na lista geral (todos os pacotes da agência) |
| RF3 | Reservar Viagem | Processamento inclusão de reserva de um pacote de viagem |
| RF4 | Gerenciar avaliação de Viagem | Processamento de Inclusão, Alteração, Exclusão e Consulta de avaliação de viagem |
| RF5 | Gerenciar "Reservas" | Processamento de Inclusão, Alteração, Exclusão e Consulta de itens na "Reservas"(pacotes de viagem que o usuário ja possui) |
| RF6 | Solicitar Reembolso | Solicitar reembolso pelo cancelamento de um pacote de viagem |
| RF7 | Gerenciar Pacotes de Viagem | Processamento de inclusão  alteração, exclusão e consulta de pacotes de viagem (ex.: destinos, preços, duração) |
| RF8 | Gerenciar Usuário | Processamento de inclusão, alteração , exclusão e consulta de dados de clientes (ex.: nome, contato, histórico de viagens) |
| RF9 | Gerenciar Pagamentos | Processamento de inclusão, alteração , exclusão e consulta de pagamentos (ex.: métodos de pagamento, confirmação de pagamento, reembolsos) |
| RF10 | Entrar No Sistema | Processamento de login de cadastro |
| RF11 | Sair do sistema | Processamento de logout de cadastro |
| RF12 | Validação da senha | Processamento de validação de cadastro |






### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional | Descrição | Prioridade |
|-------------|-------------|-------------|------------------------|
| RNF1 | Responsivo | A aplicação deve se adaptar o layout do dispositivo.| Alta ||
| RNF2 | Layout | Ter um layout intuitivo e de fácil compreensão para os usuários. | Alta ||
| RNF3 |	Requisição | Deve processar requisições do usuário em no máximo 3s | Baixa ||
| RNF4 |	Disponibilidade |	Sistema deve funcionar 24hrs, 7 dias na semana | Média ||
| RNF5 |	Manutenibilidade |	O sistema deve ser modular para facilitar a manutenção e atualização. | Média ||
| RNF6 |	Confiabilidade |	Os dados do usuário devem ser protegidos contra acesso não autorizado. |	Alta ||

### 3.3.3 Usuários 

| Ator | Descrição |
|--------------------|------------------------------------|
| Usúario comum|	Usuário responsável por compra de pacotes de viagem, avaliá-los, consultar pacotes, se cadastrar,solicitar reembolsos e suporte |
| Gerente de agência |	Usuário gerente do sistema, resposável pela administração dos fornecedores, bloqueios de usuários, e gerenciar pacotes. Possui acesso geral ao sistema|
| ... |	... |	... |

## 3.4 Modelagem do Sistema


### 3.4.1 Diagrama de Casos de Uso

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![Diagrama de Casos de Uso](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe3-t2-g4-agenciadeviagens/blob/main/docs/images/CasosDeUso.png)
 
### 3.4.2 Descrições de Casos de Uso

### Entrar no sistema (CSU01)
Sumário: O usuário comum realiza o acesso ao sistema.

Ator Primário:Usuário comum ou Gerente de Agência de Viagens.

Ator Secundário: Não Possui.

Pré-condiçoes:Usuário deve estar cadastrado no sistema.

Fluxo Principal:
1) O usuário comum informa o usuário de login e senha.
2) O Sistema Realiza a validação de senha informada.
3) Se o usuário comum informou a senha errada, o sistema apresenta mensagem de erro "Senha Incorreta" e o caso de uso retorna ao passo 1; caso contrário o caso de uso termina;
   
Pós-condições: O usuário entra no sistema e tem acesso às suas infromaç~oes e funcionalidades


### Reservar Viagem(CSU02)
Sumário: O usuário comum realiza a reserva de um pacote de viagem.

Ator Primário: Usuário Comum.

Ator Secundário: Não possui.

Pré-condições: Usuário deve fazer o login no sistema.

Fluxo Principal:
1) O usuário pesquisa um pacote de viagem de seu interesse.
2) O usuário escolhe um hotel, voo, e uma data e a opção que mais deseja entre as possibilidades.
3) O usuário efetua o pagamento.
4) O Sistema atualiza as reservas do usuário com o pacote de viagem comprado.
Pós-condições: O usuário conclui a compra do pacote

### Gerenciar Avaliação de Viagem (CSU03)
Sumário: O usuário comum realiza a gestão (inclusão, alteração, exclusão e consulta) de um pacote de viagem que ele já utilizou.

Ator Primário: Usuário comum.

Ator Secundário: Não possui.

Pré-condiçoes:O usuário deve ter feito o login e já ter concluído a viagem que ele irá avaliar.

Fluxo Principal:
1) O usuário requisita a gestão de suas avaliações.
2) O sistema apresenta as operações que podem ser realizadas: inclusão, exclusão, alteração e consulta por palavra que conste no título ou na descrição da avaliação
3) O usuário comum seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finnalizar o caso de uso.
4) Se o usuário comum desejar continuar com a gestão de suas receitas, o caso de uso retorna ao passo 2; caso contrario o caso de uso termina.

FLUXO ALTERNATIVO(3): INCLUSÃO

a) O usuário comum requisita a inclusão de uma avaliação.

b) O sistema apresenta uma janela solicitando o título da avaliação a ser cadastrada, sua descrição, destino, companhia aérea, data e hotel.

c) Após todos os campos serem preenchiodos e o usuário comum incluir a nova avaliação, a grade listando as avaliações cadastradas é atualizada.

FLUXO ALTERNATIVO(3): EXCLUSÃO

a) O usuário comum seleciona uma avaliação e requisita que o Sistema a remova.

b) O sistema realiza a remoção.

FLUXO ALTERNATIVO(3) ALTERAÇÃO

a) O usuário comum seleciona a avaliação para edição, altera os dados e requisita a atualização.

b) O Sistema altera os dados no cadastro da reserva.

FLUXO ALTERNATIVO(3): CONSULTA

a) O usuário comum opta por pesquisar pela palavra contida no título da avaliação ou na descrição dela e solicita a consulta sobre a lista de avaliações cadastradas por ele.

b) O Sistema apresenta uma lista de avaliações.

c) O usuário comum seleciona a avaliação.

d) O sistema apresenta os dados da avaliação.

Pós-condições: Uma avaliação foi inserida ou removida, seus dados foram alterados ou
apresentados na tela

### Solicitar Reembolso(CSU04)

Sumário:O usuário comum realiza um pedido de reembolso.

Ator Primário: Usuário comum.

Ator Secundário: Administrador.

Pré-condiçoes: O usuário deve fazer login e já ter feito alguma compra para poder solicitar o reembolso.

Fluxo Principal:
1) O usuário solicita o reembolso de uma compra feita por ele.
2) O sistema análisa o tempo restante para o início da viagem, caso faltarem menos de 30 dias o caso de uso é finalizado.
3) Reembolso passa por análise do administrador.


Pós-condições: O usuário concluirá sua solicitação de reembolso e receberá o valor em até 15 dias úteis.

### Pesquisar Viagem (CSU05)

Sumário: O usuário comum realiza a consulta de uma viagem cadastrada no
sistema.

Ator Primário: Usuário Comum.

Ator Secundário: Não possui.

Pré-condições: Não Possui.

Fluxo Principal:
1) O usuário comum requisita a consulta de uma viagem cadastrada no
sistema.
2) O Sistema apresenta as operações de busca de receita por palavra que conste no
título da viagem ou na sua descrição.
3) O usuário comum seleciona a Consulta, ou opta por finalizar o caso de uso.
4) Se o usuário comum desejar continuar com a consulta de receita, o caso de uso
retorna ao passo 2; caso contrário, o caso de uso termina.

Pós-condições: Uma viagem foi consultada, seus dados foram apresentados na tela


### Gerenciar "Reservas" (CSU06)
Sumário: O usuário comum realiza a gestão (alteração, exclusão e consulta) de uma reserva dele.

Ator Primário: Usuário comum.

Ator Secundário: Não possui.

Pré-condiçoes:O usuário deve ter feito o login.

Fluxo Principal:
1) O usuário requisita a gestão de suas reservas
2) O sistema apresenta as operações que podem ser realizadas: exclusão, alteração e consulta por palavra que conste no título ou na descrição da avaliação
3) O usuário comum seleciona a operação desejada: Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
4) Se o usuário comum desejar continuar com a gestão de suas receitas, o caso de uso retorna ao passo 2; caso contrario o caso de uso termina.

FLUXO ALTERNATIVO(3): EXCLUSÃO

a) O usuário comum seleciona uma reserva e requisita que o Sistema a remova.

b) A reserva de uma viagem que vai acontecer ela entre em processo de reembolso.

FLUXO ALTERNATIVO(3) ALTERAÇÃO

a) O usuário comum seleciona a reserva para edição, altera os dados e requisita a atualização.

b) O Sistema altera os dados no cadastro da reserva.

FLUXO ALTERNATIVO(3): CONSULTA

a) O usuário comum opta por pesquisar pela palavra contida no título da reserva ou na descrição dela e solicita a consulta sobre a lista de reserva feitas por ele.

b) O Sistema apresenta uma lista de reserva.

c) O usuário comum seleciona a reserva.

d) O sistema apresenta os dados da reserva.

Pós-condições: Uma reserva removida, seus dados foram alterados ou
apresentados na tela.

### GERENCIAR USUÁRIOS (CSU07)

Sumário: O usuário comum ou o administrador realiza a gestão (inclusão, alteração,
consulta e bloqueio) dos usuários comuns.

Ator Primário: Usuário comum ou Administrador.

Ator Secundário: Não possui.

Pré-condições: Usuário deve estar cadastrado no sistema como Administrador.

Fluxo Principal:
1) O Administrador requisita a gestão de usuários.
2) O Sistema apresenta as operações que podem ser realizadas: a inclusão de um
usuário comum, a alteração de um usuário comum, a busca de um usuário comum
e o bloqueio.
3) O Administrador seleciona a operação desejada: Inclusão, Exclusão, Consulta ou
opta por finalizar o caso de uso.
4) Se o usuário comum desejar continuar com a gestão de usuários, o caso de uso
retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (3): Inclusão

a) O Administrador requisita a inclusão de um usuário comum.

b) O Sistema apresenta uma janela solicitando o e-mail do usuário a ser cadastrado.

c) O Administrador fornece o dado solicitado.

d) O Sistema verifica se o usuário já está cadastrado. Se sim, o Sistema reporta o
fato e volta ao início; caso contrário, apresenta um formulário em branco para que
os detalhes do usuário comum (login, senha, email, nome, sobrenome e data de
nascimento) sejam incluídos.

e) O Administrador fornece os detalhes do novo usuário comum.

f) O Sistema verifica a validade dos dados. Se os dados forem válidos, inclui o novo
usuário comum e a grade listando os usuários comuns cadastrados é atualizada;
caso contrário, o Sistema reporta o fato, solicita novos dados e repete a
verificação.

Fluxo Alternativo (3): Alteração

a) O Administrador altera um detalhe, ou mais, do usuário comum e requisita sua
atualização.

b) O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados
na lista de usuários comuns, caso contrário, o erro é reportado.

Fluxo Alternativo (3): Consulta

a) O Administrador opta por pesquisar pelo nome ou código e solicita a consulta
sobre a lista de usuários comuns.

b) O Sistema apresenta uma lista de usuários comuns.

c) O Administrador seleciona um usuário comum.

d) O Sistema apresenta os detalhes do usuário comum no formulário de usuários
comuns.

Fluxo Alternativo (3): Bloqueio

a) O Administrador seleciona um usuário comum e requisita ao Sistema que o
bloqueie.

b) O Sistema realiza o bloqueio do usuário comum.

Pós-condições: Um usuário comum foi inserido ou bloqueado, seus dados foram
alterados ou apresentados na tela.

### Sair do Sistema (CSU08)
Sumário: O usuário comum sai do sistema.

Ator Primário: Usuário Comum ou Gerente de Agência.

Ator Secundário: Não possui.

Pré-condições: Usuário deve estar cadastrado no sistema.

Fluxo Principal:

1) O usuário comum acessa a função de saída.
2) O Sistema realiza o deslogue da conta.
4) Se o Usuário comum estiver com um processo em andamento, o sistema informa
que ele está com um processo em andamento e confirma com a seguinte
mensagem "Você possui dados não salvos que serão excluídos, deseja sair
mesmo assim?”, se ele clicar em não, o caso de uso retorna ao passo 1; caso
contrário o caso de uso termina.

Pós-condições: O usuário saiu do sistema.

### Gerenciar Pacotes de Viagens (CSU09)
Sumário: O Gerente de Agência realiza a gestão (inclusão, remoção, alteração e consulta) dos pacotes de viagens oferecidos aos clientes.

Ator Primário: Gerente de Agência.

Pré-condições: O Gerente de Agência deve ser validado pelo Sistema.

Fluxo Principal:

1) O Gerente de Agência requisita a manutenção de pacotes de viagens.
2) O Sistema apresenta as operações disponíveis: inclusão de um novo pacote, alteração de um pacote existente, exclusão de um pacote ou consulta de pacotes cadastrados.
3) O Gerente de Agência seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
4)Se o Gerente desejar continuar a gestão de pacotes, o caso de uso retorna ao passo 2; caso contrário, o caso de uso termina.

Fluxo Alternativo (3): Inclusão

a) O Gerente requisita a inclusão de um novo pacote de viagem.

b) O Sistema apresenta um formulário para o preenchimento dos detalhes do pacote (Código, Nome do Pacote, Destino, Descrição, Duração, Preço, Data de Início, Data de Término, Número de Vagas Disponíveis, Observações).

c) O Gerente de Agência preenche os detalhes do novo pacote.

d) O Sistema verifica a validade dos dados. Se válidos, o novo pacote é incluído e a lista de pacotes é atualizada; caso contrário, o Sistema reporta o erro e solicita correções.

Fluxo Alternativo (3): Remoção

a) O Gerente de Agência seleciona um pacote de viagem e solicita sua remoção.

b) Se o pacote pode ser removido (por exemplo, se não houver reservas associadas), o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (3): Alteração

a) O Gerente altera um ou mais detalhes de um pacote existente e requisita a atualização.

b) O Sistema verifica a validade dos dados e, se forem válidos, atualiza os dados do pacote na lista; caso contrário, o erro é reportado.

Fluxo Alternativo (3): Consulta

a) O Gerente de Agência opta por pesquisar pacotes de viagens pelo nome, código ou destino.

b) O Sistema apresenta a lista de pacotes correspondentes.

c) O Gerente seleciona o pacote desejado.

d) O Sistema exibe os detalhes do pacote selecionado no formulário.

Pós-condições: Um pacote de viagem foi inserido, removido, seus dados foram alterados ou consultados.

### Gerenciar Pagamnetos (CSU10)

Sumário: O Gerente de Agência realiza a gestão (inclusão, remoção, alteração e consulta) dos pagamentos dos clientes.

Ator Primário: Gerente de Agência.

Pré-condições: O Gerente de Agência deve ser validado pelo Sistema.

Fluxo Principal:

1. O Gerente de Agência requisita a gestão dos pagamentos.
2. O Sistema apresenta as operações disponíveis: Reembolso de um pagamento, inclusão de um pagamento, alteração de um pagamento, exclusão de um pagamento ou consulta de pagamentos.
4. O Gerente de Agência seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
Se o Gerente desejar continuar a gestão de pagamentos, o caso de uso retorna ao passo 2; caso contrário, o caso de uso termina.

Fluxo Alternativo (3) Reembolso

a) O Gerente seleciona um caso de reembolso para analisar.

b) Após a analise ele decide se o reembolso acontecerá ou não.

c) A solicitação de reembolso é retirada da lista de reembolso.

Fluxo Alternativo (3): Inclusão

a) O Gerente requisita a inclusão de um novo pagamento.

b) O Sistema apresenta um formulário para o preenchimento dos detalhes do pagamento (Código, Nome do Comprador, Destino, Data, Valor, Método de Pagamento).

c) O Gerente de Agência preenche os detalhes do novo pagamento.

d) O Sistema verifica a validade dos dados. Se válidos, o novo pagamento é incluído e a lista de pagamentos é atualizada; caso contrário, o Sistema reporta o erro e solicita correções.

Fluxo Alternativo (2): Remoção

a) O Gerente de Agência seleciona um pagamento e solicita sua remoção.

b) Se o pagamento pode ser removido (por exemplo, se não houver pendencias), o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (3): Alteração

a) O Gerente altera um ou mais detalhes de um pagamneto existente e requisita a atualização.

b) O Sistema verifica a validade dos dados e, se forem válidos, atualiza os dados do pagamento na lista; caso contrário, o erro é reportado.

Fluxo Alternativo (4): Consulta

a) O Gerente de Agência opta por pesquisar pagamentos pelo nome do comprador, código ou data.

b) O Sistema apresenta a lista de pagamento correspondentes.

c) O Gerente seleciona o pagamento desejado.

d) O Sistema exibe os detalhes do pagamento selecionado no formulário.

Pós-condições: Um pagamento foi reembolsado, inserido, removido, seus dados foram alterados ou consultados.

### Sair do Sistema (CSU11)


Sumário: O usuário comum sai do sistema

Ator Primário: Usuário Comum ou Administrador.

Ator Secundário: Não possui.

Pré-condições: Usuário deve estar cadastrado no sistema.

Fluxo Principal:

1) O usuário comum acessa a função de saída.

2) O Sistema realiza o deslogue da conta.

3) Se o Usuário comum estiver com um processo em andamento, o sistema informa
que ele está com um processo em andamento e confirma com a seguinte
mensagem "Você possui dados não salvos que serão excluídos, deseja sair
mesmo assim?”, se ele clicar em não, o caso de uso retorna ao passo 1; caso
contrário o caso de uso termina.
Pós-condições: O usuário saiu do sistema.


### 3.4.3 Diagrama de Classes 

#### Figura 2: Diagrama de Classes do Sistema.
 
![Diagrama de Classes](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2024-2-pe3-t2-g4-agenciadeviagens/blob/main/docs/images/Classes.png)

### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Turista |	Cadastro das informações referentes aos turistas. |
| 2	| Admin |	Cadastro de informações referentes aos administradores do sistema. |
| 3 |	Compra |	Transação de aquisição do pacote de viagem. |
| 4 |	Pacote |	Cadastro geral dos pacotes de viagem. |
| ... |	... |	... |
