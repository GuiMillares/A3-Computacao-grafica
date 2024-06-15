### Gerador de Avatar

Este projeto é um gerador de avatar dinâmico que cria avatares únicos com base no texto inserido pelo usuário. Utiliza hash SHA-256 para garantir que cada entrada produza um avatar distinto.

### Sumário

- **Instalação**
- **Uso**
- **Estrutura do Código**
- **Funções Principais**
- **Licença**

### Instalação

Para executar este projeto localmente, siga os passos abaixo:

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/gerador-avatar.git
   ```
2. Navegue até o diretório do projeto:
   ```bash
   cd gerador-avatar
   ```
3. Abra o arquivo `index.html` em um navegador.

### Uso

1. Abra o arquivo `index.html` em um navegador.
2. Digite um texto no campo de input.
3. Um avatar único será gerado e exibido no contêiner de avatar com base no texto fornecido.

### Estrutura do Código

O código consiste em um arquivo HTML que inclui um campo de input e um contêiner para exibir o avatar gerado. O avatar é desenhado dinamicamente usando funções de desenho e uma hash gerada a partir do input do usuário.


### Funções Principais

**keygen**
- **next():** Gera um número pseudo-aleatório.
- **next16():** Gera um número pseudo-aleatório usando 16 bits do hash.
- **next256():** Gera um número pseudo-aleatório usando 256 bits do hash.
- **next4095():** Gera um número pseudo-aleatório usando 4095 bits do hash.
- **getKeyParams(id):** Gera parâmetros de chave baseados no ID fornecido.
- **sha256(ascii):** Calcula o hash SHA-256 de uma string ASCII.

**widget**
- **widget(key, draw):** Função principal que desenha o avatar. Recebe a chave gerada pelo keygen e um objeto de desenho.

**getColorIterator**
- O módulo `colors` fornece uma função `getColorIterator` que retorna um iterador de cores. Utilizado pelo `widget` para definir as cores das formas desenhadas.

### Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
