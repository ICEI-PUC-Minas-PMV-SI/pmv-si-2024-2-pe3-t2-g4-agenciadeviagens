# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE

Nesta parte do trabalho você deve detalhar a documentação dos requisitos do sistema proposto de acordo com as seções a seguir. Ressalta-se que aqui é utilizado como exemplo um sistema de gestão de cursos de aperfeiçoamento.

## 3.1 Objetivos deste documento
Descrever e especificar as necessidades da Coordenação do Curso de Sistemas de Informação da PUC Minas que devem ser atendidas pelo projeto SCCA – Sistema de Cadastro de Cursos de Aperfeiçoamento.

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
| RF1 | Gerenciar Pacotes de Viagem | Processamento de inclusão  alteração, exclusão e consulta de pacotes de viagem (ex.: destinos, preços, duração) |
| RF2 | Gerenciar Reservas | Processamento de inclusão, alteração , exclusão e consulta de reservas (ex.: reservas de hotéis, passagens aéreas, transfers) |
| RF3 | Gerenciar Clientes | Processamento de inclusão, alteração , exclusão e consulta de dados de clientes (ex.: nome, contato, histórico de viagens) |
| RF4 | Gerenciar Pagamentos | Processamento de inclusão, alteração  exclusão e consulta de pagamentos (ex.: métodos de pagamento, confirmação de pagamento, reembolsos) |
| RF5 | Gerenciar Relatórios | Consulta e geração de relatórios analíticos sobre vendas, reservas, preferências de clientes e outros dados operacionais |



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
Como observado no diagrama de casos de uso da Figura 1, a secretária poderá gerenciar as matrículas e professores no sistema, enquanto o coordenador, além dessas funções, poderá gerenciar os cursos de aperfeiçoamento.

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![](docs/images/CasosDeUso.png)
 
### 3.4.2 Descrições de Casos de Uso

Cada caso de uso deve ter a sua descrição representada nesta seção. Exemplo:

### Entrar no sistema (CSU01)
Sumário: O usuário comum realiza o acesso ao sistema.

Ator Primário:Usuário comum ou Gerente de Agência de Viagens.

Ator Secundário: Não Possui.

Pré-condiçoes:Usuário deve estar cadastrado no sistema.

Fluxo Principal:
1) O usuário comum informa o usuário de login e senha.
2) O Sistema Realiza a validação de senha informada.
3) Se o usuário comum iformou a senha errada, o sistema apresenta mensagem de erro "Senha Incorreta" e o caso de uso retorna ao passo 1; caso contrário o caso de uso termina;
   
Pós-condições: O usuáio entra no sistema e tem acesso às suas infromaç~oes e funcionalidades


### Reservar Viagem(CSU02)
Sumário: O usuário comum realiza a reserva de um pacote de viagem.

Ator Primário: Usuário Comum.

Ator Secundário: Não possui.

Pré-condições: Usuário deve fazer o login no sistema.

Fluxo Principal:
1) O usuário pesquisa um pacote de viagem de seu interesse.
2) O usuário escolhe um hotel, voo, e uma data e a opção que mais deseja entre as possibilidades.
3) O usuário efetua o pagamento
Pós-condições: O usuário conclui a compra do pacote

### Avaliar Viagem (CSU03)
Sumário: O usuário comum realiza uma avaliação de um pacote de viagem que ele já utilizou.

Ator Primário: Usuário comum.

Ator Secundário: Não possui.

Pré-condiçoes:O usuário deve ter feito o login e já ter concluído a viagem que ele irá avaliar.

Fluxo Principal:
1) O usuário acessa as viagens concluídas por ele e seleciona qual deseja avaliar.
2) O usuário faz uma avaliação com um medidor de 0 a 5 estrelas, além de um texto de no mínimo 100 caracteres descrevendo sua experiência.
Pós-condições: Uma avaliação foi adicionada à aquela viagem selecionada.

### Solicitar Reembolso(CSU04)

Sumário:O usuário comum realiza um pedido de reembolso.

Ator Primário: Usuário comum.

Ator Secundário: Gerente da agência de viagens.

Pré-condiçoes: O usuário deve fazer login e já ter feito alguma compra para poder solicitar o reembolso.

Fluxo Principal:
1) O usuário solicita o reembolso de uma compra feita por ele.
2) O sistema análisa o tempo restante para o início da viagem.
3) Reembolso passa por análise do Gerente de Agência de Viagens

Fluxo alternativo(2): Faltam mais de 90 dias

a) O usuário receberá 75% do valor da compra.

Fluxo alternativo(2): Faltam mais de 30 dias

a) O usuário receberá 50% do valor da compra.

Fluxo alternativo(2): Faltam mais de 15 dias

