# 🎮 Hybrid RPG DSL V4  
## Uma DSL Híbrida para Jogos RPG com Suporte a Eventos de Gameplay  
## A Hybrid DSL for RPG Games with Gameplay Event Support

---

# 🇧🇷 Português (PT-BR)

## 📖 Sobre o Projeto

Este projeto apresenta uma **Linguagem Específica de Domínio (DSL)** híbrida voltada para a criação de jogos RPG narrativos baseados em texto.

A linguagem foi desenvolvida com foco em:

- Modelagem de narrativas interativas
- Controle de fluxo baseado em escolhas
- Eventos dinâmicos de gameplay
- Mutação de estados do jogador
- Segurança semântica preventiva
- Arquitetura inspirada em compiladores clássicos

A DSL utiliza técnicas formais de construção de compiladores, incluindo:

- Análise Léxica
- Parsing LALR(1)
- AST (Abstract Syntax Tree)
- Verificação Semântica Estática
- Runtime Interpretado em Python

A implementação foi construída utilizando a biblioteca **PLY (Python Lex-Yacc)**.

---

# ✨ Principais Recursos da V4

## ✅ Controle Narrativo

- `scene`
- `choice`
- `goto`
- `say`

## ✅ Sistema de Eventos

- `event`
- `trigger`

## ✅ Manipulação de Estado

- `set`
- `add`
- `remove`

## ✅ Controle Condicional

- `if ... then`

## ✅ Operadores Relacionais

- `==`
- `!=`
- `>`
- `<`
- `>=`
- `<=`

## ✅ Segurança Semântica

A linguagem realiza verificações preventivas para:

- Identificadores duplicados
- Tipos incompatíveis
- Referências inexistentes
- Fluxos órfãos
- Operações inválidas

## ✅ Sistema de Game Over

A engine monitora variáveis críticas em tempo de execução para impedir estados inválidos.

## ✅ Suporte a Comentários

```dsl
// Comentário
```

---

# 🏗️ Arquitetura do Projeto

O projeto foi organizado seguindo a estrutura clássica de compiladores:

```text
Lexer → Parser → AST → Semantic Checker → Runtime
```

## Estrutura Geral

```text
DSL(V4).ipynb
│
├── Tokens Léxicos
├── Parser Sintático (PLY/Yacc)
├── Nós da AST
├── Semantic Checker
└── Runtime Interativo
```

---

# ⚙️ Tecnologias Utilizadas

- Python
- PLY (Python Lex-Yacc)
- Parsing LALR(1)
- AST Interpretation
- Context-Free Grammar (CFG)
- EBNF

---

# 🧠 Gramática da DSL (V4)

```ebnf
<programa> ::= { <declaracao> }

<declaracao> ::= <cena> | <personagem> | <evento>

<cena> ::= "scene" <identificador> "{"
              { <comando> }
           "}"

<personagem> ::= "character" <identificador> "{"
                    { <atributo> }
                 "}"

<evento> ::= "event" <identificador> "{"
                { <acao> }
             "}"

<comando> ::= <dialogo>
            | <escolha>
            | <transicao>
            | <disparo_evento>

<dialogo> ::= "say" <string> ";"

<escolha> ::= "choice" "{"
                { <opcao> }
              "}"

<opcao> ::= <string> "->" <identificador> ";"

<transicao> ::= "goto" <identificador> ";"

<disparo_evento> ::= "trigger" <identificador> ";"

<atributo> ::= <identificador> "=" <valor> ";"

<acao> ::= <mutacao>
         | <condicional>
         | <dialogo>

<mutacao> ::= <op_mutacao> <identificador> <valor> ";"

<op_mutacao> ::= "set" | "add" | "remove"

<condicional> ::= "if" <condicao> "then" <acao>

<condicao> ::= <identificador> <operador> <valor>

<operador> ::= "==" | "!=" | ">" | "<" | ">=" | "<="

<comentario> ::= "//" { caractere }
```

---

# 🎲 Exemplo de Script

```dsl
character hero {
    vida = 100;
    coragem = 10;
}

scene inicio {
    say "Você acorda em um navio abandonado.";

    choice {
        "Explorar o convés" -> deck;
        "Voltar para a cabine" -> cabine;
    }
}

event batalha {
    if vida > 30 then say "Você sobreviveu à batalha.";
    remove vida 25;
    add coragem 15;
}
```

---

# 🚀 Como Executar

## 1️⃣ Instale as dependências

```bash
pip install ply
```

## 2️⃣ Abra o notebook

```bash
jupyter notebook
```

## 3️⃣ Execute o projeto

Abra:

```text
DSL(V4).ipynb
```

Execute todas as células em ordem.

---

# 🧪 Caso de Teste Experimental

A linguagem foi validada através do jogo experimental:

## 🌊 "Horizonte Rubro e o Mar Invertido"

O roteiro utiliza:

- Eventos dinâmicos
- Controle condicional
- Mutação de atributos
- Sistema de escolhas
- Inventário
- Game Over automático

---

# 📚 Conceitos Acadêmicos Aplicados

Este projeto aplica conceitos de:

- Compiladores
- Linguagens Formais
- Autômatos
- Parsing
- Verificação Semântica
- AST
- DSLs
- Engenharia de Software
- Desenvolvimento de Jogos

---

# 🔮 Trabalhos Futuros

- Escopo local de variáveis
- Save/Load Game
- Expressões matemáticas complexas
- IDE visual baseada em nós
- Integração com PLN (Processamento de Linguagem Natural)
- Suporte a NPCs avançados

---

# 👨‍💻 Autores

