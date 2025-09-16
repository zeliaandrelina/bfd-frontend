*Aula 09.09.2025

ex1:
let nome = "Helio";
console.log(Number(nome));*/

/*const user = {
    perfil: {
    
    },
};
user?.perfil?.nome;

ex2:
const livro = {
    titulo: "Js Lindo",
    autor: "Machado de Assis",
};

const { titulo, autor: autorDolivro } = livro;

const arr = [10, 20, 30, 40];
const [a, b, c, d] = arr; // a= 10, b = 20

const [, , , x] = arr;

console.log(x);

//Resto dos itens
const [head, ...tail] = arr;

console.log(head);
console.log(tail);



ex3:
//criar o terceiro objeto que junta (... spread operator)

const pessoa = {
    nome: "Zélia",
    idade: 45,
};
const profissao = {
    funcao: "Analista Financeira",
};

const novoObjeto = { ...pessoa, ...profissao };
console.log(novoObjeto);

{ nome: 'Zélia', idade: 45, funcao: 'Analista Financeira' }


ex4:
//forma de criar objeto
function Person(first, last, age, eye) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eye;
}
const p1 = new Person("Helio", "Filho", 40, "brown");
console.log(p1);




*Aula 11.09.2025
////varer um item usando o for classico //for estrutura de repetições
//const frutas = ["maça", "banana", "uva"]; // vetor ou array
////for classico
//for (let i = 0; i < frutas.length; i++) {
//    //quando eu vou parar
//    console.log(`Fruta ${i}: ${frutas[i]}`);
//    //Fruta 0: maça
//    //Fruta 1: banana
//    //Fruta 2: uva
//}

//// for of
//for (... of ..){}
//
//const frutasObj = {
//    nome: "laranja", //chave ou propriedade:"valor"
//    tipo: "citrica",
//    valor: 5,
//};
////for in (intera por chave)
//
//console.log(frutasObj);

//push serve para inserir os valores
//const arrayNumbers = [];
//while (let value = 10; value <= 10; value -= 1) {
//    arrayNumbers.push(value);
//    console.log(value);
//}

////const frutasObj = {
////    nome: "laranja", //chave ou propriedade:"valor"
////    tipo: "citrica",
////    valor: 5,
////};
//////for in (intera por chave)
//
//console.log(frutasObj[chave]);

//const numbers = [10, 20, 30, 40, 50];
//for (const index in numbers) {
//    console.log(numbers[index]);
//}

//const frutasObj = {
//    "nome": "laranja", //chave ou propriedade:"valor"
//    "variedades":{
//        variedade1: "pera"
//        variedade2: "mimo"
//    },
//    "tipo": "citrica",
//    "valor": 5,
//}
//for(chave in frutasObj){
//    console.log(chave + "-" + frutasObj[chave])
//}

//const frutasObj = {
//    nome: "laranja", //chave ou propriedade:"valor"
//    variedades: {
//        variedade1: "pera",
//        variedade2: "mimo",
//    },
//    tipo: "citrica",
//    valor: 5,
//};
//for (chave in frutasObj) {
//    console.log(chave + "-" + frutasObj[chave]);
//}

//// imprimir frutas e o index
//const frutas = ["maça", "banana", "uva"];
//
//frutas.forEach((fruta, index) => {
//    console.log(`fruta: ${index}`);
//});

//function ListaFrutas() {
//    const frutas = ["maça", "banana", "uva"];
//
//    return (
//        <ul>
//            {[...frutas].sort().map((fruta, index) => (
//                <li key={index}> {fruta}</li>
//            ))}
//        </ul>
//    );
//}

ex:
//const numeros = [1, 2, 3, 4];
//
////map - cada elemento dobrado
////transformação de dados
//soma = numeros.reduce((acumulador, n) => acumulador + n, 0);
//console.log(soma);

ex:
//arrow function retornar o cubo de valor 
const numeros = [1, 2, 3, 4];
const cubo = numeros.map((n) => n * n * n);
console.log(cubo);


//Aula 16.09.2025

//ex1:
const users = [
    {
        name: "Ana Souza",
        age: 28,
        contact: "55 11 91234-5678",
        city: "São Paulo",
    },
    {
        name: "Carlos Mendes",
        age: 15,
        contact: "55 11 99876-5432",
        city: "São Paulo",
    },
    {
        name: "Fernanda Lima",
        age: 12,
        contact: "55 31 98765-4321",
        city: "Belo Horizonte",
    },
    {
        name: "Mariana Costa",
        age: 25,
        contact: "55 71 99888-1122",
        city: "Salvador",
    },
];
//objeto: vazio = {}
//callback: (acc, user) => {...}

const contagem = users.reduce((acc, user) => {
    // Se a cidade ainda não existe no acumulador, inicializa com 0
    if (!acc[user.city]) {
        acc[user.city] = 0;
    }

    // Incrementa 1 para essa cidade
    acc[user.city] += 1;

    // Retorna o acumulador atualizado para a próxima iteração
    return acc;
}, {});

console.log(contagem);


//ex2:
const users = [
    {
        name: "Ana Souza",
        age: 28,
        contact: "55 11 91234-5678",
        city: "São Paulo",
    },
    {
        name: "Carlos Mendes",
        age: 15,
        contact: "55 11 99876-5432",
        city: "São Paulo",
    },
    {
        name: "Fernanda Lima",
        age: 12,
        contact: "55 31 98765-4321",
        city: "Belo Horizonte",
    },
    {
        name: "Mariana Costa",
        age: 25,
        contact: "55 71 99888-1122",
        city: "Salvador",
    },
];
//objeto: vazio = {}
//callback: (acc, user) => {...}

const somaDasIdades = users.reduce((acc, user, index, array) => {
    acc += user.age;
    if (index === array.length - 1) {
        return acc / array.length;
    }
    return acc;
}, 0);
console.log(somaDasIdades);
//const mediaDasIdades = somaDasIdades / users.length;

//ex3:

const users = [
    {
        name: "Ana Souza",
        age: 28,
        contact: "55 11 91234-5678",
        city: "São Paulo",
    },
    {
        name: "Carlos Mendes",
        age: 15,
        contact: "55 11 99876-5432",
        city: "São Paulo",
    },
    {
        name: "Fernanda Lima",
        age: 12,
        contact: "55 31 98765-4321",
        city: "Belo Horizonte",
    },
    {
        name: "Mariana Costa",
        age: 25,
        contact: "55 71 99888-1122",
        city: "Salvador",
    },
];

// Filtra os usuários com idade maior ou igual a 25 anos
const maiorQueVinteCinco = users.filter((user) => user.age >= 25);

// Exibe no console o array com os usuários filtrados
console.log(maiorQueVinteCinco);