a) O usuário receberá 35% do valor da compra.

Fluxo alternativo(2): Faltam mais de 7 dias

a) O usuário receberá 10% do valor da compra.

Pós-condições: O usuário concluirá sua solicitação de reembolso e recebrá o valor em até 3 dias úteis.

### Solicitar Suporte(CSU05)
Sumário:O usuário comum inicia uma nova solicitação de suporte
Ator Primário:Usuário comum
Ator Secundário:Não possui
Pré-condiçoes:Usuário deve fazer login.

Fluxo Principal:
1) O usuário comum informa a necessidade de suporte.
2) O sistema aprensenta opções de setores de dúvidas: Reembolso, Reserva de viagem, Avaliar viagem, Login, Pesquisa de viagem, Gerenciamento de Viagens.
3) O usuário comum seleciona o setor com dúvida: Reembolso, Reserva de viagem, Avaliar viagem, Login, Pesquisa de viagem, Gerenciamento de Viagens e já informa o motivo da solicitação do suporte.
4) O sistema deve responder em no máximo 24 horas.
5) Após a resolução do probelma, se o usuário ainda tiver alguma dúvida o caso de uso retorna ao passo 2, caso contrário o caso de uso termina.

Fluxo Alternativo(3): Reembolso

a)O usuário é direcionado para o setor de suporte de reembolso.

Fluxo Alternativo(3): Reserva de Viagem

a)O usuário é direcionado para o setor de suporte de reserva de viagem.

Fluxo Alternativo(3): Avaliar Viagem

a)O usuário é direcionado para o setor de suporte de avaliação de viagem.

Fluxo Alternativo(3): Login

a)O usuário é direcionado para o setor de suporte de login.

Fluxo Alternativo(3): Pesquisa de Viagem

a)O usuário é direcionado para o setor de suporte de pesquisa de viagem.

Fluxo Alternativo(3): Gerenciamento de viagem.

a)O usuário é direcionado para o setor de suporte de gerenciamento de viagem.

Pós-condições:O problema será resolvido e anotado para análise e manuntenção.

### Gerenciar Viagens (CSU06)
Sumário: O Usuário Comum realiza a gestão de suas viagens, podendo gerenciar viagens futuras, pacotes de viagem favoritos e consultar viagens já concluídas.

Ator Primário: Usuário Comum.

Pré-condições: O Usuário Comum deve estar autenticado no sistema.

Fluxo Principal:

1. O Usuário acessa a funcionalidade de Gerenciar Viagens.
2. O Sistema apresenta as três opções disponíveis: Gerenciar Viagens Futuras, Gerenciar Pacotes de Viagem Favoritos ou Verificar Viagens Concluídas.
3. O Usuário seleciona a operação desejada.
4. O Sistema apresenta as informações relacionadas à opção selecionada.
5. O Usuário pode realizar ações de inclusão, exclusão, alteração ou consulta relacionadas à operação escolhida, ou optar por encerrar o caso de uso.

Se o Usuário desejar realizar outra operação, o caso de uso retorna ao passo 2; caso contrário, o caso de uso termina.

Fluxo Alternativo (1): Gerenciar Viagens Futuras

a) O Usuário seleciona a opção "Gerenciar Viagens Futuras".

b) O Sistema apresenta uma lista de viagens reservadas que ainda não foram realizadas.

c) O Usuário pode consultar os detalhes de uma viagem, alterar a reserva (se permitido), ou cancelar a viagem.

d) O Sistema processa a solicitação e, se houver alterações, atualiza a lista de viagens futuras.

Fluxo Alternativo (2): Gerenciar Pacotes de Viagem Favoritos

a) O Usuário seleciona a opção "Gerenciar Pacotes de Viagem Favoritos".

b) O Sistema apresenta uma lista de pacotes de viagem que o usuário marcou como favoritos.

c) O Usuário pode consultar os detalhes de um pacote, remover da lista de favoritos, ou optar por reservar o pacote.

d) O Sistema processa a solicitação e, se houver alterações, atualiza a lista de pacotes favoritos.

Fluxo Alternativo (3): Verificar Viagens Concluídas

a) O Usuário seleciona a opção "Verificar Viagens Concluídas".

b) O Sistema apresenta uma lista de viagens que o usuário já realizou.

c) O Usuário pode consultar os detalhes das viagens concluídas, incluindo destino, datas, e histórico de reservas, mas não pode alterá-las.

d) O Usuário pode optar por retornar ao menu principal ou encerrar o caso de uso.
Pós-condições: O Usuário Comum gerenciou suas viagens futuras, pacotes de viagem favoritos ou verificou viagens concluídas, realizando as devidas ações de consulta, alteração, inclusão ou exclusão.

