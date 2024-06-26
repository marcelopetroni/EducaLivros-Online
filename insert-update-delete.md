* ### Nesse arquivo, teremos todos os insert, delete e updates que utilizamos para testar o nosso banco de dados.

*obs: Primeiro coloque todos as inserções nas tabelas para não cair em
nenhuma restrição.*

# ----- INSERT ---------


### Inserção de usuários de exemplo
```sql
INSERT INTO Usuario (ID_Usuario, Telefone, Email, Endereco, Data_de_Nascimento, CPF, Nome, Idade)
VALUES (1, '123456789', 'exemplo1@email.com', 'Endereço 1', '1990-01-01', '12345678900', 'Usuário 1', 30);

INSERT INTO Usuario (ID_Usuario, Telefone, Email, Endereco, Data_de_Nascimento, CPF, Nome, Idade)
VALUES (2, '987654321', 'exemplo2@email.com', 'Endereço 2', '1995-05-05', '98765432100', 'Usuário 2', 25);

INSERT INTO Usuario (ID_Usuario, Telefone, Email, Endereco, Data_de_Nascimento, CPF, Nome, Idade)
VALUES (3, '543216789', 'exemplo3@email.com', 'Endereço 3', '1998-10-10', '54321678900', 'Usuário 3', 22);

INSERT INTO Usuario (ID_Usuario, Telefone, Email, Endereco, Data_de_Nascimento, CPF, Nome, Idade)
VALUES (4, '987123456', 'exemplo4@email.com', 'Endereço 4', '2000-03-15', '98712345600', 'Usuário 4', 21);

INSERT INTO Usuario (ID_Usuario, Telefone, Email, Endereco, Data_de_Nascimento, CPF, Nome, Idade)
VALUES (5, '654987321', 'exemplo5@email.com', 'Endereço 5', '1993-08-20', '65498732100', 'Usuário 5', 28);
```


### Inserir valores na tabela editora
```sql
INSERT INTO Editora (Nome_Editora, Telefone, Email)
VALUES
('Companhia das Letras', '+55 11 9999-9999', 'contato@companhiadasletras.com.br'),
('Penguin Random House', '+1 212-782-9000', 'info@penguinrandomhouse.com'),
('HarperCollins', '+1 212-207-7000', 'webmaster@harpercollins.com');
```

### Inserir valores na tabela Usuario
```sql
INSERT INTO Usuario (ID_Usuario, Telefone, Email, Endereco, Data_de_Nascimento, CPF, Nome, Idade)
VALUES
(1, '+55 11 1234-5678', 'fulano@gmail.com', 'Rua A, 123', '1990-01-15', '123.456.789-00', 'Fulano de Tal', 34),
(2, '+55 11 9876-5432', 'beltrano@gmail.com', 'Rua B, 456', '1985-05-20', '987.654.321-00', 'Beltrano da Silva', 39),
(3, '+55 11 1111-2222', 'ciclano@gmail.com', 'Rua C, 789', '2000-12-10', '111.222.333-00', 'Ciclano Pereira', 24);
```

### Inserir valores na tabela Livro
```sql
INSERT INTO Livro (Titulo, ID_Livro, Sessao, Numeros_De_Pags, Autor, Ano, Genero, Numero, fk_Emprestimo_ID_Emprestimo, fk_Editora_Nome_Editora)
VALUES
('Dom Casmurro', 1, 'Ficção', 256, 'Machado de Assis', 1899, 'Romance', 101, NULL, 'Companhia das Letras'),
('Os Miseráveis', 2, 'Ficção', 1488, 'Victor Hugo', 1862, 'Romance', 102, NULL, 'Penguin Random House'),
('1984', 3, 'Ficção', 328, 'George Orwell', 1949, 'Ficção Científica', 103, NULL, 'HarperCollins');
```

### Inserir valores na tabela Emprestimo
```sql
INSERT INTO Emprestimo (ID_Emprestimo, ID_Livro, ID_Usuario, Data_De_Emprestimo, Data_De_Devolucao_Efetiva, Data_De_Devolucao, Disponibilidade)
VALUES
(101, 1, 1, '2024-04-20', '2024-05-10', NULL, 'Disponível'),
(102, 2, 2, '2024-04-15', NULL, '2024-05-15', 'Indisponível'),
(103, 3, 3, '2024-04-10', NULL, '2024-05-10', 'Indisponível');
```


### Inserir valores na tabela de Alunos
```sql
INSERT INTO Aluno_Matricula (Mensalidade, RG, Notas, fk_Usuario_ID_Usuario, Numero, Materias_Matriculadas, Coeficiente_Rendimento, Historico_Escolar)
VALUES (1000.00, '123456789', 8.5, 1, 1, 'Matemática, Física', 8.5, 'Excelente aluno');

INSERT INTO Aluno_Matricula (Mensalidade, RG, Notas, fk_Usuario_ID_Usuario, Numero, Materias_Matriculadas, Coeficiente_Rendimento, Historico_Escolar)
VALUES (1000.00, '987654321', 7.2, 2, 1, 'História, Geografia', 7.2, 'Bom aluno');

INSERT INTO Aluno_Matricula (Mensalidade, RG, Notas, fk_Usuario_ID_Usuario, Numero, Materias_Matriculadas, Coeficiente_Rendimento, Historico_Escolar)
VALUES (1000.00, '543216789', 9.0, 3, 1, 'Português, Literatura', 9.0, 'Ótimo aluno');

INSERT INTO Aluno_Matricula (Mensalidade, RG, Notas, fk_Usuario_ID_Usuario, Numero, Materias_Matriculadas, Coeficiente_Rendimento, Historico_Escolar)
VALUES (1000.00, '987123456', 6.8, 4, 1, 'Química, Biologia', 6.8, 'Aluno mediano');

INSERT INTO Aluno_Matricula (Mensalidade, RG, Notas, fk_Usuario_ID_Usuario, Numero, Materias_Matriculadas, Coeficiente_Rendimento, Historico_Escolar)
VALUES (1000.00, '654987321', 9.5, 5, 1, 'Inglês, Espanhol', 9.5, 'Excelente aluno');
```


