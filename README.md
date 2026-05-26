# DSL para Visualização de Dados Simples

**Disciplina:** Teoria da Computação e Compiladores  
**Autor:** Caetano Orloski Moriconi  
**Instituição:** Fundação Hermínio Ometto — FHO, Mogi Mirim - SP  

## O que é este projeto

Implementação de uma linguagem específica de domínio (DSL) para geração de visualizações simples de dados. O usuário escreve comandos como:

GRAFICO BARRA DADOS(40, 70, 55, 90) TITULO "Vendas"

E o sistema gera o gráfico automaticamente.

## Etapas implementadas

| Etapa | Classe | O que produz |
|---|---|---|
| Análise Léxica | `Lexer` | Lista de tokens |
| Análise Sintática | `Parser` | AST (Árvore Sintática Abstrata) |
| Análise Semântica | `AnalisadorSemantico` | Validação de significado |
| Interpretação | `Interpretador` | Gráficos com matplotlib |

## Linguagem aceita

GRAFICO BARRA DADOS(v1, v2, ...) TITULO "texto"
GRAFICO LINHA DADOS(v1, v2, ...) TITULO "texto"

- Valores devem ser **inteiros positivos**
- Mínimo de **2 valores** por comando
- O `TITULO` é opcional
