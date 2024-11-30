
O grafo de fluxo abaixo representa o fluxo lógico do código


1. Início do método `conectarBD()`.
2. Carregar o driver JDBC.
3. Tentar estabelecer a conexão com o banco de dados.
4. Exceção capturada em caso de erro.
5. Retorna a conexão.
6. Início do método `verificarUsuario()`.
7. Montagem do SQL de validação.
8. Conectar ao banco e preparar a query.
9. Executar a query.
10. Usuário encontrado (caso positivo).
11. Exceção capturada em caso de erro.
12. Retornar o resultado (true ou false).

Grafo de fluxo

[1] -> [2] -> [3] -> [5]
                |
                v
               [4]

[6] -> [7] -> [8] -> [9] -> [10] -> [12]
                              |
                              v
                             [11]

Complexidade Ciclomática

 Resultados
 Método `conectarBD()`
 Caminhos Independentes:
  1. Caminho 1: Conexão bem-sucedida.
  2. Caminho 2: Exceção durante a conexão.

Complexidade Ciclomática: \( M = 2 \)

 Método `verificarUsuario()`
Caminhos Independentes:
  1. Caminho 1: Usuário encontrado.
  2. Caminho 2: Usuário não encontrado.
  3. Caminho 3: Exceção durante a execução da query.

- Complexidade Ciclomática: \( M = 3 \)

Complexidade Total do Código
A soma das complexidades dos dois métodos é:
\[
M_{\text{total}} = 5
\]


Grafo do Método `conectarBD()`
[1] -> [2] -> [3] -> [5]
                |
                v
               [4]