### Buscar Viagem (CSU07)
Sumário: O Usuário Comum realiza a busca e consulta de pacotes de viagem disponíveis no sistema.

Ator Primário: Usuário Comum.

Pré-condições: O Usuário deve estar autenticado no sistema.

Fluxo Principal:

1. O Usuário acessa a funcionalidade de busca de pacotes de viagem.
2. O Sistema solicita que o usuário forneça critérios de busca, como destino, data, duração, ou faixa de preço.
3. O Usuário insere os critérios desejados e confirma a busca.
4. O Sistema processa os critérios e apresenta uma lista de pacotes de viagem que correspondem aos parâmetros fornecidos.
5. O Usuário pode selecionar um pacote para visualizar os detalhes.
6. O Sistema exibe os detalhes completos do pacote de viagem, incluindo destino, data, preço, disponibilidade, descrição e condições.
7. O Usuário pode optar por realizar outra busca, reservar a viagem ou encerrar o caso de uso.

Fluxo Alternativo (1): Busca sem Resultados

a) O Sistema não encontra pacotes de viagem que correspondam aos critérios fornecidos.

b) O Sistema informa o Usuário que não foram encontrados resultados para os parâmetros especificados e oferece a opção de refinar a busca ou encerrar o caso de uso.

Fluxo Alternativo (2): Pacote Indisponível

a) O Usuário seleciona um pacote que está indisponível (por exemplo, esgotado ou fora do período de validade).

b) O Sistema informa o Usuário da indisponibilidade e oferece a opção de buscar outros pacotes ou encerrar o caso de uso.
Pós-condições: O Usuário visualizou os pacotes de viagem disponíveis ou foi informado da ausência de resultados conforme os critérios de busca fornecidos.

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

### Gerenciar Usuário (CSU09)
Sumário: O Gerente de Agência realiza a gestão (inclusão, remoção, alteração e consulta) dos usuários do sistema.

Ator Primário: Gerente de Agência.

Ator Secundário: Usuário Comum.

Pré-condições: O Gerente de Agência deve ser validado pelo Sistema.
Fluxo Principal:

1. O Gerente de Agência requisita a manutenção dos usuários.
2. O Sistema apresenta as operações disponíveis: inclusão de um novo usuário, alteração de um usuário existente, exclusão de um usuário ou consulta dos usuários cadastrados.
3. O Gerente de Agência seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
Se o Gerente desejar continuar a gestão de usuários, o caso de uso retorna ao passo 2; caso contrário, o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Gerente requisita a inclusão de um novo usuário.

b) O Sistema apresenta um formulário solicitando os dados do usuário (Nome, CPF, E-mail, Telefone, Endereço, Nome de Usuário, Senha, Nível de Acesso).

c) O Gerente preenche os dados do novo usuário.

d) O Sistema verifica a validade dos dados. Se válidos, o novo usuário é incluído e a lista de usuários é atualizada; caso contrário, o Sistema reporta o erro e solicita correções.

Fluxo Alternativo (2): Remoção

a) O Gerente seleciona um usuário e solicita sua remoção.

b) Se o usuário pode ser removido (por exemplo, se não houver operações críticas associadas a ele), o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (3): Alteração

a) O Gerente altera um ou mais detalhes de um usuário existente e requisita a atualização.

b) O Sistema verifica a validade dos dados e, se forem válidos, atualiza os dados do usuário na lista; caso contrário, o erro é reportado.

Fluxo Alternativo (4): Consulta

a) O Gerente opta por pesquisar usuários pelo nome, CPF ou nome de usuário.

b) O Sistema apresenta a lista de usuários correspondentes.

c) O Gerente seleciona o usuário desejado.

d) O Sistema exibe os detalhes do usuário selecionado no formulário.

Pós-condições: Um usuário foi inserido, removido, seus dados foram alterados ou consultados.

### Gerenciar Pacotes de Viagens (CSU10)
Sumário: O Gerente de Agência realiza a gestão (inclusão, remoção, alteração e consulta) dos pacotes de viagens oferecidos aos clientes.

Ator Primário: Gerente de Agência.

Pré-condições: O Gerente de Agência deve ser validado pelo Sistema.

Fluxo Principal:

1. O Gerente de Agência requisita a manutenção de pacotes de viagens.
2. O Sistema apresenta as operações disponíveis: inclusão de um novo pacote, alteração de um pacote existente, exclusão de um pacote ou 3. consulta de pacotes cadastrados.
4. O Gerente de Agência seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
Se o Gerente desejar continuar a gestão de pacotes, o caso de uso retorna ao passo 2; caso contrário, o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Gerente requisita a inclusão de um novo pacote de viagem.

