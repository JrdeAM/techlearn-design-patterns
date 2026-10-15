# techlearn-design-patterns
# TechLearn — Padrões de Projeto

Projeto desenvolvido como atividade prática da disciplina de **Padrões de Projetos**, com o objetivo de aplicar e integrar os padrões **Singleton, Composite e Iterator** utilizando Java.

A atividade consiste em um sistema simples de gerenciamento de cursos, no qual é possível organizar módulos e aulas, calcular a duração dos conteúdos, registrar operações e percorrer os componentes do catálogo.

## Padrões utilizados

### Singleton
Foi utilizado na classe `LoggerService` para centralizar os registros de logs do sistema, garantindo o acesso a uma única instância do serviço durante a execução.

### Composite
Foi utilizado para organizar os cursos, módulos e aulas em uma estrutura hierárquica.

As principais classes são:
- `ComponenteCatalogo`: classe abstrata que define os métodos comuns.
- `Aula`: representa os conteúdos individuais.
- `Modulo`: permite armazenar aulas e outros módulos, além de calcular a duração total dos conteúdos.

### Iterator
Foi utilizado para percorrer os componentes dos módulos de forma sequencial, sem que o código cliente precise acessar diretamente a lista interna.

Foi implementado por meio da interface `Iterator` e das classes `ModuloIterator` e `NullIterator`.

## Funcionalidades

- Organização de cursos, módulos e aulas.
- Adição e remoção de componentes.
- Cálculo da duração total dos conteúdos.
- Registro de operações por meio de logs.
- Navegação pelos módulos utilizando Iterator.
- Filtragem de aulas com duração menor ou igual a 45 minutos.

## Estrutura do projeto

```text
src/
└── techlearn/
    ├── Main.java
    ├── composite/
    │   ├── Aula.java
    │   ├── ComponenteCatalogo.java
    │   └── Modulo.java
    ├── iterator/
    │   ├── Iterator.java
    │   ├── ModuloIterator.java
    │   └── NullIterator.java
    └── logging/
        └── LoggerService.java
```

## Tecnologias utilizadas

- Java 21
- Visual Studio Code
- Git e GitHub

## Como executar

É necessário ter o JDK instalado e configurado.

Clone o repositório:

```bash
git clone https://github.com/JrdeAM/techlearn-design-patterns.git
```

Entre na pasta do projeto:

```bash
cd techlearn-design-patterns/src
```

Compile o programa:

```bash
javac techlearn/Main.java
```

Execute:

```bash
java techlearn.Main
```

## Resultado da execução

Durante a execução, o programa apresenta os registros de logs, a organização do curso e a duração de seus módulos.

O curso **Engenharia de Software Moderna** contém dois módulos e cinco aulas, totalizando **225 minutos**.

No desafio final, foi implementado um filtro que identifica as aulas com duração menor ou igual a 45 minutos. O resultado apresenta três aulas:

- Coesão e Acoplamento — 45 minutos.
- Singleton na Prática — 30 minutos.
- Iterator para Coleções — 40 minutos.

## Sobre a atividade

A atividade permitiu colocar em prática os três padrões de projeto e entender como eles podem ser utilizados juntos em um mesmo sistema, facilitando a organização do código e a inclusão de novas funcionalidades.