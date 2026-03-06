# 🧠 ESTRUTURA FIXA DO TREINO (USE TODO DIA)

### **⏱️ Tempo diário: 30–40 minutos**

Todo dia você fará o mesmo ritual, só muda o cenário.

---

## 🔹 RITUAL DIÁRIO (OBRIGATÓRIO)

### PASSO 1 — Leitura analítica (5 min)
* Leia o cenário e sublinhe mentalmente:

	* Substantivos → possíveis entidades
	* Verbos → possíveis relacionamentos
	* Características → atributos
	
### PASSO 2 — Lista de entidades (5 min)

* Liste:

	* Entidades fortes
	* Possíveis entidades fracas
	* Possível entidade associativa

Não desenhe ainda.

### PASSO 3 — Definição de atributos (10 min)

Para cada entidade:

* PK obrigatória
* 3–6 atributos
* Marque:
	* (O) opcional
	* (M) multivalorado
	* (U) chave alternativa
	
### PASSO 4 — Relacionamentos e cardinalidade (10 min)

Para cada relacionamento:

* Nome
* Cardinalidade
* Identifique se gera entidade associativa

### PASSO 5 — Generalização / Especialização (5 min)

Pergunte:

* Existe uma entidade genérica com variações?

Se sim:

* Defina supertipo e subtipos
* Marque se é parcial/total e disjunta/sobreposta

### PASSO 6 — Conversão lógica (5 min)

Agora sim:

* Defina PK
* Defina FK
* Defina AK

---

## 🔍 CHECKLIST FINAL (TODO DIA)

Antes de encerrar, confirme:

 * Toda entidade tem PK ( )

 * Toda FK vem de relacionamento ( )

 * Toda N:N virou associativa ( )

 * Multivalorado não ficou como atributo simples ( )

 * Generalização faz sentido ( )

 * Não misture conceitual com lógico ( )
 
---
 
### 📅 DESAFIO DE 30 DIAS (PROGRESSIVO)

Cada dia tem:

1. Cenário

2. O que construir

3. Como construir (guia mental)

---

## 🟢 SEMANA 1 — FUNDAMENTOS (Dias 1–7)

### Dia 1 — Biblioteca

**Cenário: livros, autores, editoras.**

Construa:

* Entidades

* Relacionamentos

* PK e AK

Guia:

* Livro ↔ Autor é N:N → associativa

* ISBN é AK

### Dia 2 — Clínica

**Pacientes, médicos, consultas.**

Construa:

* Entidade associativa Consulta

* Cardinalidade correta

Guia:

* Consulta identifica Médico + Paciente + data

### Dia 3 — Escola

**Alunos, cursos, matrículas.**

Construa:

* Matrícula como associativa

* Atributos próprios

### Dia 4 — E-commerce

**Clientes, pedidos, produtos.** 

Guia:

* Pedido_Produto associativa

* Quantidade como atributo da associativa

### Dia 5 — Empresa

**Funcionários, departamentos.**

Guia:

* Funcionário pertence a um departamento

* CPF como AK

### Dia 6 — Hotel

**Hóspedes, quartos, reservas.**

Guia:

* Reserva como associativa

* Datas como atributos

### Dia 7 — Revisão

**Refaça um modelo da semana sem olhar.**

---

## 🟡 SEMANA 2 — GENERALIZAÇÃO E FRACAS (Dias 8–14)

### Dia 8 — Sistema bancário

**Conta, cliente, conta corrente, conta poupança.**

Guia:

* Generalização total

* Atributos específicos por subtipo

### Dia 9 — Loja física

**Pessoa, cliente, fornecedor.**

Guia:

* Generalização parcial e sobreposta

### Dia 10 — Saúde

**Pessoa → Médico / Paciente**

Guia:

* Especialização sobreposta

### Dia 11 — Educação

**Curso → graduação / pós**

### Dia 12 — Transporte

**Veículo → carro / moto / caminhão**

### Dia 13 — Revisão

**Explique por escrito cada generalização**

### Dia 14 — Modelo livre

**Você escolhe o domínio.**

---

## 🔵 SEMANA 3 — OTIMIZAÇÃO LÓGICA (Dias 15–21)

### Dia 15 — Sistema financeiro

**Contas, transações, categorias.**

Guia:

* Transação depende de Conta

### Dia 16 — RH

**Funcionário, cargo, histórico de cargos.**

Guia:

* Histórico como entidade fraca

### Dia 17 — Universidade

**Professor, disciplina, oferta.**

Guia:

* Oferta como associativa temporal

### Dia 18 — Streaming

**Usuário, plano, assinatura.**

### Dia 19 — Marketplace

**Vendedor, produto, anúncio.**

### Dia 20 — Revisão crítica

Encontre:

* Entidades fracas

* Chaves compostas

### Dia 21 — Refatoração

**Simplifique um modelo antigo.**

---

## 🔴 SEMANA 4 — CONVERSÃO E MATURIDADE (Dias 22–30)

### Dia 22 — Converta modelo ER → Relacional

### Dia 23 — Adicione AK e índices (conceito)

### Dia 24 — Modele pensando em consulta

### Dia 25 — Modele pensando em escrita

### Dia 26 — Modele pensando em histórico

### Dia 27 — Modele pensando em auditoria

### Dia 28 — Modelo completo (livre)

### Dia 29 — Autoavaliação técnica

**Explique decisões.**

### Dia 30 — Modelo final

**Refaça o melhor modelo do mês do zero.**