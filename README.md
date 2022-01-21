# PERGUNTA5
--Ctraete de table Alunos
CREATE table Alunos(
  ID INT,
  NOME VARCHAR (20),
  VALOR INT
  );
 
 --Create de table Notas
 CREATE TABLE Notas(
   NOTA INT (2),
   VALOR_MIN INT (2),
   VALOR_MAX INT (3)
   );

-- Insert a table Alunos
   INSERT INTO Alunos VALUES
   (1,'JULIA',81);
   INSERT INTO Alunos VALUES
   (2,'CAROL',68);
   INSERT INTO Alunos VALUES
   (3,'MARIA',99);
   INSERT INTO Alunos VALUES
   (4,'ANDREINA',78);
   INSERT INTO Alunos VALUES
   (5,'JAQUELINE',63);
   INSERT INTO Alunos VALUES
   (6,'MARCELA',88);

--Consulta table Alunos
  SELECT * 
  FROM Alunos;
  
  -- Insert a table Notas
  INSERT INTO Notas VALUES
  (1,0,9);
  INSERT INTO Notas VALUES
  (2,10,19);
  INSERT INTO Notas VALUES
  (3,20,29);
  INSERT INTO Notas VALUES
  (4,30,39);
  INSERT INTO Notas VALUES
  (5,40,49);
  INSERT INTO Notas VALUES
  (6,50,59);
  INSERT INTO Notas VALUES
  (7,60,69);
  INSERT INTO Notas VALUES
  (8,70,79);
  INSERT INTO Notas VALUES
  (9,80,89);
  INSERT INTO Notas VALUES
  (10,90,100);
  
  --Consulta a table Noatas
  SELECT * 
  FROM Notas;
  
  --Consulta para respusta num 5
  SELECT case n.nota 
  WHEN 7 THEN a.NOME = NULL
  ELSE a.nome
  end nome,
  n.NOTA,
  a.valor
  FROM Alunos a, Notas n
  WHERE a.valor <= n.valor_max
  and   a.valor >= n.valor_min
  order by a.VALOR DESC, a.nome ASC;
