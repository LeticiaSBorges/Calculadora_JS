# Calculadora_JS
Este projeto consistiu na criação de uma calculadora com operaçõs básicas de matemática que foram soma, subtração, multiplicação e divisão. 
As linguagens utilizadas foram HTML 5, CSS e JavaScript.

O resuldado do projeto pode ser apreciado em funcionamento clicando [aqui](https://rapid-graceful-tortoise.glitch.me), ou observado por meio das imagens a seguir.

![Imagem 1 - Layout e Calculadora.](https://github.com/LeticiaSBorges/Calculadora_JS/blob/e4c1d16c2fccd2971b2205e61b209f8b92631832/img/calc1.PNG?raw=true)

![Imagem 2 - Calculadora.](https://github.com/LeticiaSBorges/Calculadora_JS/blob/e4c1d16c2fccd2971b2205e61b209f8b92631832/img/calc2.PNG?raw=true)       

![Imagem 3 - Calculadora e operações.](https://github.com/LeticiaSBorges/Calculadora_JS/blob/e4c1d16c2fccd2971b2205e61b209f8b92631832/img/calc3.PNG?raw=true)

O código em html usado foi:
~~~html
<div class="fundo">
        <h1>Letícia Borges</h1>
        <div class="calculadora">
            <h1>Calculadora</h1>
            <p id="resultado"></p>
            <table>
                <tr>
                    <td><button class="botao" onclick="clean()">C</button></td>
                    <td><button class="botao" onclick="back()">&lt</button></td>
                    <td><button class="botao" onclick="insert('/')">/</button></td>
                    <td><button class="botao" onclick="insert('*')">X</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('7')">7</button></td>
                    <td><button class="botao" onclick="insert('8')">8</button></td>
                    <td><button class="botao" onclick="insert('9')">9</button></td>
                    <td><button class="botao" onclick="insert('-')">-</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('4')">4</button></td>
                    <td><button class="botao" onclick="insert('5')">5</button></td>
                    <td><button class="botao" onclick="insert('6')">6</button></td>
                    <td><button class="botao" onclick="insert('+')">+</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('1')">1</button></td>
                    <td><button class="botao" onclick="insert('2')">2</button></td>
                    <td><button class="botao" onclick="insert('3')">3</button></td>
                    <td rowspan="2"><button class="botao" style="height: 130px;" onclick="calcular()">=</button></td>
                </tr>
                <tr>
                    <td colspan="2"><button class="botao" style="width: 130px;" onclick="insert('0')">0</button></td>
                    <td><button class="botao" onclick="insert('.')">.</button></td>
                </tr>
            </table>

        </div>
    </div>
~~~

Já os código em CSS foram:

~~~css
* {
    margin: 0;
    padding: 0;
}

.fundo {
    background-image: linear-gradient(to left top, black, green);
    height: 100vh;
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
}

.calculadora {
    position: absolute;
    background-color: rgba(0, 0, 0, 0.8);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 15px;
    padding: 25px;
}

.botao {
    width: 60px;
    height: 60px;
    font-size: 25px;
    cursor: pointer;
    background-color: rgb(31, 31, 31);
    border: none;
    color: #fff;
    margin: 2px;
}

.botao:hover {
    background-color: black;
}

#resultado {
    width: 250px;
    background-color: white;
    height: 30px;
    margin: 5px;
    font-size: 25px;
    color: black;
    text-align: right;
    padding: 5px;
}
~~~

E por fim as linhas de comando do JavaScript foram:
~~~javascript
function insert(num) {
    var numero = document.getElementById('resultado').innerHTML;
    document.getElementById('resultado').innerHTML = numero + num;
}

function clean() {
    document.getElementById('resultado').innerHTML = "";
}

function back() {
    var resultado = document.getElementById('resultado').innerHTML;
    document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length - 1);

}

function calcular() {
    var resultado = document.getElementById('resultado').innerHTML;
    if (resultado) {
        document.getElementById('resultado').innerHTML = eval(resultado);
    }
    else {
        document.getElementById('resultado').innerHTML = 0.0;
    }
}
~~~



