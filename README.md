### Building Container

```bash
docker-compose build
```

### Subindo o Container

```bash
docker-compose up 
```
### Rodando algum comando extra

```bash
docker-compose run web _commando_
```

### Como configurar o tailwindcss no projeto

```bash
docker-compose run web npm install -D tailwindcss postcss autoprefixer

docker-compose run web npx tailwindcss init
```

Ao rodar o comando com npx, um arquivo chamado tailwind.config.js será gerado no seguinte formato: 

```javascript
module.exports = {
  content: [],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Depois, é necessário modificar esse arquivo para ficar da seguinte forma:

```javascript
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Por fim, basta fazer a importação no arquivo css do projeto:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Referencias
:books: [tailwindcss](https://tailwindcss.com/docs/guides/create-react-app)

:books: [Dockerizando uma aplicação React JS](https://blog.codeexpertslearning.com.br/dockerizando-uma-aplica%C3%A7%C3%A3o-react-js-f6a22e93bc5d)
