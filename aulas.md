# 27/02/2024 - Aulas de inicio do segundo trabalho

## Controlo de acesso
Nos primeiro sistemas já existia o Reference Monitoring .

* Engloba três principais operações:
 * Autenticação - ;
 * Autorização - user roles;
 * Auditoria - ;

* Modelos para implementação para o controlo de acesso:
 * Existem dois grandes o Kerberos e o Activity Directory(Igual ao Kerberos, mas feito pela Microsoft)
 * A parte de auditoria fica mais complexa, porque temos de verificar em dois servidores.

## Politicas

* DAC:
 * É o que nós temos no nosso computador, base dos computadores pessoais;

* MAC
 * Como se comprassemos o computador e não podessemos mudar nada no controlo de acesso;
 * Mais para contexto militar;
 * É precisso verificar tudo em todas as operações que alguém queira fazer;

* RBAC
 * Criamos um conjunto de roles;
 * Cada role tem um conjunto de regras;

* ABAC - Este não é tão importante como os outros 3
 * Igual ao RBAC, com uma pequena alteração;
 * Em vez de fazermos a divisão por roles, fazemos a divisão por atributos;
 * Mais usado para divisão geográfica,
 * Exemplo google maps, waze, etc

##  Modelos de Segurança



### Bell-LaPadula (BLP) - O que vamos usar no trabalho
* MAC E DAC
* Mostra os principios gerais.
* Modelo estático - não é muito bom para os sistemas atuais.
* Temos o Chinese Wall que é uma alternativa dinâmica.
* É bastante formal.
* Apenas garantimos a confidencialidade.
* Se tivermos 100% de confidencialidade, não conseguimos ter 100% de integridade
* Temos sempre Multi-level Security (MLS), por exemplo Publico, estrito, etc...
* Uso da sanatização
* Baseado em transições de estado

## Exercicio
label - nivel de segurança e conjunto de categorias exemplo: (C,{AS,ScS})
Lettice - relação entre todas as labels
* Lettice
* Pergunta se o aluno pode fazer batota
* COmo vou implementar isto, Elaborar como podia ser feito na realidade