### Inserir valores na tabela de Bibliotecario
```sql
INSERT INTO Bibliotecario (Nome_Funcionario, ID_Funcao_Biblioteca)
VALUES ('João Silva', 1),
       ('Maria Souza', 2),
       ('Carlos Ferreira', 3);
```

### Inserir valores na tabela de Entregador
```sql
INSERT INTO Entregador (ID_Motoboy, Valor, Endereco)
VALUES (101, 50.00, 'Rua A, 123'),
       (102, 55.00, 'Rua B, 456'),
       (103, 60.00, 'Rua C, 789');
```

### Inserir valores na tabela de Disciplina
```sql
INSERT INTO Disciplina (Codigo, Descricao, Nome, Horario, Carga_Horaria)
VALUES (1, 'Matemática', 'Matemática Básica', '08:00:00', 60),
       (2, 'História', 'História do Brasil', '10:00:00', 60),
       (3, 'Física', 'Física Moderna', '14:00:00', 60);
```

### Inserir valores na tabela de Aula
```sql
INSERT INTO Aula (Horario, Presenca_Alunos, Codigo_Turma, fk_Disciplina_Codigo)
VALUES ('08:00:00', 'Presente', 101, 1),
       ('10:00:00', 'Presente', 102, 2),
       ('14:00:00', 'Ausente', 103, 3);
```

### Inserir valores na tabela de EAD
```sql
INSERT INTO EAD (Plataforma, FK_Aula_Codigo_Turma)
VALUES ('Google Meet', 101),
       ('Zoom', 102),
       ('Microsoft Teams', 103);
```

### Inserir valores na tabela de Presencial_Escola
```sql
INSERT INTO Presencial_Escola (Local, fk_Aula_Codigo_Turma)
VALUES ('Sala 101', 101),
       ('Sala 201', 102),
       ('Sala 301', 103);
```

# --- UPDATE ---

### Update em Editora
```sql
UPDATE Editora SET Telefone = '+55 11 9876-5432' WHERE Nome_Editora = 'Companhia das Letras';

UPDATE Editora SET Email = 'info@harpercollins.com' WHERE Nome_Editora = 'HarperCollins';
```
### Update em Usuario
```sql
UPDATE Usuario SET Telefone = '+55 11 1111-2222', Email = 'novobeltrano@gmail.com' WHERE ID_Usuario = 2;
```
### Update em Emprestimo
```sql
UPDATE Emprestimo SET Data_De_Emprestimo = '2024-04-24' WHERE ID_Livro = 2;

UPDATE Emprestimo SET   Data_De_Devolucao = '2024-05-24' WHERE ID_Livro = 2;

UPDATE Emprestimo SET  Data_De_Devolucao_Efetiva = '2024-06-24' WHERE ID_Livro = 2;
```

# ----- DELETE ----

### Delete um usuário
```sql
DELETE FROM Usuario WHERE ID_Usuario = 3;
```
### Delete um livro
```sql
DELETE FROM Livro WHERE ID_Livro = 2;
```

### Delete um Bibliotecario
```sql
DELETE FROM Bibliotecario WHERE ID_Funcao_Biblioteca = 1;

DELETE FROM Bibliotecario WHERE Nome_Funcionario = 'João Silva';
```


# ----- Restriçoes -----

#### 1 - Chave Primária (Primary Key):
Em cada tabela, há uma coluna designada como chave primária, identificada pela declaração PRIMARY KEY. Essa restrição garante que cada registro na tabela tenha um valor único nessa coluna. Por exemplo, na tabela Livro, a coluna ID_Livro é a chave primária, garantindo que cada livro tenha um ID único.

#### 2 - Chave Estrangeira (Foreign Key):

As chaves estrangeiras são definidas nas tabelas para estabelecer relacionamentos entre elas. Por exemplo, na tabela Livro, existem duas chaves estrangeiras: fk_Emprestimo_ID_Emprestimo, que faz referência à tabela Emprestimo, e fk_Editora_Nome_Editora, que faz referência à tabela Editora. Essas chaves estrangeiras garantem a integridade referencial entre as tabelas.

#### 3 - Restrição ON DELETE:

As restrições ON DELETE especificam o que acontece com os registros relacionados quando um registro primário é excluído. Por exemplo, na tabela Livro, a restrição ON DELETE RESTRICT na chave estrangeira fk_Emprestimo_ID_Emprestimo impede que um livro seja excluído se estiver associado a um empréstimo. Outro exemplo, é tentar apagar a editora de um livro

Já a restrição ON DELETE CASCADE na tabela Online faz com que as entradas relacionadas sejam excluídas quando um empréstimo é excluído.

#### 4 - Restrição ON UPDATE:
Embora não esteja explicitamente definida em seu modelo, a restrição ON UPDATE determinaria o que acontece com as entradas relacionadas quando uma chave primária é atualizada. Por exemplo, você pode especificar que os registros relacionados também devem ser atualizados quando a chave primária é atualizada.

