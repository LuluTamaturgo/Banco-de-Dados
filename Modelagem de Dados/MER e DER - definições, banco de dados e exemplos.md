# MER e DER: definições, banco de dados e exemplos
---

Muitas pessoas confundem MER (Modelo Entidade Relacionamento) com DER (Diagrama Entidade-Relacionamento), mas a diferença é simples: **um é o conceito** e o **outro é o desenho**.

## MER vs. DER: Do Conceito ao Desenho

**1. Definições**
* MER (Modelo Entidade-Relacionamento): 
	* É a parte abstrata. É o modelo conceitual que descreve os objetos do mundo real (entidades), suas características (atributos) e como se conectam (relacionamentos). É a "teoria" dos dados.

* DER (Diagrama Entidade-Relacionamento): 
	* É a parte visual. É a representação gráfica do MER usando símbolos (retângulos, losangos e elipses). É o "mapa" que os desenvolvedores olham para entender a estrutura.
	
**2. No Banco de Dados**
A dupla MER/DER serve como o blueprint (planta baixa). Sem eles, o banco de dados corre o risco de ter dados duplicados ou falta de integridade. Eles garantem que a estrutura lógica suporte todas as regras de negócio antes de qualquer linha de código SQL ser escrita.

**3. Exemplos Práticos**
Imagine um sistema de **E-commerce:**
	* Entidades: Cliente, Pedido, Produto.
	* Atributos: Nome do Cliente, Data do Pedido, Preço do Produto.
	* Relacionamento: Um Cliente faz um Pedido; Um Pedido contém Produtos.
	
| Termo | O que é? | Representação |
| :--- | :--- | :--- |
| **MER** | Modelo Conceitual | Descrição textual e lógica das regras. |
| **DER** | Diagrama Visual | Desenho técnico com símbolos e ligações. |

---

## O que são entidades?

Uma entidade é qualquer "coisa" (física ou abstrata) sobre a qual você precisa guardar informações. Elas são classificadas pela sua autonomia:

**1. Entidade Forte**
É independente. Ela existe por si só e possui um identificador próprio (chave primária).

* Exemplo: CLIENTE. Um cliente existe no sistema independente de qualquer outra coisa.

**2. Entidade Fraca**
Não tem vida própria. Ela só faz sentido se estiver conectada a uma entidade forte. Se a entidade forte for deletada, a fraca geralmente perde o sentido.

* Exemplo: DEPENDENTE. Um dependente só existe no banco de dados se estiver vinculado a um FUNCIONÁRIO (entidade forte).

**3. Entidade Associativa**
Surge para resolver um relacionamento complexo (muitos-para-muitos). Ela "transforma" um relacionamento em uma entidade para que possamos guardar dados sobre essa união.

* Exemplo: MATRÍCULA. Ela une ALUNO e DISCIPLINA. Sozinha ela não existe, mas é necessária para registrar informações como a "Nota" ou "Frequência" daquela união específica.

| Tipo de Entidade | Dependência | Exemplo Típico |
| :--- | :--- | :--- |
| **Forte** | Independente | Carro, Pessoa, Produto |
| **Fraca** | Depende de uma Forte | Parcela (de um Empréstimo) |
| **Associativa** | Resolve N:N | Item_Pedido (une Produto e Pedido) |

---

## O que são Atributos?

Atributos são as propriedades que definem uma entidade. Eles variam conforme a complexidade da informação que carregam:

**1. Atributo Simples (Atômico)**
É a menor unidade de dado. Não faz sentido dividi-lo.

* Exemplo: CPF ou RG.

**2. Atributo Composto**
Pode ser subdividido em partes menores que também são atributos.

* Exemplo: Endereço (que se divide em Rua, Número, Bairro e Cidade).

**3. Atributo Multivalorado**
Aquele que pode aceitar mais de um valor para a mesma entidade.

* Exemplo: Telefone (uma pessoa pode ter celular, fixo e comercial).

**4. Atributo Derivado**
Não precisa ser armazenado diretamente, pois pode ser calculado a partir de outro dado.

* Exemplo: Idade (derivada da Data de Nascimento).

**5. Atributo Chave (Identificador)**
É o "RG" do registro. Ele garante que uma entidade seja única e não se repita.

* Exemplo: ID_Cliente ou Código_Produto.


| Tipo de Atributo | Característica | Exemplo |
| :--- | :--- | :--- |
| **Simples** | Indivisível (Atômico) | CPF |
| **Composto** | Composto por subpartes | Endereço |
| **Multivalorado** | Aceita múltiplos valores | Telefone, E-mail |
| **Derivado** | Calculado de outro dado | Idade |
| **Chave** | Identificador único | ID, Código, Matrícula |

---

## relacionamentos

Eles explicam como as entidades interagem entre si, geralmente representados por verbos que ditam as regras de negócio.

A forma como essas associações ocorrem é chamada de Cardinalidade. Aqui está o resumo dos três tipos:

### Tipos de Relacionamentos (Cardinalidade)

**1. Um para Um (1:1)**
Cada registro de uma tabela está ligado a apenas um registro da outra.

* Exemplo: PESSOA e CPF. Uma pessoa possui apenas um CPF, e um CPF pertence a apenas uma pessoa.

**2. Um para Muitos (1:N)**
Um registro da Entidade A pode se relacionar com vários da Entidade B, mas o contrário não é verdade.

* Exemplo: CLIENTE e PEDIDO. Um cliente pode fazer vários pedidos, mas cada pedido pertence a apenas um único cliente.

**3. Muitos para Muitos (N:N)**
Vários registros da Entidade A podem se relacionar com vários da Entidade B.

* Exemplo: ALUNO e DISCIPLINA. Um aluno pode se matricular em várias disciplinas, e uma disciplina pode ter vários alunos matriculados.

* Nota: No modelo lógico, esse relacionamento geralmente gera uma Entidade Associativa (tabela intermediária).

| Tipo | Sigla | Descrição | Exemplo Prático |
| :--- | :--- | :--- | :--- |
| **Um para Um** | 1:1 | Associação exclusiva entre dois registros. | Pessoa ↔ CPF |
| **Um para Muitos** | 1:N | Um "pai" para vários "filhos". | Departamento ↔ Funcionários |
| **Muitos para Muitos** | N:N | Múltiplas conexões em ambos os lados. | Livro ↔ Autor |