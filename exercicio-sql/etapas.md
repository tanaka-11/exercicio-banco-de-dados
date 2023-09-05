# Exercícios de Banco de Dados - Etapa 1

## Modelagem Lógica e Física

### A. Modelagem Lógica

#### Usando o MySQL Workbench, faça a modelagem lógica de três entidades (tabelas): **cursos**, **professores** e **alunos**.

- A entidade **cursos** deve conter os seguintes campos:

    - Id (inteiro pequeno), não nulo, com chave primária e auto incrementado
    - Título (string com tamanho 30) não nulo
    - Carga horária (inteiro pequeno), não nulo
    - Id do Professor (inteiro pequeno) nulo

- A entidade **professores** deve conter os seguintes campos:    

    - Id (inteiro pequeno), não nulo, com chave primária e auto incrementado
    - Nome (string com tamanho 50) não nulo
    - Área de atuação (uma lista de dados contendo somente as opções *design*, *desenvolvimento*, *infra*) não nulo
    - Id do Curso (inteiro pequeno) não nulo

- A entidade **alunos** deve conter os seguintes campos:    

    - Id (inteiro pequeno), não nulo, com chave primária e auto incrementado
    - Nome (string com tamanho 50) não nulo
    - Data de nascimento (Data) não nulo
    - Primeira nota (decimal tamanho total 4, 2 dígitos depois da vírgula) não nulo
    - Segunda nota (decimal tamanho total 4, 2 dígitos depois da vírgula) não nulo
    - Id do Curso (inteiro pequeno) não nulo

  
#### Crie os relacionamentos de acordo com a cardinalidade indicada a seguir:

- **1 curso tem vários alunos**, portanto será usada a cardinalidade **1:N**. 

*Isso criará um campo chamado curso_id na tabela de alunos. Dica: clique primeiro em alunos e depois em cursos.*

- **1 professor leciona somente 1 curso**, portanto será usada a cardinalidade **1:1**. 

*Isso criará um campo chamado professor_id na tabela cursos. Dica: clique primeiro em cursos e depois em professores.*

- **1 curso é lecionado somente por 1 professor**, portanto será usada a cardinalidade **1:1**. 

*Isso criará um campo chamado curso_id na tabela professores. Dica: clique primeiro em professores e depois em cursos.*

---

### B. Modelagem Física

- Crie um banco de dados chamado **tecinternet_escola_seunome**
- Usando o phpMyAdmin (via interface e/ou códigos SQL), crie a modelagem física de acordo com o que foi feito na modelagem lógica.

# Exercícios de Banco de Dados - Etapa 2

## CRUD - Cadastro geral

### Cadastre pelo menos 5 cursos: 

1. Front-End, carga horária 40h
2. Back-End, carga horária 80h
3. UX/UI Design, carga horária 30h
4. Figma, carga horária 10h
5. Redes de Computadores, carga horária 100h

**Atenção:** por enquanto, deixe o campo professor_id como nulo

---

### Cadastre pelo menos 5 professores: 

1. Jon Oliva, área infra
2. Lemmy Kilmister, área design
3. Neil Peart, área design
4. Ozzy Osbourne, área desenvolvimento
5. David Gilmour, área desenvolvimento

**Atenção:** durante o cadastro dos professores, associe cada professor a um curso na ordem contrária dos registros. 

Exemplos: 

- O primeiro professor (Jon Oliva, infra) será atribuido ao último curso (Redes de Computadores)
- O segundo professor (Lemmy, design) será atribuido ao penúltimo curso (Figma)

---

### Atualize os dados do campo professor_id da tabela cursos, associando cada curso ao seu professor correspondente.

---

### Cadastre pelo menos 10 alunos distribuidos aleatoriamente dentre os cursos, com datas de nascimento variadas, notas baixas e altas (sempre entre 0.00 e 10.00).

---

# Exercícios de Banco de Dados - Etapa 3

## CRUD - Consultas

***Atenção**: todos os comandos bem-sucedidos devem ser documentados e colocados no seu repositório do exercício.*

### 1) Faça uma consulta que mostre os alunos que nasceram antes do ano 2009

---

### 2) Faça uma consulta que calcule a média das notas de cada aluno e as mostre com duas casas decimais.

---

### 3) Faça uma consulta que calcule o limite de faltas de cada curso de acordo com a carga horária. Considere o limite como 25% da carga horária. Classifique em ordem crescente pelo título do curso.

---

### 4) Faça uma consulta que mostre os nomes dos professores que são somente da área "desenvolvimento".

---

### 5) Faça uma consulta que mostre a quantidade de professores que cada área ("design", "infra", "desenvolvimento") possui.

---

### 6) Faça uma consulta que mostre o nome dos alunos, o título e a carga horária dos cursos que fazem.

---

### 7) Faça uma consulta que mostre o nome dos professores e o título do curso que lecionam. Classifique pelo nome do professor.

---

### 8) Faça uma consulta que mostre o nome dos alunos, o título dos cursos que fazem, e o professor de cada curso.

---

### 9) Faça uma consulta que mostre a quantidade de alunos que cada curso possui. Classifique os resultados em ordem descrecente de acordo com a quantidade de alunos.

---

### 10) Faça uma consulta que mostre o nome dos alunos, suas notas, médias, e o título dos cursos que fazem. Devem ser considerados somente os alunos de Front-End e Back-End. Mostre os resultados classificados pelo nome do aluno.

---

### 11) Faça uma consulta que altere o nome do curso de Figma para Adobe XD e sua carga horária de 10 para 15.

---

### 12) Faça uma consulta que exclua um aluno do curso de Redes de Computadores e um aluno do curso de UX/UI.

---

### 13) Faça uma consulta que mostre a lista de alunos atualizada e o título dos cursos que fazem, classificados pelo nome do aluno.

---

## DESAFIOS

1) Criar uma consulta que calcule a idade do aluno
2) Criar uma consulta que calcule a média das notas de cada aluno e mostre somente os alunos que tiveram a média **maior ou igual a 7**.
3) Criar uma consulta que calcule a média das notas de cada aluno e mostre somente os alunos que tiveram a média **menor que 7**.
4) Criar uma consulta que mostre a quantidade de alunos com média **maior ou igual a 7**.




