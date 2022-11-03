# Projeto Graph Database
###### Disciplina Tópicos Avançados em Bancos de Dados - Ciência da Computação FEI

_O passo a passo a seguir mostra a criação de nós e relacionamentos entre professora, aluna, disciplina cursada e curso de graduação através de um Banco de Dados Orientado a Grafos (GDB)._

<br>

### Como criar um GDB simples usando Neo4j:<br><br>

1. Download Neo4j pelo [link](https://neo4j.com/download-center/)

2. Clique em **New** para criar um novo projeto 

3. Clique em **Add** > **Local DBMS** > **Start**

4. Clique em **Graph Apps** > **Neo4j Browser open**
> em neo4j$

5. Crie nó _Pessoa_: `CREATE (Professora:Pessoa {nome:'Professora'})` `CREATE (Aluna:Pessoa {nome:'Aluna'})`

6. Verifique nomes de Pessoa: `MATCH (p:Pessoa) return p.nome`
CREATE (BancoDeDados:Disciplina {nome_disc:'Banco de Dados'})

7. Crie nó _Disciplina_: `CREATE (BancoDeDados:Disciplina {nome_disc:'Banco de Dados'})`

8. Crie nó _Projeto_: `CREATE (TCC:Projeto {nome_proj:'TCC'})`

9. Crie nó _Curso_: `CREATE (CienciaDaComputacao:Curso {nome_curso:'Ciência da Computação'})`

10. Crie relacionamento entre os nós: <br>
`CREATE (Professora)-[:Ensina]->(BancoDeDados)` `CREATE (Professora)-[:Orienta]->(TCC)` 

`CREATE (Aluna)-[:Estuda]->(CienciaDaComputacao)` `CREATE (BancoDeDados)-[:Compoe]->(CienciaDaComputacao)` `return *`

