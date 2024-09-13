# Exerc-cio-de-Log-ca
Lógica de Programação Senai 
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Foco no Sucesso📘</title>
</head>
<body style="text-align: center;">
    <h1>Logica de Progamação</h1> 
    <p>Foca</p> 
    <label for="nome">Nome</label>
    <input id="nome" type="text" placeholder="Ex:Ulisses Santos"><br> 
    <button onclick="boasVindas()">Clique aqui</button><br>
    <button onclick="parOuImpar()">Par ou Impar</button><br>
    <button onclick="conversao()">Temperatura</button><br>
    <button onclick="media()">Media</button><br>
    <button onclick="pesca()">Pesca</button><br>
    <button onclick="volume()">Moveis Sobremedida</button>
    

    <script>
        function boasVindas(){
            let nome = document.getElementById("nome").value;
            let ano = prompt("Bem vindo, " +nome+"! Digite seu ano de nascimento");
            if(2024 - ano >17){
                alert("Portanto tu éish maior de idade, poish teinx "+(2024-ano)+" anos");
            } 
            else  {
                alert("Portanto tu éish menor de idade, poish teinx "+(2024-ano)+" anos");
            }
        } 

        function parOuImpar(){
        let n = prompt("Digite um numero ");
        if(n % 2 == 0){
            alert ("E par!!");
        }
        else  {
            alert ("E impar!!");
        }

        }

        function conversao(){
            let opcao = prompt("Seja benvindo, que conversão deseja fazer: \n 1- Celcius para Fahrenheit \n 2- Fahrenheit para Celsius \n 3- Celcius para Kelvin \n 4- Kelvin para Celcius \n 5- Fahrenheit para Kelvin \n 6- Kelvin para Fahrenheit ");
            
        if (opcao ==1) {
            let t = prompt ("Digite a temperatura em Celcius: ");
            let r = (t*1.8)+32 ;
            alert ("A temperatura em Fahrenheit é: "+r );
        } 
        else if (opcao ==2) {
            let t = prompt ("Digite a temperatura em Fahrenheit: ");
            let r = ((t-32) * (5/9));
            alert ("A temperatura em Celcius e: "+r );
        }
        else if (opcao ==3) {
            let t = prompt ("Digite a temperatura Celcius:");
            let r = t+273.15;
            alert ("A temperatura em Kelvin é: "+r);
        }
        else if (opcao ==4) {
            let t = prompt ("Digite a temperatura em Kelvin:");
            let r = t-273.15;
            alert ("A temperatura em Celcius é:"+r);
        }
        else if (opcao==5) {
            let t = prompt ("Digite a temperatura em Fahrenheit:");
            let r = ((t - 32) * (5/9)) + 273.15;
            alert ("A temperatura em Kelvin é:"+r);
        }
        else if (opcao==6) {
            let t = prompt ("Digite a temperatura em Kelvin:");
            let r = (t - 273.15) * (9/5) + 32;
            alert ("A temperatura em Fahrenheit e:"+r);
        }
        else { alert ("Opcao Invalida");
        }
        }
  
        

        function media(){
        let n1 = Number( prompt("Digite o valor do primeiro número: ")) ;
        let n2 = Number( prompt("Digite o valor do segundo número: "));
        alert("A media é: "+(n1 + n2)/2);
       }

       function pesca(){
        let pesoPermitido = prompt("Digite o peso permitido:");
        let quantPes = prompt("Digite o peso pescado: ");
        let multaPorPeso = prompt("Digite a multa por excesso: ");
        
        if (quantPes > pesoPermitido){
        let diferenca= quantPes - pesoPermitido;
        let multa = (diferenca * multaPorPeso);
        alert ("O peso excedeu em: "+diferenca+"kg , portanto deverá pagar multa de R$ "+multa);
       }
        else { 
            alert ("O peso esta dentro do limite permitido, portanto nao precisa pagar multa.");
        }
       }

       function volume(){
       let a = prompt("Digite a altura: ");
       let c = prompt("Digite o comprimento: ");
       let l = prompt("Digite a largura: ");
       alert ("O volume do seu movel e: "+(a*c*l));
       }

    </script>
</body>
</html>
