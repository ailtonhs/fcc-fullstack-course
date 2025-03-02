# Revisão de variáveis e tipos de dados JavaScript

## Trabalhando com HTML, CSS e JavaScript

Enquanto HTML e CSS fornecem estrutura para sites, JavaScript traz interatividade aos sites ao permitir funcionalidades complexas, como manipular entradas do usuário, animar elementos e até mesmo criar aplicativos web completos.

## Tipos de dados em JavaScript

Os tipos de dados ajudam o programa a entender o tipo de dado com qual está trabalhando, seja um número, texto ou outra coisa.

* Number: Um número representa tanto inteiros quanto valores de ponto flutuante. Exemplos de inteiros incluem 7, 19, e 90.

* Ponto flutuante: Um número de ponto flutuante é um número coom um ponto decimal. Exemplos incluem 3,14, 0,5 e 0,0001.

* String: Uma string é uma sequência de caracteres, ou texto, entre aspas. 'Eu gosto de codificação' e "JavaScript é divertido" são exemplos de strings.

* Boolean: Um boolean representa um de dois valores possíveis: true ou false. Você pode usar um boolean para representar um condição, como isLoggedin = true.

* Undefined e Null: Um undefined valor é uma variável que foi declarada, mas não recebeu um valor. Um null valor é um valor vazio, ou uma variável que recebeu intencionamente um valor de null.

* object: Um object é uma coleção de pares chave-valor. A chave é o nome da propriedade, e o valor é o valor da propriedade.

Aqui, o pet object tem três propriedade ou chaves: name, age, e type. Os valores são Fluffy, 3, e dog, respectivamente.

```JavaScript
let pet = {
    name: 'Fluffy',
    age: 3,
    type: 'dog'
};
```

* Symbol: O tipo de dado Symbol é um valor único e imutável que pode ser usado como um identificador para propriedade de objects.

Neste exemplo abaixo, dois Symbol são criado com a mesma descrição, mais não são iguais.

```JavaScript
const cryptickey1 = Symbol("saltNpepper");
const cryptickey2 = Symbol("saltNpepper");
console.log(cryptickey1 === cryptickey2); //false
```

*BigInt: Quando o número é muito grande para o Number tipo de dado, você pode usar o tipo de dado BigInt para representar inteiros de comprimento arbitrário.

Ao adicionar um n ao final do número, você pode criar um BigInt.

```JavaScript
const veryBigNumber = 1234567890123456789012345678901234567890n;
```

## variáveis em JavaScript

* variáveis podem ser declaradas usando a let palavra-chave.

```JavaScript
let cityName;
```

* Para atribuir um valor a uma variável, você pode usar o operador de atribuição =.

```JavaScript
cityName = 'New York';
```

* variáveis declaradas usando let podem receber um novoo valor novamente.

```JavaScript
cityName = 'Los Angeles';
console.log(cityName); //Los Angeles
```

* Além de let, você também pode usar const para declarar uma variável. No entanto, uma const variável não pode ter um novo valor reatribuído.

```JavaScript
const cityName = 'New York';
cityName = 'Los Angeles'; //TypeError
```
* Variáveis declaradas usando const são usadas na declaração de constantes, que não podem mudar ao longo do código, como PI ou MAX_SIZE.

## Convenções de nomenclatura de variáveis

* Os nomes das variáveis devem ser descritivos e significativos.

* Os nomes das variáveis devem ser camelCase como cityName, isLoggedin, e veryBigNumer.

* Os nomes de variáveis não devem começar com um número. Eles devem começar com uma letra, _ ou $.

* Os nomes de variáveis não devem conter espaços ou caracteres especiais, exceto _ e $.

* Nomes de variáveis não devem ser palavra-chave reservada.

* Os nomes de variáveis diferenciam maiúsculas de minúsculas age e Age são variáveis diferentes.

## String e imutabilidade de strings em JavaScript

* Strings são sequências de caracteres entre aspas. Elas podem ser criadas usando aspas simples e duplas.

```JavaScript
let correctWay = 'This is a string';
let alsoCorrect = 'This is also a string';
```

* Strings são imutáveis em JavaScript. Isso significa que, uma vez que uma string é criada, você não pode alterar os caracteres na string. No entanto, você ainda pode reatribuir strings a um novo valor.

```JavaScript
let firstName = 'John';
firstName = 'Jane';
```

## Concatenação de strings em JavaScript

* Concatenação é o processo de juntar múltiplas strings ou combinar strings com variáveis que contêm texto. O operador + é um dos métodoos mais simples e mais frequentemente usados para concatenar strings.

```JavaScript
let studentName = 'Asad';
let studentAge = 25;
let studentInfo = studentName + ' is ' + studentAge + ' years old.';
console.log(studentInfo); // Asad is 25 years oold.
```

* Se você precisar adicionar ou anexar a uma string existente, então você pode usar o += operador. Isso é útil quando você quer construir sobre uma string adicionando mais texto a ela ao longo do tempo.

```JavaScript
let message = 'Welcome to programming, ';
message += 'Asad!';
console.log(message); //Welcome to programming, Assad!
```

* Outra maneira de concatenar strings é usar o método concat(). Este método une duas ou mais strings.

```JavaScript
let firstName = 'John';
let lastName = 'Doe';
let fullName = firstName.concat(' ', lastName);
console.log(fullName); //John Doe
```

## Registrando mensagens com console.log()

* O método console.log() é usado para registrar mensagens no console. É uma ferramenta útil para depurar e testar seu código.

```JavaScript
console.log('Hello, world!');
```

## Ponto e vírgula em JavaScript

* Ponto e vírgula são usados principalmente para marcar o fim de uma declaração. Isso ajuda o mecanismo JavaScript a entender a separação de instruções individuais, o que é crucial para a execução correta.
```JavaScript
let message = 'Hello, World';
let number = 42;
```
* Ponto e vírgula ajudam a evitar ambiguidades na execução do código e garantem que as instruções sejam encerradas corretamente.

## Comentários em JavaScript

* Qualquer linha de código que seja comentada é ignorada pelo mecanismo JavaScript. Comentários são usados para explicar código, fazer anotações ou desabilitar código temporariamente.

* Comentários de linha única são criados usando //.

```JavaScript
//Este é um comentário de linha única e será ignorado pelo mecanismo JavaScript
```

* Comentários multilinha são criados usando /* para iniciar o comentário e */ para finalizá-lo.

```JavaScript
/*Este é um comentário de multilinha. 
pode abrager várias linhas*/
```

## JavaScript como uma linguagem dinamicamente tipada

* JavaScript é uma linguagem dinamicamente tipada, o que significa que você não precisa especificar o tipo de dado de uma variável quando a declara. O mecanismo JavaScript determina automaticamente o tipo de dado com base no valor atribuído à variável.
```JavaScript
let error = 404; // aqui erro é number
erro = 'Not Found'; // agora erro é string
```
* Outras linguagens, como Java, que não são tipadas dinamicamente, resultariam em um erro:

```Java
int error = 404; // O valor deve ser sempre um número inteiro
error = 'Not Found'; // Isso causaria um erro em Java
```

## Usando o typeof operador

* O operador typeof é usado para verificar o tipo de dado de uma variável. Ele retorna uma string indicando o tipo da variável.

```JavaScript
let age = 25;
console.log(typeof age); //number


let isLoggedin = true;
console.log(typeof isLoggedin); //boolean
```

* No entanto, há uma peculidade bem conhecida em JavaScript quando se trata de null. O operador typeof retorna object para null valores.

```JavaScript
let user = null;

console.log(typeof user); //object
```