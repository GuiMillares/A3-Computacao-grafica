# Gerador de Avatar

Este projeto é um gerador de avatar dinâmico que cria um avatar único com base no input fornecido pelo usuário. Ele utiliza um hash gerado a partir do input para garantir que cada entrada produza um avatar distinto.

## Sumário

- [Instalação](#instalação)
- [Uso](#uso)
- [Estrutura do Código](#estrutura-do-código)
- [Funções Principais](#funções-principais)
- [Licença](#licença)

## Instalação

Para executar este projeto localmente, siga os passos abaixo:

1. Clone o repositório:
    ```sh
    git clone https://github.com/seu-usuario/gerador-avatar.git
    ```
2. Navegue até o diretório do projeto:
    ```sh
    cd gerador-avatar
    ```
3. Abra o arquivo `index.html` em um navegador.

## Uso

1. Abra o arquivo `index.html` em um navegador.
2. Digite um texto no campo de input.
3. Um avatar único será gerado e exibido no contêiner de avatar com base no texto fornecido.

## Estrutura do Código

O código consiste em um arquivo HTML que inclui um campo de input e um contêiner para exibir o avatar gerado. O avatar é desenhado dinamicamente usando funções de desenho e uma hash gerada a partir do input do usuário.

### Estrutura do Diretório

```
gerador-avatar/
├── index.html
├── scripts/
│   ├── keygen.js
│   ├── main.js
│   ├── utils/
│   │   └── colors/
│   │       └── color.js
├── styles/
│   └── main.css
└── README.md
```

## Funções Principais

### `keygen`

O módulo `keygen` gera um hash a partir de um input string. Ele contém as seguintes funções principais:

- `next()`: Gera um número pseudo-aleatório.
- `next16()`: Gera um número pseudo-aleatório usando 16 bits do hash.
- `next256()`: Gera um número pseudo-aleatório usando 256 bits do hash.
- `next4095()`: Gera um número pseudo-aleatório usando 4095 bits do hash.
- `getKeyParams(id)`: Gera parâmetros de chave baseados no ID fornecido.
- `sha256(ascii)`: Calcula o hash SHA-256 de uma string ASCII.

### `widget`

O módulo `widget` desenha o avatar no contêiner especificado. Ele utiliza a hash gerada pelo `keygen` para determinar as formas, cores e posições dos elementos do avatar.

- `widget(key, draw)`: Função principal que desenha o avatar. Recebe a chave gerada pelo `keygen` e um objeto de desenho.

### `getColorIterator`

O módulo `colors` fornece uma função `getColorIterator` que retorna um iterador de cores. Ele é utilizado pelo `widget` para definir as cores das formas desenhadas.

### `sample`

O módulo `sample` (localizado em `examples/widget00.js`) pode ser usado para gerar um exemplo de avatar. Está comentado no código, mas pode ser descomentado para visualizar um exemplo específico.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Para mais detalhes ou contribuições, por favor, visite o repositório do projeto no GitHub.
