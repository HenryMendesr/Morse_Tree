Árvore Binária de Código Morse (Java)

Implementação acadêmica, em Java, de uma árvore binária para Código Morse, onde ponto (.) navega para a esquerda e traço (-) para a direita até o nó que armazena o símbolo.
O programa fornece um menu no console para popular a árvore com o alfabeto padrão, inserir novos mapeamentos, codificar e decodificar mensagens, e exibir a árvore.

Universidade

Pontifícia Universidade Católica do Paraná (PUCPR)

Professor

Andrey Cabral Meira

Equipe:

Henry Mendes
Kaue Fontoura
Matheus Bernardi
Rafael Maluf

Regras e restrições usadas no trabalho

Sem estruturas prontas de dados: não usar List, ArrayList, Map, StringBuilder, etc.

Permitido: String, tipos primitivos (int, float), try-catch, throws e funções básicas de entrada.

length apenas em String.

Árvore binária implementada manualmente com nós encadeados (Nodo com esquerdo e direito).

Sem dependências externas e sem emojis.

O código deste repositório segue essas restrições.

Estrutura de pastas e arquivos
src/
└── morse/
    ├── ArvoreBinariaMorse.java   # Lógica da árvore (inserir/buscar/remover, codificar/decodificar, exibir, popular padrão)
    ├── Main.java                 # Programa principal com menu de console
    └── Nodo.java                 # Estrutura do nó (símbolo, esquerdo, direito)


Pacote: morse

Arquivos:

Nodo.java: nó mínimo com char simbolo, Nodo esquerdo, Nodo direito.

ArvoreBinariaMorse.java: árvore de Morse com:

inicializar()

inserir(String codigoMorse, char simbolo)

buscar(String codigoMorse)

remover(String codigoMorse)

buscarMorsePorCaractere(char simbolo)

textoParaMorse(String texto)

morseParaTexto(String codigoMorse)

exibir()

popularPadrao() → carrega A–Z e 0–9 conforme a tabela tradicional.

Main.java: cria a árvore, chama popularPadrao() e apresenta menu interativo no console.

Pré-requisitos

Java JDK 17+ (funciona também em 11+ se o compilador aceitar o código).

Terminal do sistema (Windows, macOS ou Linux).

Verifique sua instalação com:

java -version
javac -version

Como compilar e executar

Compile a partir da pasta src para respeitar o package morse.

Linux / macOS
cd src
javac morse/*.java
java morse.Main

Windows (PowerShell ou CMD)
cd src
javac morse\*.java
java morse.Main


Se usar uma IDE (VS Code ou IntelliJ), configure src como pasta de fontes e mantenha o package morse.

Uso – fluxo geral

Ao iniciar:

A árvore é criada e popularPadrao() insere os códigos de A–Z e 0–9.

O menu do Main oferece operações como:

Inserir novo mapeamento (código Morse e símbolo).

Codificar texto em Morse.

Decodificar Morse para texto.

Remover um mapeamento existente.

Exibir a árvore no console.

Sair do programa.

A ordem e nomes das opções podem variar conforme a versão do Main.java, mas as funções da árvore suportam todas as operações acima.

Exemplos rápidos
Decodificar

Entrada:

.... . .-.. .-.. ---


Saída:

HELLO


Entrada:

.---- ..--- ...-- ....- -----


Saída:

12345

Codificar

Entrada:

PUCPR


Saída:

.--. ..- -.-. .--. .-.

Inserir mapeamento

Código:

.-.--


Símbolo:

X


Resultado: cria nós intermediários se necessário e grava X no nó destino.

Decisões de implementação

Navegação por string: . segue para esquerdo, - para direito.

Operações somente com String e tipos primitivos, sem coleções prontas.

popularPadrao() monta a base completa de A–Z e 0–9.

Métodos adicionais para suporte bidirecional:

textoParaMorse() → codificação.

morseParaTexto() → decodificação.

buscarMorsePorCaractere() → busca reversa de símbolo.

Testes manuais sugeridos

Popular a árvore padrão e decodificar ... --- ... → SOS.

Codificar PUCPR → .--. ..- -.-. .--. .-..

Inserir um novo mapeamento (.-.- → X) e validar com codificar/decodificar.

Remover um mapeamento e verificar comportamento ao decodificar aquele caminho.

Exibir a árvore e conferir a distribuição esquerda/direita conforme . e -.