b) O Sistema apresenta um formulário para o preenchimento dos detalhes do pacote (Código, Nome do Pacote, Destino, Descrição, Duração, Preço, Data de Início, Data de Término, Número de Vagas Disponíveis, Observações).

c) O Gerente de Agência preenche os detalhes do novo pacote.

d) O Sistema verifica a validade dos dados. Se válidos, o novo pacote é incluído e a lista de pacotes é atualizada; caso contrário, o Sistema reporta o erro e solicita correções.

Fluxo Alternativo (2): Remoção

a) O Gerente de Agência seleciona um pacote de viagem e solicita sua remoção.

b) Se o pacote pode ser removido (por exemplo, se não houver reservas associadas), o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (3): Alteração

a) O Gerente altera um ou mais detalhes de um pacote existente e requisita a atualização.

b) O Sistema verifica a validade dos dados e, se forem válidos, atualiza os dados do pacote na lista; caso contrário, o erro é reportado.

Fluxo Alternativo (4): Consulta

a) O Gerente de Agência opta por pesquisar pacotes de viagens pelo nome, código ou destino.

b) O Sistema apresenta a lista de pacotes correspondentes.

c) O Gerente seleciona o pacote desejado.

d) O Sistema exibe os detalhes do pacote selecionado no formulário.

Pós-condições: Um pacote de viagem foi inserido, removido, seus dados foram alterados ou consultados.

### Integração com Fornecedores (CSU11)
Sumário: O Gerente de Agência realiza a integração e manutenção de informações (inclusão, exclusão, alteração e consulta) sobre fornecedores.

Ator Primário: Gerente de Agência.

Pré-condições: O Gerente de Agência deve ser validado pelo Sistema.

Fluxo Principal:

1. O Gerente de Agência requisita a manutenção de fornecedores.
2. O Sistema apresenta as operações disponíveis: inclusão de um novo fornecedor, alteração de um fornecedor, exclusão de um fornecedor ou consulta de dados de um fornecedor.
3. O Gerente de Agência seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
Se o Gerente de Agência desejar continuar a gestão de fornecedores, o caso de uso retorna ao passo 2; caso contrário, o caso de uso termina.

Fluxo Alternativo (1): Inclusão

a) O Gerente de Agência requisita a inclusão de um fornecedor.

b) O Sistema solicita o CNPJ do fornecedor a ser cadastrado.

c) O Gerente de Agência fornece o CNPJ.

d) O Sistema verifica se o fornecedor já está cadastrado. Se sim, o Sistema reporta o fato e retorna ao início; caso contrário, apresenta um formulário em branco para preenchimento dos detalhes do fornecedor (CNPJ, Nome, Endereço, Cidade, Estado, Telefone, E-mail, Categoria de Fornecimento, Observações).

e) O Gerente de Agência fornece os detalhes do novo fornecedor.

f) O Sistema verifica a validade dos dados. Se válidos, o novo fornecedor é incluído e a lista de fornecedores é atualizada; caso contrário, o Sistema solicita novos dados e repete a verificação.

Fluxo Alternativo (2): Remoção

a) O Gerente de Agência seleciona um fornecedor e solicita sua remoção.

b) Se o fornecedor pode ser removido, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato.

Fluxo Alternativo (3): Alteração

a) O Gerente de Agência altera um ou mais detalhes do fornecedor e requisita a atualização.

b) O Sistema verifica a validade dos dados e, se forem válidos, altera os dados do fornecedor; caso contrário, o erro é reportado.

Fluxo Alternativo (4): Consulta

a) O Gerente de Agência opta por pesquisar pelo nome ou CNPJ do fornecedor.

b) O Sistema apresenta a lista de fornecedores correspondentes.

c) O Gerente de Agência seleciona o fornecedor desejado.

d) O Sistema exibe os detalhes do fornecedor selecionado no formulário.

Pós-condições: Um fornecedor foi inserido, removido, seus dados foram alterados ou consultados.

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. A Matrícula deve conter a identificação do funcionário responsável pelo registro, bem com os dados do aluno e turmas. Para uma disciplina podemos ter diversas turmas, mas apenas um professor responsável por ela.

#### Figura 2: Diagrama de Classes do Sistema.
 
![dcu](https://github.com/user-attachments/assets/97ab1aa8-eb03-4b58-9ad5-1697d414a451)

### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Turista |	Cadastro das informações referentes aos turistas. |
| 2	| Admin |	Cadastro de informações referentes aos administradores do sistema. |
| 3 |	Compra |	Transação de aquisição do pacote de viagem. |
| 4 |	Pacote |	Cadastro geral dos pacotes de viagem. |
| ... |	... |	... |
