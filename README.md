# Uma DSL Híbrida para Jogos RPG com Suporte a Eventos de Gameplay

Projeto acadêmico voltado ao desenvolvimento de uma DSL (Domain-Specific Language) híbrida para criação de RPGs textuais interativos com suporte a eventos de gameplay, interpretação dinâmica e narrativa procedural.

O sistema utiliza conceitos de:
- compiladores;
- análise léxica e sintática;
- AST (Abstract Syntax Tree);
- interpretação de linguagem;
- motores narrativos interativos.

---

## Objetivo do Projeto

O projeto tem como objetivo desenvolver uma linguagem específica de domínio capaz de simplificar a criação de jogos RPG textuais interativos.

A DSL permite que desenvolvedores descrevam:
- cenas;
- personagens;
- diálogos;
- eventos;
- escolhas;
- condições;
- progressão narrativa.

Tudo isso através de uma sintaxe simplificada baseada em gramática EBNF.

---

## Tecnologias Utilizadas

- Python 3
- PLY (Python Lex-Yacc)
- Google Colab
- Jupyter Notebook

---

## Funcionalidades

- Sistema de cenas
- Sistema de diálogos
- Navegação entre cenas
- Eventos de gameplay
- Sistema de escolhas
- Condições
- Variáveis
- Runtime interpretativo
- Parser utilizando PLY/Yacc
- AST personalizada
- Estrutura baseada em EBNF

---

## Arquitetura do Sistema

```text
Código DSL
    ↓
Lexer
    ↓
Parser
    ↓
AST
    ↓
Runtime
    ↓
Jogo Interativo
```

---

## Exemplo da DSL

```txt
character hero {

    vida = 100;
    ouro = 50;
}

scene inicio {

    say "Você acorda em uma floresta.";

    choice {

        "Ir para vila" -> vila;
        "Explorar caverna" -> caverna;
    }
}
```

---

## Exemplo Simplificado da Gramática EBNF

```ebnf
program         ::= declaration+

declaration     ::= scene
                  | character
                  | event

scene           ::= "scene" ID "{" commands "}"

commands        ::= command+

command         ::= say
                  | choice
                  | goto
                  | trigger
```

---

## Estrutura do Projeto

```text
project/
│
├── DSL(V1).ipynb
├── DSL(V2).ipynb
├── DSL(V3).ipynb
│
├── lexer/
├── parser/
├── runtime/
├── ast/
│
└── README.md
```

---

## Como Executar

### Instalação do PLY

```bash
pip install ply
```

### Execução

Abra os notebooks no:
- Google Colab
- Jupyter Notebook

Execute:
- DSL(V1).ipynb
- DSL(V2).ipynb
- DSL(V3).ipynb

---

## Possíveis Expansões Futuras

- Sistema de combate
- Inteligência artificial narrativa
- Geração procedural avançada
- Sistema de save/load
- Inventário expandido
- Interface gráfica
- Multiplayer textual
- Exportação de jogos

---

## Contexto Acadêmico

Este projeto integra pesquisas relacionadas a:
- Linguagens específicas de domínio;
- Compiladores;
- Interpretação de linguagens;
- Jogos digitais;
- Narrativas procedurais;
- RPGs textuais interativos.

---

## Autores

### Gabriel Franklin Martins Lazzarini Miranda
Engenharia da Computação  
Centro Universitário – Fundação Hermínio Ometto  
Araras, Brasil

### Lucas Fortolan Sampaio
Engenharia da Computação  
Centro Universitário – Fundação Hermínio Ometto  
Araras, Brasil


# A Hybrid DSL for RPG Games with Gameplay Event Support

Academic project focused on developing a hybrid DSL (Domain-Specific Language) for creating interactive text-based RPGs with gameplay event support, dynamic interpretation, and procedural storytelling.

The system uses concepts related to:
- compilers;
- lexical and syntax analysis;
- AST (Abstract Syntax Tree);
- language interpretation;
- interactive narrative engines.

---

## Project Goal

The goal of this project is to develop a domain-specific language capable of simplifying the creation of interactive text RPG games.

The DSL allows developers to describe:
- scenes;
- characters;
- dialogues;
- events;
- choices;
- conditions;
- narrative progression.

All through a simplified syntax based on EBNF grammar.

---

## Technologies Used

- Python 3
- PLY (Python Lex-Yacc)
- Google Colab
- Jupyter Notebook

---

## Features

- Scene system
- Dialogue system
- Scene navigation
- Gameplay events
- Choice system
- Conditions
- Variables
- Interpretive runtime
- Parser using PLY/Yacc
- Custom AST
- EBNF-based structure

---

## System Architecture

```text
DSL Code
    ↓
Lexer
    ↓
Parser
    ↓
AST
    ↓
Runtime
    ↓
Interactive Game
```

---

## DSL Example

```txt
character hero {

    vida = 100;
    ouro = 50;
}

scene inicio {

    say "You wake up in a forest.";

    choice {

        "Go to village" -> village;
        "Explore cave" -> cave;
    }
}
```

---

## Simplified EBNF Grammar Example

```ebnf
program         ::= declaration+

declaration     ::= scene
                  | character
                  | event

scene           ::= "scene" ID "{" commands "}"

commands        ::= command+

command         ::= say
                  | choice
                  | goto
                  | trigger
```

---

## Project Structure

```text
project/
│
├── DSL(V1).ipynb
├── DSL(V2).ipynb
├── DSL(V3).ipynb
│
├── lexer/
├── parser/
├── runtime/
├── ast/
│
└── README.md
```

---

## How to Run

### Install PLY

```bash
pip install ply
```

### Execution

Open the notebooks using:
- Google Colab
- Jupyter Notebook

Run:
- DSL(V1).ipynb
- DSL(V2).ipynb
- DSL(V3).ipynb

---

## Future Improvements

- Combat system
- Narrative AI integration
- Advanced procedural generation
- Save/Load system
- Expanded inventory
- Graphical interface
- Text multiplayer
- Game export support

---

## Academic Context

This project is part of research involving:
- Domain-Specific Languages;
- Compilers;
- Language Interpretation;
- Digital Games;
- Procedural Narratives;
- Interactive Text RPGs.

---

## Authors

### Gabriel Franklin Martins Lazzarini Miranda
Computer Engineering  
Centro Universitário – Fundação Hermínio Ometto  
Araras, Brazil

### Lucas Fortolan Sampaio
Computer Engineering  
Centro Universitário – Fundação Hermínio Ometto  
Araras, Brazil
