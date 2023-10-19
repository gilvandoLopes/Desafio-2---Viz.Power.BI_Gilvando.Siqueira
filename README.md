# Desafio-2---Viz.Power.BI_Gilvando.Siqueira
Desafio de Projeto 2 - Visualização e Análise de Dados com Power BI - Bootcamp Santander 2023

# Desafio ETL – Gilvando Siqueira

## Diretrizes para transformação dos dados

### 1. Verifique os cabeçalhos e tipos de dados
1.1 Na tabela company department, alterei o tipo de dados da coluna Mgr_ssn para número inteiro.
1.2 Na tabela company dependent, alterei a coluna Essn para o tipo número inteiro.
1.3 Na tabela company work_on, alterei a coluna Essn para o tipo número inteiro.
1.4 Na tabela company dependent, coluna sex, alterei as letras iniciais (F e M) para Feminino e Masculino, respectivamente.
1.5 Na tabela company employee, coluna sex, alterei as letras iniciais (F e M) para Feminino e Masculino, respectivamente.

### 2. Modifique os valores monetários para o tipo double preciso
Resposta: Realizada a alteração. Na tabela company_employee, foi alterada a coluna Salary para Número decimal fixo.

### 3. Verifique a existência dos nulos e analise a remoção
Resposta: Os nulos foram tratados diretamente no banco, pois o script apresentava erro quando tentava inserir registros nas tabelas.

### 4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente
Resposta: Não há empregado sem gerente. O script de criação do banco de dados precisou ser alterado, pois estava gerando conflito de chave.

### 5. Verifique se há algum departamento sem gerente
Resposta: Não há departamento sem gerente. O script foi ajustado para popular as tabelas.

### 6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas
Resposta: Não há departamento sem gerente. O script foi ajustado para popular as tabelas.

### 7. Verifique o número de horas dos projetos
Resposta: Não foi possível identificar na tabela Project a coluna referente às horas do projeto, pois o nome do campo não é objetivo e não foi disponibilizado o dicionário dos dados do banco. Em um cenário real, seria necessário consultar a área de negócio.

### 8. Separar colunas complexas
Resposta: A única coluna complexa identificada foi a de endereço (Address) na tabela company employee. Foi dividida em 4 colunas (número, rua, cidade e estado).

### 9. Mesclar consultas employee e department para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção
Resposta: Criei uma mescla do tipo nova consulta. Assim a tabela ficou com 3 registros (linhas): Nome_colaborador | azure_company department.Dname
- Franklin T Wong | Research
- James E Borg | Headquarters
- Jennifer S Wallace | Administration

### 10. Neste processo elimine as colunas desnecessárias.
Resposta: Deixei apenas as colunas nome empregado, nome departamento e Ssn.

### 11. Realize a junção dos colaboradores e respectivos nomes dos gerentes. Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.
Resposta: No script disponibilizado não consta a criação de uma tabela de gerentes, assim não foi possível executar.

### 12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores
Resposta: Na tabela employee, mesclei as colunas do nome, sobrenome e do nome do meio.

### 13. Mescle os nomes de departamentos e localização. Isso fará com que cada combinação departamento-local seja única. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
Resposta: Criei uma consulta mesclada. Tabela Departamento_localizacao.

### 14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.
Resposta: A mesclagem combina dados com base em uma chave de correspondência, criando uma tabela única e relacionada, enquanto a atribuição simplesmente empilha tabelas para criar uma tabela maior sem combinar dados com base em colunas específicas.

### 15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente
Resposta: No script de criação do banco de dados não constava uma tabela de gerentes, por isso não foi possível incluí-la. Em um cenário real, seria necessário consultar a área de negócio.

### 16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela
Respostas: Colunas removidas.

