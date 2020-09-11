# Iniciando o projeto

Para iniciar um projeto Nextjs, execute:

```bash
yarn init -y
```

Instale o next e o react:

```bash
yarn add next react react-dom
```

Adicione o Typescript (opcional):

```bash
yarn add -D typescript @types/node @types/react
```
Na pasta do projeto, crie o diretório *pages*.

```bash
mkdir pages
```

```bash
cd pages
```

Dentro de *pages*, crie o arquivo **index.tsx**:

```bash
touch index.tsx
```

Dentro de **index.ts**, adicione o seguinte código;

```javascript
import React from 'react';

const Home = () => {
    return <h1>Hello!!!</h1>
}

export default Home;
```

Na pasta principal, execute o comando:

```bash
yarn next
```

Agora abra uma aba no navegador acessando a porta *3000* do localhost.

![Alt text](./resources/tela-inicial.png?raw=true "Optional Title")

Pronto. Projeto NextJS configurado!