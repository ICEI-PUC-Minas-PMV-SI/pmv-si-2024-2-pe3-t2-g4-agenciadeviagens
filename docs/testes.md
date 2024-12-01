# 5. PLANO DE TESTES DE SOFTWARE
   
Nesta etapa devem ser realizados dois tipos de avaliação: por observação de sessão de uso (teste com usuários) e por inspeção (avaliação heurística, realizada pelos especialistas em usabilidade). Foram disponibilizados em "Material de Apoio" modelos para o registro dos testes que deverão ser realizados da seguinte maneira:
•	Na avaliação heurística, cada integrante do grupo deverá preencher a planilha correspondente ao teste (arquivo Avaliação_Heurística.xlsx). Ao final, os resultados deverão ser compilados em arquivo único de mesmo formato.
•	Na avaliação por observação de sessão de uso, deverão ser definidas tarefas em quantidade igual ao número de integrantes do grupo (ex.: grupo com 5 integrantes, 5 tarefas) e documentadas no relatório de testes com usuário (arquivo Relatório_de_Testes_com_Usuário.docx). Cada integrante do grupo deverá realizar o teste com um usuário distinto (ex.: grupo com 5 integrantes, 5 usuários deverão ser escolhidos, um por cada membro, para a realização dos testes).

Ao final, os relatórios gerados por cada membro deverão ser disponibilizados aqui, juntamente com a planilha consolidada da avaliação heurística.

Material de apoio para esta etapa:


[Avaliação_Heurística.xlsx](https://github.com/user-attachments/files/16501461/Avaliacao_Heuristica.xlsx) 

[Relatório_de_Testes_com_Usuário.docx](https://github.com/user-attachments/files/16501456/Relatorio_de_Testes_com_Usuario.docx)

[Relatório_de_Testes_com_Usuário_exemplo.docx](https://github.com/user-attachments/files/16501459/Relatorio_de_Testes_com_Usuario_exemplo.docx)

# Relatório de Teste com Usuário

**Projeto (Nome do Sistema):** Mundo Sem Fronteiras  
**Equipe:** [Sua Equipe]  

**Nome do Avaliador:** [Seu Nome]  
**Data:** 01/12/2024  
**Participante Nº:** 1  

---

## Proposta

A proposta deste teste é verificar o entendimento e a usabilidade do sistema *Mundo Sem Fronteiras* a partir das interações de um usuário representativo do público-alvo. O teste também avalia a satisfação geral do uso pelo usuário.

---

## Questões Introdutórias e Tarefas

1. **Você já ouviu falar desse tipo de sistema?**  
   ___Sim    ___Não  
   - **Caso sim, diga-me o que você sabe sobre:**  
     "Sim, já ouvi falar. É um sistema de busca de pacotes de viagem e promoções."

2. **Através da tela inicial, que tipo de informação você acha que poderia obter desse sistema?**  
   - "Eu acho que posso procurar por destinos e pacotes promocionais de viagem."

3. **Para quem você acha que esse sistema foi desenvolvido? Por quê?**  
   - "Parece ser desenvolvido para qualquer pessoa que queira viajar, principalmente quem está buscando ofertas e pacotes turísticos."

4. **Quem você acha que é o responsável por esse sistema?**  
   - "Provavelmente uma agência de viagens ou uma empresa especializada em turismo."

---

## Cenário

Imagine que você está planejando uma viagem e deseja procurar pacotes e ofertas. Você está na página inicial do site e deseja buscar pacotes, adicionar um ao carrinho e realizar uma compra.

---

## Tarefa 1: Buscar pacotes de viagem

| **Descrição dos Passos Esperados**                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------|
| 1. O usuário localiza o formulário de busca na tela inicial.                                                            |
| 2. Preenche os campos de origem e destino.                                                                              |
| 3. Insere as datas e clica no botão "Buscar destino".                                                                   |

| **Caminhos**                   | **Resultado**                       | **Anotações / Observações**                                                           |
|--------------------------------|-------------------------------------|---------------------------------------------------------------------------------------|
| 0 - Não completou              |                                     |                                                                                       |
| 1 - Completou com dificuldade  | Sim                                 | O usuário teve dificuldade em entender o campo "Data de Retorno".                    |
| 2 - Completou facilmente       |                                     |                                                                                       |

---

## Tarefa 2: Adicionar um pacote ao carrinho de compras

| **Descrição dos Passos Esperados**                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------|
| 1. O usuário visualiza os pacotes de viagem na página de resultados.                                                    |
| 2. Seleciona um pacote e clica no botão "Adicionar ao Carrinho".                                                        |

| **Caminhos**                   | **Resultado**                       | **Anotações / Observações**                                                           |
|--------------------------------|-------------------------------------|---------------------------------------------------------------------------------------|
| 0 - Não completou              |                                     |                                                                                       |
| 1 - Completou com dificuldade  | Sim                                 | O botão "Adicionar ao Carrinho" estava difícil de localizar entre as opções de pacotes. |
| 2 - Completou facilmente       |                                     |                                                                                       |

---

## Tarefa 3: Consultar ofertas de pacotes

| **Descrição dos Passos Esperados**                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------|
| 1. O usuário deve rolar a página para encontrar a seção de "Ofertas".                                                   |
| 2. Clica em uma promoção e visualiza os detalhes do pacote.                                                             |

| **Caminhos**                   | **Resultado**                       | **Anotações / Observações**                                                           |
|--------------------------------|-------------------------------------|---------------------------------------------------------------------------------------|
| 0 - Não completou              |                                     |                                                                                       |
| 1 - Completou com dificuldade  | Sim                                 | O usuário achou os descontos pouco evidentes.                                         |
| 2 - Completou facilmente       |                                     |                                                                                       |

---

## Questionário Final

1. **Qual foi a sua impressão geral do sistema?**  
   - "Achei o sistema funcional, mas algumas partes podem ser mais claras."

2. **Qual foi a sua impressão sobre as atividades propostas?**  
   - "As tarefas foram bem organizadas, mas algumas tinham pequenos problemas de usabilidade."

3. **Você acha que este sistema é atual? Por quê?**  
   - "Sim, o design é moderno, mas a experiência de navegação pode ser aprimorada."

4. **O que você mais gostou neste sistema?**  
   - "A facilidade de buscar pacotes e promoções."

5. **O que você menos gostou neste sistema?**  
   - "A falta de destaque em algumas seções, como o botão de adicionar ao carrinho."

6. **Há alguma coisa que você acha que está faltando neste sistema?**  
   - "Filtros mais detalhados na busca de pacotes."

7. **Se você fosse descrever este sistema para um colega em uma sentença ou duas, o que você diria?**  
   - "Um site funcional para buscar e reservar pacotes de viagem, mas com algumas áreas que podem ser melhoradas."

8. **Você gostaria de fazer algum comentário final ou pergunta?**  
   - "Gostei da proposta, mas acho que algumas funções podem ser mais intuitivas."

---

## Conclusões do Avaliador sobre o Teste com o Usuário

### Problemas Identificados
1. **Campos de Formulário:** Dificuldade em identificar os campos de datas no formulário de busca.  
2. **Botões Visíveis:** Botão "Adicionar ao Carrinho" pouco destacado.  
3. **Destaque em Promoções:** Os descontos não chamam atenção suficiente na seção de ofertas.

### Recomendações de Melhorias
1. Aumentar a clareza dos campos no formulário de busca, especialmente os de data.  
2. Melhorar o destaque visual dos botões de ação, como "Adicionar ao Carrinho".  
3. Usar cores mais vibrantes ou etiquetas para destacar as promoções na página inicial.

---



