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


# 12/03/2024 - Inicio de Projeto 3

O trabalho vai estar sobre as public keys entre emails a usar PKIs.

Tema principal - **Cirptografia**.

Usar **cifrar** e **desifrar** em vez de encritar

## Tema - Applied Cryptography

### Terminologia
* Plain text and Message - M
* Texto Cifrado - C
* Algoritmo de cifra - E
* Decifrar - D

* Areas
    * Cryptology - Parte da matematica que e a base da todo este mundo.

O que e que a criptgrafia oferece:
* Confidencialidade
* Integridade
* Autenticidade
* Não-repudio

Ataques:
* Tentar pegar em texto cifrado e tentar decifar (já não funciona)
* Se soubermos qual é o algoritmo e soubermos mais ao menos o contexto da mensage;
* Se tivermos um conjunto de mensagens e sabermos do que se trata, é possível conseguir chegar ao chave de cifra.

As empresas tem o wifi apenas para acesso a recursos não críticos, os recursos mais críticos são acedidos por uma network fora da rede de normalmente usada.

* **Restrict Algo**: O segredo está no algoritmo
    * Problema: Se alguém sai da nossa empresa, e se souber como funciona, pode ser um problema, para mudar os sistemas que o usam demora muito, não sendo assim escalavel
    * Tem de ter um numero limite 
* **Key Algo**: 
    * É preciso ter a chave, pois o algortimo é conhecido;
    * Em termos de vulnerabilidade é melhor;
    * É o que é mais usado hoje em dia;
    * **Algoritmos simétricos**: A chave que usamos para cifrar é a mesma para decifrar.
    * **Public key Algo**/**Algoritmos assimétricos**: Usa duas chaves que não se relacionam. 
        * Problema: É muito intensivo computacionalmente e lento.
* **Hash Funciton**:
    * Ter a encriptacao, e apenas conseguimos verificar se o texto é igual, não sendo uma opção inicial de decifrar a frase.

### https://www.cryptool.org/en/cto/ - para aprender cryptologia

### PGP - Pretty Good Privacy
* A versão original foi vendida
* No linux chama-se GNUPG
* Para windows GPG4win

* O professor recomenda o GNUPG
* Mais de mercado podemos usar o da simon tech
* Se estivermos dependentes do windows usar o GPG4win

* Dividir o grupo em 2, um vai usar uma lógica e outra parte outra lógica

* O professor recomenda que uma parte usa o GNUPG, enquanto a outra parte usa a tech mais comercial (simon)

* Thunder Bird para usar como email

## Como funciona
Usa o algo simetrico

* Como a chave assimetrica é muito pesado, o pgp cifra a seed e **não** a mensagem, usando o a chave pública da outra pessoa (que temos no nosso keyring).
* Depois a pessoa decifra a mensagem com a sua chave privada, para extrair a chave de sessão e conseguimos retirar a mensagem.

* ***Problema***: Qualquer pessoa pode escrever uma mensagem, iludir a remetente de mensagens de email para enganar o sistema para parecer que outra pessoa é que enviou o email. **NÃO TEMOS GARANTIA DE AUTENTICIDADE DO REMETENTE**
* Como podemos resolver: Obrigar o emissor a usar a sua propria chave privada

* Usar a assinatura digital: 
    * Garante a autenticidade
    * Garante a Integridade da mensagem
    * Não repudio (pode se bom ou mau dependendo da forma como vemos)

* Podemos usar a funcao hash em cima do texto, é uma coisa pequena que serve para o emissor usar a sua chave privada.
* O hash temos sempre o mesmo tamanho

### Como funciona a Assinatura digital
* Do texto, fazemos hash e temos um Message Digest, e ao aplicar 

Uma ssinatura é uma hash com uma chave privada para conseguir verificara autenticade, integridade e não repudio.

* A mensagem é enviada de forma, da mensagem e depois a assinatura, se alguém vir não consegue chegar a qual é a chave privada

* Se o remetente não conseguir obter o mesom hash, é porque o remetente nao é aquele ou a mensagem foi alterada

Instalar as ferramentas, instaladas as chaves 