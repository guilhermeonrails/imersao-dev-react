# Imersão | Bandas

Este é um projeto simples de demonstração de bandas usando React.

## Estrutura HTML/CSS

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <script crossorigin src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <title>Imersão | Bandas</title>
</head>
<body>
    <section class="bandas" id="bandas">
        <!-- Conteúdo gerado dinamicamente pelo React -->
    </section>

    <script type="text/babel" src="app.jsx"></script>
</body>
</html>
```


```jsx
function Banda(props) {
    return (
        <div className="bandas__cartao">
            <h1>{props.nome}</h1>
            <img src={props.imagem} alt={`Imagem da banda ${props.nome}`} />
        </div>
    )
}


var bandas = (
    <div>
        <Banda nome='Oasis' imagem='https://monkeybuzz.com.br/wp-content/uploads/2014/08/oasis(1).jpg'></Banda>
        <Banda nome='U2' imagem='https://i0.wp.com/www.wikimetal.com.br/wp-content/uploads/2022/02/U2.jpg?fit=1200%2C675&ssl=1'></Banda>
        <Banda nome='Pink Floyd' imagem='https://i.scdn.co/image/d011c95081cd9a329e506abd7ded47535d524a07'></Banda>
        <Banda nome='Red Hot' imagem='https://i.pinimg.com/1200x/01/9a/1f/019a1f097751c6d53eeb054aad7c1ff0.jpg'></Banda>
    </div>
)

ReactDOM.render(bandas, document.getElementById('bandas'))
```