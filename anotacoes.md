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
