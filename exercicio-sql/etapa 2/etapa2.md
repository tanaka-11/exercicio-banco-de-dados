# Recriando a tabela professores:

```sql
CREATE TABLE professores (
    id TINYINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nomeProf VARCHAR(50) NOT NULL,
    materia ENUM('design', 'desenvolvimento', 'infra') NOT NULL,
    curso_id TINYINT, NOT NULL
);
```
 

# Cadastrando 5 cursos:

```sql
INSERT INTO cursos (
    nomeCurso, cargaHoraria, professor_id
) VALUES (
    'Front-End',
    40,
    null
),
(
    'Back-End',
    80,
    null
),
(
    'UX/UI design',
    30,
    null
),
(
    'Figma',
    10,
    null
),
(
    'Redes de computadores',
    100,
    null
);
```

# Cadastrando 5 professores:

```sql
INSERT INTO professores (
    nomeProf, materia, curso_id
) VALUES (
    'Jon Oliva',
    'infra',
    5
),
(
    'Lemmy Kilmister',
    'design',
    4
),
(
    'Neil Peart',
    'design',
    3
),
(
    'Ozzy Osbourne',
    'desenvolvimento',
    2
),
(
    'David Gilmour',
    'desenvolvimento',
    1
);
```

# Atualizando dados do campo professor_id

```sql
-- Professor Front-End "Daivid Gilmour"
UPDATE cursos SET professor_id = 5 WHERE id = 1;

-- Professor Back-End "Ozzy Osbourne"
UPDATE cursos SET professor_id = 4 WHERE id = 2;

-- Professor de UX/UI design "Neil Peart"
UPDATE cursos SET professor_id = 3 WHERE id = 3;

-- Professor de Figma "Lemmy Kilmister"
UPDATE cursos SET professor_id = 2 WHERE id = 4;

-- Professor de Redes de Computadores "Jon Oliva"
UPDATE cursos SET professor_id = 1 WHERE id = 5;

```

# Cadastrando 10 alunos, suas notas e data de nascimento
```sql
INSERT INTO alunos (
    nomeAluno, nascimento, nota1, nota2, curso_id
) VALUES (
    'Marina Tanaka',
    '2001/11/10',
    09.50,
    07.50,
    3
),
(
    'Beatriz Kogici',
    '2004/03/12',
    07.50,
    08.00,
    1
),
(
    'Luis Fernando',
    '2001/07/27',
    05.00,
    05.00,
    4
),
(
    'Mariana Koki',
    '2001/11/29',
    08.00,
    07.00,
    2
),
(
    'Analice Ameilda',
    '2001/10/27',
    10.00,
    10.00,
    3
),
(
    'Isabella Rossi',
    '2000/05/07',
    10.00,
    03.50,
    5
),
(
    'Roberto Garcia',
    '1980/06/05',
    08.50,
    02.50,
    5
),
(
    'Eliane Tanaka',
    '1982/05/05',
    10.00,
    10.00,
    2
),
(
    'Cleiton Rogerio',
    '2006/10/05',
    02.50,
    01.50,
    1
),
(
    'Marcos Yan',
    '1999/04/12',
    00.00,
    05.00,
    1
);

```