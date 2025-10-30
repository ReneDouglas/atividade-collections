# Atividade com Collections, Streams e Lambdas

## Contexto do Problema
Foi concebido a você a tarefa de criar as consultas para um sistema de biblioteca
em desenvolvimento pela empresa na qual você trabalha.

## Modelagem
Classes do sistema
- Classe Autor
  - nome (String)
  - nacionalidade (String)
  - anoNascimento (int)
- Classe Livro
  - isbn (String)
  - titulo (String)
  - autor (Autor)
  - anoPublicacao (int)
  - categoria (String) - ex: "Ficção", "Técnico", "Biografia"
  - disponivel (boolean)
  - numeroPaginas (int)
- Classe Emprestimo
  - livro (Livro)
  - nomeUsuario (String)
  - dataEmprestimo (LocalDate)
  - dataDevolucao (LocalDate)

Implemente os seguintes métodos usando **Collections, Streams e Lambdas**:

## Métodos Obrigatórios:

1. **`List<Livro> buscarLivrosPorAutor(String nomeAutor)`**
    - Retorna todos os livros de um determinado autor

2. **`List<Livro> livrosDisponiveisOrdenadosPorAno()`**
    - Retorna livros disponíveis ordenados por ano de publicação (mais recente primeiro)

3. **`Map<String, Long> contarLivrosPorCategoria()`**
    - Retorna um mapa com a quantidade de livros por categoria

4. **`double mediaAnoPublicacao()`**
    - Calcula a média dos anos de publicação de todos os livros

5. **`List<Livro> livrosPublicadosEntre(int anoInicio, int anoFim)`**
    - Retorna livros publicados em um intervalo de anos

6. **`List<String> autoresMaisProlificos(int top)`**
    - Retorna os N autores com mais livros no acervo

7. **`boolean existeLivroComMaisDePaginas(int numeroPaginas)`**
    - Verifica se existe algum livro com mais páginas que o valor informado

8. **`List<Emprestimo> emprestimosDoMes(int mes, int ano)`**
    - Retorna empréstimos realizados em um mês/ano específico

9. **`String usuarioComMaisEmprestimos()`**
    - Retorna o nome do usuário que mais realizou empréstimos

10. **`List<Livro> livrosMaisEmprestados(int top)`**
    - Retorna os N livros mais emprestados

## 🧪 Testes

Crie uma classe `Main` ou método de teste que:

1. Popule o acervo com pelo menos 15 livros de diferentes autores e categorias
2. Registre pelo menos 10 empréstimos
3. Teste todos os métodos implementados
4. Imprima os resultados de forma organizada no console

## 📊 Exemplo de Saída Esperada
```
=== BIBLIOTECA MUNICIPAL ===

📖 Livros de Machado de Assis:
- Dom Casmurro (1899)
- Memórias Póstumas de Brás Cubas (1881)

📚 Livros disponíveis (mais recentes):
1. Algoritmos Modernos (2023)
2. Java Avançado (2022)
...

📊 Livros por categoria:
Ficção: 6
Técnico: 4
Biografia: 3
Romance: 2

📅 Média de ano de publicação: 2005.3

👤 Usuário com mais empréstimos: João Silva (5 empréstimos)

## 🚀Desafio Extra (opcional)
Implemente mais 2 métodos:
- `Map<Autor, List<Livro>> agruparLivrosPorAutor()`
- `Optional<Livro> livroMaisAntigo()`


## 💡Dicas
- Use `stream()` para processar as coleções
- Combine `filter()`, `map()`, `sorted()`, `collect()` conforme necessário
- Para contagens, use `Collectors.counting()` ou `Collectors.groupingBy()`
- Para ordenação customizada, use `Comparator.comparing()` ou `reversed()`