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

