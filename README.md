# PHP-exercicios

### 1 . Faça uma função que calcule se um número é positivou, negativo ou nulo. Após isso, mostrar o resultado
```
<?php
function calcular() {
    $num = readline("insira um número: ");
    
    if ($num>0) {
        echo "este número é positivo";
    }
    if ($num<0) {
        echo "este número é negativo";
    }
    if ($num==0) {
    echo "este número é nulo";
    }
}

calcular()
?>
```

### 2 . Faça uma função que mostre os números de 1 a 10 usando for
```
<?php
function calcular() {
    for ($i=1;$i<11;$i++){
        $i==$i+1;
        echo "$i, ";
    }
}
echo "números de 1 a 10:\n";
calcular()
?>
```

### 3 . Faça uma função que numere uma lista de objetos.

```
<?php
function calcular() {
    $frutas = array( "limão", "tangerina", "uva", "mamão", "maçã"
        );
    for ($i=0 ;$i<count($frutas); $i++){
    echo ($i + 1) . ". " . $frutas[$i] . "\n";
    }
}
calcular()
?>
```
### 4 . Faça um foreach que mostre os dados de uma pessoa.

```
<?php
$pessoa = array(
    "nome" => "John Doe",
    "idade" => 30,
    "cidade" => "Ohio",
    "profissao" => "Golpista"
);

extract($pessoa);

foreach ($pessoa as $key => $value) {
    if ($key == "nome") {
        echo "Seu nome é: $value\n";
    }
    if ($key == "idade") {
        echo "Sua idade é: $value\n";
    }
    if ($key == "cidade") {
        echo "Sua cidade é: $value\n";
    }
    if ($key == "profissao") {
        echo "Sua profissão é: $value\n";
    }
}
?>
```
### 5 . Usando um array de arrays, faça um foreach que mostre com uma frase se a pessoa selecionada do array pode dirigir, baseado em sua idade.

```
<?php
$pessoas = array(
    array(  "nome" => "João",
            "idade" => 19,
            "cidade" => "Campinas"
            ),
    array(  "nome" => "Pedro",
            "idade" => 16,
            "cidade" => "Sumaré"
            ),
    array(  "nome" => "José",
            "idade" => 18,
            "cidade" => "Ribeirão Preto"
            )
);
foreach ($pessoas as $pessoa) {
    
    if ($pessoa["idade"] >= 18) {
        $pode_dirigir = "pode";
    } else {
        $pode_dirigir = "não pode";
    }

    echo $pessoa["nome"] . " é de " . $pessoa["cidade"] . " e tem " . $pessoa["idade"] . " anos, logo, " . $pode_dirigir . " dirigir.\n";
}

?>
```
