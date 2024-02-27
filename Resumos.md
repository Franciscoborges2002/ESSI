# Ficheiro para termos chaves

## 1. Diferença entre Ameaças, Ataques e Vulnerabilidades?

- Ameaças:
```
        Qualquer fator ou ação que possa interferir e causar danos à integridade, confidencialidade, autenticidade e disponibilidade de dados e informações.
```

* O que as ameaças impendem sobre recursos críticos
    * Availability (and Utility) - **Interruption** (or disruption)
        * Detruição, dano ou contaminação
        * Recusar ou tornar demorado o acesso
        * Deslocação ou ofuscação
    * Integrity (and Authenticity) - **Mofification/Fabrication** (or deception and usurpation)
        * Inserir ou produzir dados
        * Repor, remover, separar ou re organizar
        * Representar ou codificação
        * Repudio
    * Confidentiality (and Possession) - **Interception** (or disclosure)
        * Cópia ilicita, observação, monitorização ou inferencia
        * Transferencia indesejada de controlos de custódia
        * Disclosure


- Ataques:
```
        Uma ataque surge quando existe um método, oportunidade e um motivo
```

. **Método**: conhecimento, habilidades e ferramentas para explorar vulnerabilidades.

. **Oportunidade**: tempo e condição para aceder

. **Motivo**: Uma razão para levar a cabo o ataque

- Vulnerabilidades:
```
        asdaasd
```


*Hierarquia*:
* Uma ameça gera uma Ataque;
* Ataques exploram Vulnerabilidades;
* Vulnerabilidades aumentam riscos
* Vulnerabilidades aumentam as Ameaças.
* Usamos controlos para conseguir proteger/medir/prevenir deste três fatores;

## 2. O que são controlos de segurança?

Controlos de segurança são **políticas**, **procedimentos**, **guias**, boas práticas, **dispositivos de software e hardware**.

Podem ser orientados a cada uma das ciglas do CIA (Confidentiality, Intigrity and Availability).

## 3. Controlo de Acesso

Inclui a autenticação, autorização e accounting/auditing (AAA), mas normalmente estes não são completamente implementados;

Para controlar as condições de acesso a um **assunto** a um **objeto** podemos implementar primeramente a autorização. Existindo dois tipos de implementação:
* Baseado na Matrix de acesso: Processo normalmente gerido pelo sistema operativo -> **Modelo centralizado**.
* Baseado na atribuição de capacidades: Processo normalmente gerido por um servidor centrar -> **Modelo distribuido**.

#### Principais políticas:
* **DAC** (Discretionary Access Control):
 * A política de acesso de um objeto é *definida pelo dono*. 
* **MAC** (Mandatory Access Control):
 * A política de acesso de um objeto é *definida pelo sistema*, *need-to-know principle*.
* **RBAC** (Role based Access Control):
 * A política de acesso de um objeto é *definida pelo sistema*. Mas ao invés de ter permissões associadas com o o nível de segurança de um assunto, existem permissões associadas com **papeis de assuntos** do sistema.
* **ABAC** (Attribute based Access Control):
 * Baseado nos atributos dos utilizadores, é um standard deste janeiro de 2023.

### Modelos de segunraça de controlos de segurança

## 4. Autenticação

## 5. Autenticação de utilizador