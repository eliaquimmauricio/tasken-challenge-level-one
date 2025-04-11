# 🧠 Desafio Tasken - Programação & Banco de Dados - Level 1️⃣

Olá! Este desafio tem como objetivo avaliar suas habilidades de programação e conhecimentos em banco de dados. Leia com atenção as instruções abaixo.

---

## 📌 Instruções

1. **Faça um fork** deste repositório.
2. **Configure o seu repositório como privado.**
3. **Conceda acesso ao usuário `eliaquimmauricio`.**
4. Crie um diretório para cada questão, com os respectivos códigos e uma explicação rápida (caso necessário).
5. Responda o e-mail que você recebeu com o link do **SEU** repositório. 
6. **Prazo de entrega**: até **3 dias corridos** após o recebimento.
7. Em caso de dúvidas, entre em contato com o RH via WhatsApp.
8. Evite o uso de IA para resolver as questões, vai ser fácil de detectar o plágio. 😉
9. Faça commits a medida que você evoluir o seu projeto, não deixe para fazer um unico commit no final.

---

## 💻 Linguagens Aceitas

- **Programação:** C#, Python, JavaScript ou Delphi.
- **Banco de Dados:** SQL Server (preferencialmente), MySQL ou PostgreSQL.

---

## 🔢 Questões de Programação

### 1. Função para Impressão em Pirâmide

Crie uma função que receba um valor inteiro `n` e imprima na tela `n` linhas no formato abaixo:

```
Informe um número: 10

100 81 64 49 36 25 16 9 4 1
81 64 49 36 25 16 9 4 1
64 49 36 25 16 9 4 1
49 36 25 16 9 4 1
36 25 16 9 4 1
25 16 9 4 1
16 9 4 1
9 4 1
4 1
1
```

- Se `n <= 0`, deve ser exibida uma crítica e o processo abortado.

---

### 2. Compactação de String

Escreva uma função que receba uma `string` e retorne sua "versão compactada". Exemplo:

```text
Entrada: jjjjooaoo  
Saída: j4o2ao2
```

---

### 3. Leitura de Números Positivos

Crie um programa que:

- Leia números positivos até que `0` seja digitado.
- Em seguida, exiba:
  - a) Quantos números foram lidos
  - b) O maior número
  - c) A média dos números
  - d) O menor número ímpar (caso exista)
  - e) A quantidade de vezes que cada número foi digitado. Exemplo: "O número 7 ocorreu 2 vezes." 
"O número 13 ocorreu 8 vezes"

💡 **Dica:** use vetores (ou listas, arrays, dicionários etc.)

---

### 4. Análise de Arquivo Texto

Faça um programa que leia um arquivo `.txt` fornecido pelo usuário. O programa deve indicar:

- A linha com **mais vogais**
- A linha com **mais consoantes**

⚠️ Considere apenas letras (sem acentos ou "ç") e espaços.

---

### 5. 🥇 Bônus Question: Conversão de Números por Extenso
Implemente uma função que converta um número inteiro positivo (até 999.999) para a forma por extenso.
Exemplo:

```text
Entrada: 123456  
Saída: "cento e vinte e três mil, quatrocentos e cinquenta e seis"
```

---

## 🧩 Questões de Banco de Dados

Utilize a sintaxe de um banco relacional. Preferencialmente, utilize SQL Server.

---

### 1. Criação de Tabelas

Crie o script para as tabelas:

```text
CLIENTES
- ID (auto incremental, chave primária)
- CPF (varchar, não deve existir repetições na tabela)
- NOME (varchar)
- IDADE (int)

TELEFONES
- ID (auto incremental, chave primária)
- ID_CLIENTE (chave estrangeira da tabela CLIENTES)
- DDD (varchar)
- TELEFONE (varchar)
```
---

### 2. Consulta por Idade

Crie uma consulta SQL que retorne o **nome dos clientes com 22 anos ou mais**, ordenados por idade de forma crescente.

---

### 3. Contagem de Telefones

Escreva uma consulta que retorne:
- Nome do cliente
- Quantidade de telefones que ele possui

💡 Mostrar apenas clientes com pelo menos 1 telefone.

---

### 4. Remoção de Clientes

Escreva o comando SQL para **excluir todos os clientes com sobrenome `santos`**.

---

### 5. 🥇 Bônus Question: Deletar Telefones Duplicados (Mesmo Cliente, Mesmo Número)

Escreva um comando SQL para **remover os telefones duplicados** de um mesmo cliente, ou seja, quando o **mesmo número (DDD + TELEFONE)** estiver registrado mais de uma vez para o mesmo cliente.

**Regras:**
- Mantenha **apenas um dos registros duplicados**.
- Pode assumir que `ID` é a chave primária e deve ser usada para identificar qual apagar.
- Considere que dois telefones são duplicados **somente se DDD e TELEFONE forem iguais para o mesmo cliente**.

💡 *Dica: use `ROW_NUMBER()` ou `CTE` com `PARTITION BY` para identificar os duplicados a serem deletados.*