## Gabriel Franklin Martins Lazzarini Miranda
Engenharia da Computação  
Centro Universitário Fundação Hermínio Ometto (FHO)
https://www.linkedin.com/in/gabriel-franklin-martins-lazzarini-miranda/

## Lucas Fortolan Sampaio
Engenharia da Computação  
Centro Universitário Fundação Hermínio Ometto (FHO)
https://www.linkedin.com/in/lucasfortolan/

---

---

# 🇺🇸 English Version

## 📖 About the Project

This project presents a hybrid **Domain-Specific Language (DSL)** designed for text-based narrative RPG games.

The language was created focusing on:

- Interactive narrative modeling
- Choice-driven flow control
- Dynamic gameplay events
- Player state mutation
- Preventive semantic safety
- Compiler-inspired architecture

The DSL applies formal compiler construction techniques, including:

- Lexical Analysis
- LALR(1) Parsing
- Abstract Syntax Tree (AST)
- Static Semantic Verification
- Python Interpreted Runtime

The implementation was built using **PLY (Python Lex-Yacc)**.

---

# ✨ Main Features of V4

## ✅ Narrative Control

- `scene`
- `choice`
- `goto`
- `say`

## ✅ Event System

- `event`
- `trigger`

## ✅ State Mutation

- `set`
- `add`
- `remove`

## ✅ Conditional Logic

- `if ... then`

## ✅ Relational Operators

- `==`
- `!=`
- `>`
- `<`
- `>=`
- `<=`

## ✅ Semantic Safety

The language performs preventive checks for:

- Duplicate identifiers
- Invalid types
- Missing references
- Orphan narrative flows
- Invalid operations

## ✅ Game Over System

The runtime monitors critical variables to prevent invalid execution states.

## ✅ Comment Support

```dsl
// Comment
```

---

# 🏗️ Project Architecture

The project follows a traditional compiler pipeline:

```text
Lexer → Parser → AST → Semantic Checker → Runtime
```

## General Structure

```text
DSL(V4).ipynb
│
├── Lexical Tokens
├── Syntax Parser (PLY/Yacc)
├── AST Nodes
├── Semantic Checker
└── Interactive Runtime
```

---

# ⚙️ Technologies Used

- Python
- PLY (Python Lex-Yacc)
- LALR(1) Parsing
- AST Interpretation
- Context-Free Grammar (CFG)
- EBNF

---

# 🧠 DSL Grammar (V4)

```ebnf
<programa> ::= { <declaracao> }

<declaracao> ::= <cena> | <personagem> | <evento>

<cena> ::= "scene" <identificador> "{"
              { <comando> }
           "}"

<personagem> ::= "character" <identificador> "{"
                    { <atributo> }
                 "}"

<evento> ::= "event" <identificador> "{"
                { <acao> }
             "}"

<comando> ::= <dialogo>
            | <escolha>
            | <transicao>
            | <disparo_evento>

<dialogo> ::= "say" <string> ";"

<escolha> ::= "choice" "{"
                { <opcao> }
              "}"

<opcao> ::= <string> "->" <identificador> ";"

<transicao> ::= "goto" <identificador> ";"

<disparo_evento> ::= "trigger" <identificador> ";"

<atributo> ::= <identificador> "=" <valor> ";"

<acao> ::= <mutacao>
         | <condicional>
         | <dialogo>

<mutacao> ::= <op_mutacao> <identificador> <valor> ";"

<op_mutacao> ::= "set" | "add" | "remove"

<condicional> ::= "if" <condicao> "then" <acao>

<condicao> ::= <identificador> <operador> <valor>

<operador> ::= "==" | "!=" | ">" | "<" | ">=" | "<="

<comentario> ::= "//" { caractere }
```

---

# 🎲 Example Script

```dsl
character hero {
    vida = 100;
    coragem = 10;
}

scene inicio {
    say "You wake up inside an abandoned ship.";

    choice {
        "Explore the deck" -> deck;
        "Return to the cabin" -> cabin;
    }
}

event battle {
    if vida > 30 then say "You survived the battle.";
    remove vida 25;
    add coragem 15;
}
```

---

# 🚀 Running the Project

## 1️⃣ Install dependencies

```bash
pip install ply
```

## 2️⃣ Open the notebook

```bash
jupyter notebook
```

## 3️⃣ Run the project

Open:

```text
DSL(V4).ipynb
```

Execute all notebook cells in order.

---

# 🧪 Experimental Validation

The language was validated using the experimental RPG:

## 🌊 "Horizonte Rubro e o Mar Invertido"

The test scenario explores:

- Dynamic events
- Conditional execution
- Attribute mutation
- Branching choices
- Inventory system
- Automatic Game Over

---

# 📚 Academic Concepts Applied

This project applies concepts from:

- Compiler Design
- Formal Languages
- Automata Theory
- Parsing
- Semantic Verification
- AST
- DSL Engineering
- Software Engineering
- Game Development

---

# 🔮 Future Work

- Local variable scopes
- Save/Load system
- Complex mathematical expressions
- Visual node-based IDE
- NLP integration
- Advanced NPC support

---

# 👨‍💻 Authors

## Gabriel Franklin Martins Lazzarini Miranda
Computer Engineering  
Centro Universitário Fundação Hermínio Ometto (FHO)
https://www.linkedin.com/in/gabriel-franklin-martins-lazzarini-miranda/

## Lucas Fortolan Sampaio
Computer Engineering  
Centro Universitário Fundação Hermínio Ometto (FHO)
https://www.linkedin.com/in/lucasfortolan/
---
