# BCC328: Construção de Compiladores I

[![Build Status](https://travis-ci.org/romildo/bcc328.2020.1.svg?branch=master)](https://travis-ci.org/romildo/bcc328.2020.1)

Writing a compiler for a toy language.


## Preparing the environment for the project (Ubuntu >= 18.04)

### Installing some development languages, libraries and tools

- Processador de macro de uso geral que é usado por vários componentes do OCaml
  ```
  $ sudo apt install m4
  ```

- Utilitário que usa a biblioteca readline para permitir a edição da entrada do teclado para qualquer comando
  ```
  $ sudo apt install rlwrap
  ```

- Opam (OCaml package manager)
  Install binary directly from the internet. Alternatively can be installed using the operating system package manager.
  ```
  $ sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)
  ```

  Inicializa o estado interno do opam no diretório ~/.opam
  ```
  $ opam init --bare
  ```

- Instala compilador de OCaml
  ```
  $ opam switch create 4.11.1
  ```

  Aplica as alterações para o shell atual
  ```
  $ eval $(opam env)
  ```

- Sistema de construção para OCaml
  ```
  $ opam install dune
  ```

- Serviço de editor que fornece recursos IDE modernos para o OCaml
  ```
  $ opam install merlin
  ```

- Extensão de sintaxe que permite extrair tipos ou assinaturas de outros arquivos de interface compilados
  ```
  $ opam install ppx_import
  ```

- Extensão de sintaxe que facilita geração de código baseada em tipos em OCaml
  ```
  $ opam install ppx_deriving
  ```

- Extensão de sintaxe para escrita de testes em OCaml
  ```
  $ opam install ppx_expect
  ```

- Biblioteca unicode para OCaml
  ```
  $ opam install camomile
  ```

- Gerador de analisador sintático para OCaml
  ```
  $ opam install menhir
  ```

- Get a textual interface file (.mli) from the compiled interface (.cmi)
  ```
  $ opam install ocaml-print-intf
  ```

- Implementação do servidor de protocolo de linguagem para OCaml
  ```
  $ opam install ocaml-lsp-server
  ```

- Ambiente interativo alternativo para OCaml
  ```
  $ opam install utop
  ```

- Install LLVM and CLang
  - CLang (C/C++ compiler)
    ```
    $ sudo apt install clang
    ```
  - Dependencies for building OCaml LLVM bindings
    ```
    $ sudo apt install cmake m4 python2
    ```
  - LLVM bindings for OCaml
    ```
    $ opam install llvm
    ```

## Sugestion for an IDE:
- [Visual Studio Code](https://code.visualstudio.com/) with the OCaml Platform extension.

## How to clean uneeded files

```
$ dune clean
```

## How to compile and run the `hello` example

```
$ dune build src/hello/hello.exe
```

```
$ dune exec src/hello/hello.exe
```
