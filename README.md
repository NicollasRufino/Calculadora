# Calculadora
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
</head>
<style>
  *{
      margin: 0;
      padding: 0;
  }
  .fundo{
      background-image: linear-gradient(45deg, yellow, blue );
    height: 100vh;
    color: azure;
    font-family:'Courier New', Courier, monospace;
    text-align: left;
}

    .calculadora{
        position:absolute;
        background-color: rgba(0,0,0,1);
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        border-radius: 15px;
        padding: 15px;
    }
    .botao{
        width: 50px;
        height: 50px;
        font-size: 25px;
        cursor: pointer;
        margin: 3px;
        background-color: rgb(31, 31,31);
        border: none;
        color:#fff;
    }
    .botao:hover{
        background-color: black;
    }
    #resultado{
        background-color: #fff;
        width: 226px;
        height:30px;
        margin: 5px;
        font-size: 25px;
        color: black;
        text-align: right;
    }

</style>
<body>
    <div class="fundo">
        <h1> Nicollas E Igor</h1>
        <h1> Calculadora Semi Cientifica</h1>
        <p id="resultado"></p>
        <table>
            <td><button class="botao" onclick=clean() >C</button></td>
            <td><button class="botao" onclick="insert('7')" ><</button></td>
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
            <td><button class="botao">^</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('7')">%</button></td>
            <td><button class="botao" onclick="insert('±')">±</button></td>
            <td><button class="botao" onclick="insert(',')">,</button></td>
            <td><button class="botao" onclick=calcular()>=</button></td>
        </tr>
        <tr>
            <td colspan="4" ><button class="botao" style="width: 206px;" onclick="insert('0')">0</button></td>
        <tr>
        </table>
    </div>
</div>
<script>     
            function insert()
            {
                var resultado = document.getElementById('resultado').innerHTML;
                document.getElementById('resultado').innerHTML = numero + num;
            }       
            function clean(){
                document.getElementById('resultado').innerHTML =""
            }
            function back()
            {
                var resultado = document.getElementById('resultado').innerHTML;
              document.getElementById('resultado').innerHTML = resultado.substring(0,resultado.length, -1)
             
                
            }
            function calcular()
            {
                var resultado = document.getElementById('resultado').innerHTML;
              if(resultado){

                document.getElementById('resultado').innerHTML = eval(resultado)
              }
             else
             {
                 document.getElementById('resultado').innerHTML = "ERROR"
             }
                
            }
</script>
</body>
</html>

//Nicollas e Igor, dps de muitos erros deu certo
