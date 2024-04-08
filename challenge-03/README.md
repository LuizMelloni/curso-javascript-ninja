# Desafio da semana #3

```js
// Declarar uma variável qualquer, que receba um objeto vazio.
?

/*
Declarar uma variável `pessoa`, que receba suas informações pessoais.
As propriedades e tipos de valores para cada propriedade desse objeto devem ser:
- `nome` - String
- `sobrenome` - String
- `sexo` - String
- `idade` - Number
- `altura` - Number
- `peso` - Number
- `andando` - Boolean - recebe "falso" por padrão
- `caminhouQuantosMetros` - Number - recebe "zero" por padrão
*/
?

/*
Adicione um método ao objeto `pessoa` chamado `fazerAniversario`. O método deve
alterar o valor da propriedade `idade` dessa pessoa, somando `1` a cada vez que
for chamado.
*/
?
function fazerAniversario(){
    return pessoa.idade++;
}

/*
Adicione um método ao objeto `pessoa` chamado `andar`, que terá as seguintes
características:
- Esse método deve receber por parâmetro um valor que representará a quantidade
de metros caminhados;  
- Ele deve alterar o valor da propriedade `caminhouQuantosMetros`, somando ao
valor dessa propriedade a quantidade passada por parâmetro;
- Ele deverá modificar o valor da propriedade `andando` para o valor
booleano que representa "verdadeiro";
*/
?
function andar(a){
    metrosCaminhados = a;
    pessoa.caminhouQuantosMetros += metrosCaminhados;
    pessoa.andando = true;
}

/*
Adicione um método ao objeto `pessoa` chamado `parar`, que irá modificar o valor
da propriedade `andando` para o valor booleano que representa "falso".
*/
?
function parar(){
    pessoa.andando = false;
}

/*
Crie um método chamado `nomeCompleto`, que retorne a frase:
- "Olá! Meu nome é [NOME] [SOBRENOME]!"
*/
?
function nomeCompleto(){
    return 'Olá, meu nome é ' + pessoa.nome + ' ' + pessoa.sobrenome;
}

/*
Crie um método chamado `mostrarIdade`, que retorne a frase:
- "Olá, eu tenho [IDADE] anos!"
*/
?
function mostrarIdade(){
    return 'Eu tenho '+ pessoa.idade + ' anos';
}

/*
Crie um método chamado `mostrarPeso`, que retorne a frase:
- "Eu peso [PESO]Kg."
*/
?
function mostrarPeso(){
    return 'Eu peso ' + pessoa.peso + ' kg';
}

/*
Crie um método chamado `mostrarAltura` que retorne a frase:
- "Minha altura é [ALTURA]m."
*/
?
function mostrarAltura(){
    return 'Eu tenho ' + pessoa.altura + ' m de altura';
}

/*
Agora vamos brincar um pouco com o objeto criado:
Qual o nome completo da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?
nomeCompleto()
//Olá, meu nome é Luiz Melloni
/*
Qual a idade da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?
mostrarIdade()
// Eu tenho 21 anos
/*
Qual o peso da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?
mostrarPeso
// Eu peso 100 kg
/*
Qual a altura da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?
mostrarAltura()
// Eu tenho 1.85 m de altura
/*
Faça a `pessoa` fazer 3 aniversários.
*/
?
fazerAniversario()
fazerAniversario()
fazerAniversario()

/*
Quantos anos a `pessoa` tem agora? (Use a instrução para responder e
comentários inline ao lado da instrução para mostrar qual foi a resposta
retornada)
*/
?
// 25

/*
Agora, faça a `pessoa` caminhar alguns metros, invocando o método `andar` 3x,
com metragens diferentes passadas por parâmetro.
*/
?
andar(2)
andar(3)
andar(5)

/*
A pessoa ainda está andando? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?
console.log(pessoa.andando)
// true
/*
Se a pessoa ainda está andando, faça-a parar.
*/
?
parar()

/*
E agora: a pessoa ainda está andando? (Use uma instrução para responder e
comentários inline ao lado da instrução para mostrar a resposta retornada)
*/
?
console.log(pessoa.andando)
// false

/*
Quantos metros a pessoa andou? (Use uma instrução para responder e comentários
inline ao lado da instrução para mostrar a resposta retornada)
*/
?
console.log(pessoa.caminhouQuantosMetros)
// 10

/*
Agora vamos deixar a brincadeira um pouco mais divertida! :D
Crie um método para o objeto `pessoa` chamado `apresentacao`. Esse método deve
retornar a string:
- "Olá, eu sou o [NOME COMPLETO], tenho [IDADE] anos, [ALTURA], meu peso é [PESO] e, só hoje, eu já caminhei [CAMINHOU QUANTOS METROS] metros!"

Só que, antes de retornar a string, você vai fazer algumas validações:
- Se o `sexo` de `pessoa` for "Feminino", a frase acima, no início da
apresentação, onde diz "eu sou o", deve mostrar "a" no lugar do "o";
- Se a idade for `1`, a frase acima, na parte que fala da idade, vai mostrar a
palavra "ano" ao invés de "anos", pois é singular;
- Se a quantidade de metros caminhados for igual a `1`, então a palavra que
deve conter no retorno da frase acima é "metro" no lugar de "metros".
- Para cada validação, você irá declarar uma variável localmente (dentro do
método), que será concatenada com a frase de retorno, mostrando a resposta
correta, de acordo com os dados inseridos no objeto.
*/
?
pessoa.apresentacao = function() {
    var sexoCondicional = pessoa.sexo === "Feminino" ? 'a' : 'o';
    var idadeCondicional = pessoa.idade === 1 ? 'ano' : 'anos'
    var metrosCondicional = pessoa.caminhouQuantosMetros === 1 ? 'metro' : 'metros'

    return "Ola, sou " + sexoCondicional + " " + pessoa.nomeCompleto() + ", tenho " + pessoa.idade + " " + idadeCondicional + ", " + pessoa.altura + " m, e só hoje, caminhei " + pessoa.caminhouQuantosMetros + " " + metrosCondicional
} 

// Agora, apresente-se ;)
?
Ola, sou a Luiz Melloni, tenho 25 anos, 1.85 m, e só hoje, caminhei 10 metros
```
