# Lista da Atividade Ponderada

# Questôes alternativas

1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.

        console.log(x);
        var x = 5;
        console.log(y);
        let y = 10;

**a) A saída será undefined seguido de erro**

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

Justificativa: O erro do código acontece pois um "console.log" não pode mostrar uma variável que ainda não foi declarada. Dessa forma, para resolver esse código, é nes=cessário declarar a variável antes de tentar imprimí-la.

2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.

        function soma(a, b) {
            if (a || b === 0) {
                return "Erro: número inválido";
            }
            return a + b;
        }
        console.log(soma(2, 0));

**a) Substituir if (a || b === 0) por if (a === 0 || b === 0)**

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

Justificativa: A substituição deve acontecer para que o código funcione pois if (a || b === 0) verifica se a é truthy OU b === 0, mas isso não verifica corretamente se algum dos dois valores é zero.

3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.

        function calcularPreco(tipo) {
            let preco;

            switch(tipo) {
                case "eletrônico":
                    preco = 1000;
                case "vestuário":
                    preco = 200;
                    break;
                case "alimento":
                    preco = 50;
                    break;
                default:
                    preco = 0;
            }

            return preco;
        }

        console.log(calcularPreco("eletrônico"));

a) O código imprime 1000.

**b) O código imprime 200.**

c) O código imprime 50.

d) O código gera um erro.

Justificativa: O código imprime 200 pois é o próximo caminho depois do case("eletrônico). O correto seria a impressão do valor 1000 do primeiro case, mas como ele não apresenta um break, o código acaba lendo o próximo case.

4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.

        let numeros = [1, 2, 3, 4, 5];

        let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

        console.log(resultado);
a) 0

b) 6

c) 18

**d) 24**

Justificativa: O código multiplica todos os elementos do array por 2, em seguida verifica os resultados que são maiores do que 5 e por fim os soma e imprime o resultado

5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.

        let lista = ["banana", "maçã", "uva", "laranja"];
        lista.splice(1, 2, "abacaxi", "manga");
        console.log(lista);

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

**c) ["banana", "abacaxi", "manga", "laranja"]**

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

Justificativa: A função "lista.splice" realiza uma troca dos elementos de posição 1 e 2 por "abacaxi" e "manga". Dessa forma, obtemos a resposta "C".

6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.

II. Em JavaScript, a herança é implementada através da palavra-chave extends.

**a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.**

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

Justificativa: A segunda afirmação justifica a primeira pois apresenta um mecanismo concreto que permite o funcionamento da herança.

7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.

        class Pessoa {
        constructor(nome, idade) {
            this.nome = nome;
            this.idade = idade;
        }

        apresentar() {
            console.log(Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.);
        }
        }

        class Funcionario extends Pessoa {
        constructor(nome, idade, salario) {
            super(nome, idade);
            this.salario = salario;
        }

        apresentar() {
            super.apresentar();
            console.log(Meu salário é R$ ${this.salario}.);
        }
        }

I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.

II) O método apresentar() da classe Funcionario sobrepõe o método apresentar() da classe Pessoa, mas chama o método da classe pai usando super.

III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

**a) I e II são verdadeiras.**

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

Justificativa: A alternativa III é falsa pois contradiz toda a ideia de herança implementada em JavaScript no código.

8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.

Asserção: O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.
Razão: Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

**b) A asserção é verdadeira e a razão é falsa.**

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

Justificativa: A razão é falsa pois o JavaScript não suporta a sobrecarga de métodos, visto que se um método for definido várias vezes a última definição sobrescreve as anteriores.

# Questões dissertativas

9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.
function somaArray(numeros) {

        for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
        }
        return soma;
        }
        console.log(somaArray([1, 2, 3, 4]));

Resolução: 

    //Declara a função somaArray

    function somaArray(numeros) {

    //Declara a variável soma equivalente a 0 para armazenar a soma dos números

    let soma = 0;

    //Percorre o array de números e soma o dobro de cada número

    for (i = 0; i < numeros.length; i++) {

    //Soma o dobro do número atual ao valor da variável soma

     soma += (2*numeros[i]);
    }
    //Retorna a soma dos números
    return soma;
    }
    //Exporta a função somaArray
    console.log(somaArray([1, 2, 3, 4]));
    //Define os parâmetros da função somaArray

10) Crie um exemplo prático no qual você tenha duas classes:
Uma classe Produto com atributos nome e preco, e um método calcularDesconto() que aplica um desconto fixo de 10% no preço do produto.
Uma classe Livro que herda de Produto e modifica o método calcularDesconto(), aplicando um desconto de 20% no preço dos livros.
Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe Livro.

Resolução: 

    class Produto {
        constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
        }
  
    calcularDesconto() {
      console.log(Seu desconto é de R$ ${this.preco * 0.1}, logo o preço final é de R$ ${this.preco * 0.9}.);
    }
    }
    
    class Livro extends Produto {
        constructor(nome, preco, novoDesconto) {
        super(nome, preco);
        this.novoDesconto = novoDesconto;
        }
  
    calcularDesconto() {
      super.calcularDesconto();
      console.log(O novo desconto para o livro é de R$ ${this.preco * this.novoDesconto}, logo o preço final é de R$ ${this.preco * (1 - this.novoDesconto)}.);
    }
    }
    
    const livro = new Livro("JavaScript Avançado", 100, 0.2);
    livro.calcularDesconto();

//Resposta dissertativa para a questão:
//Para implementar a herança nesse código, defini que a classe Livro herdaria os atributos nome e preco da classe Produto, aproveitando assim a reutilização de código e evitando repetições desnecessárias. Como diferencial, a classe Livro modifica a lógica do método calcularDesconto(), aplicando um desconto maior do que o da classe Produto. Além disso, para tornar a saída mais intuitiva, a função calcularDesconto() exibe a equação do desconto aplicado, deixando claro como o preço final foi calculado.

