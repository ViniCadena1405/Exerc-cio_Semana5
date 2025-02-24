# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

a) Imprime os números pares de 1 a 10. X

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10.

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

A) let carro = new Carro("Toyota"); X

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

A) 18 X

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

A) ![Uma imagem](assets/ex04_1.PNG) X

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

A) ![Uma imagem](assets/ex05_1.PNG) X

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

A) "Olá, meu nome é João. Olá, meu nome é Maria." X

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** 

class Animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`Nome: ${this.nome}, Idade: ${this.idade}`)
    }
}

let animal1 = new Animal("Cachorro", 10);
let animal2 = new Animal("Gato", 5);

animal1.descrever();
animal2.descrever();

______

**8)** 

class Animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`Nome: ${this.nome}, Idade: ${this.idade}`)
    }
}

class Gato extends Animal {
    constructor(nome, idade, cor) {
        super(nome, idade);
        this.cor = cor;
    }

    miar() {
        console.log("Miau!!!")
    }
}

let cachorro = new Animal("Cachorro", 10);
let gato = new Gato("Gato", 5, "Preto");

cachorro.descrever();
gato.descrever();
gato.miar();


______

**9)** 

class SomadordeNotas {
    constructor(total = 0) {
        this.total = total
    }

    adicionarNota(nota) {
        this.total += nota
    }

    verTotal() {
        console.log(`Nota: ${this.total}`);
    }
}

let somador = new SomadordeNotas();
somador.adicionarNota(6);
somador.adicionarNota(3);
somador.verTotal();


______

**10)** 

class Funcionário {
    constructor(nome, idade, salárioBase) {
        this.nome = nome;
        this.idade = idade;
        this.salárioBase = salárioBase;
    }
}

class Professor extends Funcionário {
    constructor(nome, idade, salárioBase, disciplina, horaSemana) {
        super(nome, idade, salárioBase);
        this.disciplina = disciplina;
        this.horaSemana = horaSemana;
    }

    //Cálculo do salário

    calcularSalário(aula) {
        this.salárioBase = (this.horaSemana * (this.horaSemana / aula)).toFixed(2);
        console.log(`Salário de ${this.nome}: ${this.salárioBase}`);
    }
}

let professor1 = new Professor("Mario", 55, 25, "Matemática", 5);
let professor2 = new Professor("Joana", 35, 20, "Física", 7);

professor1.calcularSalário(3);
professor2.calcularSalário(5);
