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



//ex4:
// Função saudacao recebe um parâmetro 'nome'
function saudacao(nome) {
    // Cria uma mensagem personalizada usando template string
    const mensagem = `olá, ${nome}`;

    // Define uma função interna que acessa a variável 'mensagem'
    function mostrarSaudacao() {
        console.log(mensagem); // Imprime a mensagem no console
    }

    // Retorna a função interna sem executá-la ainda
    return mostrarSaudacao;
}

// Cria uma constante que armazena a função retornada por saudacao
const olaHeitor = saudacao("Heitor");

// Executa a função armazenada, que imprime "olá, Heitor"
olaHeitor();


Aula 18.09.2025

Ex1:
// Declara um objeto JavaScript chamado 'usuario' com três propriedades
const usuario = {
    // id do usuário
    id: 1,
    // nome do usuário
    nome: "Maria",
    // indica se o usuário está ativo ou não (booleano)
    ativo: true,
};

// Converte o objeto 'usuario' para uma string no formato JSON
const jsonString = JSON.stringify(usuario);

// Exibe o objeto original no console (ainda como objeto JS, não como string JSON)
console.log(usuario);


//JSON.stringify(usuario) transforma o objeto em uma string JSON como esta: {"id":1,"nome":"Maria","ativo":true}
//console.log(usuario) imprime o objeto original, e não a string convertida.


Ex2:
// Declaração de um objeto JavaScript chamado 'usuario'
const usuario = {
    // Comentário indicando que é um objeto JS
    // Propriedade 'id' com valor numérico 1
    id: 1,
    // Propriedade 'nome' com valor string "Maria"
    nome: "Maria",
    // Propriedade 'ativo' com valor booleano true
    ativo: true,
};

// Converte o objeto 'usuario' em uma string JSON formatada
// Parâmetros:
// - usuario: o objeto a ser convertido
// - null: sem função de substituição (replacer)
// - 4: número de espaços usados para identação (formatação mais legível)
const jsonString = JSON.stringify(usuario, null, 4);

// Exibe a string JSON formatada no console
console.log(jsonString);


Ex3:
// Declaração de um objeto JavaScript chamado 'usuario'
const usuario = {
    // Comentário indicando que é um objeto JS
    id: 1,                   // Propriedade numérica
    nome: "Maria",           // Propriedade string
    ativo: true,             // Propriedade booleana
};

// Converte o objeto 'usuario' em uma string JSON
const jsonString = JSON.stringify(usuario);

// Exibe a string JSON no console
console.log(jsonString);    // Resultado: '{"id":1,"nome":"Maria","ativo":true}'

// Declara uma string que simula um JSON recebido de alguma fonte externa (ex: API, arquivo, etc.)
const jsonRecebido = '{"id":1, "nome": "Maria", "ativo": true}';

try {
    // Tenta converter (parsear) a string JSON para um objeto JavaScript
    const dados = JSON.parse(jsonRecebido);

    // Acessa e exibe a propriedade 'nome' do objeto convertido
    console.log(dados.nome);    // Resultado: "Maria"

    // Acessa e exibe a propriedade 'ativo' do objeto convertido
    console.log(dados.ativo);   // Resultado: true

} catch (e) {
    // Em caso de erro ao fazer o parse (ex: JSON malformado), exibe mensagem de erro no console
    console.error("Erro ao processar json:", e.message);
}


//O que esse código faz no geral:
//Cria um objeto JavaScript (usuario).
//Converte esse objeto para o formato JSON (string).
//Simula o recebimento de uma string JSON (jsonRecebido).
//Usa JSON.parse() para converter essa string de volta em objeto JS.
//Acessa propriedades do objeto convertido (nome e ativo).
//Usa um bloco try...catch para tratar possíveis erros caso o JSON esteja malformado.

ex4:
// Comentário indicando que será feita uma requisição GET
//GET

// Declaração de uma função assíncrona chamada 'buscarUsuarios'
async function buscarUsuarios() {
    try {
        // Faz uma requisição HTTP GET para o endpoint da API
        const res = await fetch("https://jsonplaceholder.typicode.com/users/");

        // Verifica se a resposta da requisição não foi bem-sucedida (status diferente de 200–299)
        if (!res.ok) {
            // Lança um erro com o código de status HTTP
            throw new Error(`Erro HTPP: ${res.status}`);
        }

        // Converte o corpo da resposta em JSON (aguarda a conversão)
        const dados = await res.json();

        // Exibe os dados obtidos no console
        console.log(dados);

    } catch (erro) {
        // Caso ocorra algum erro (na requisição ou no parse), exibe mensagem de erro no console
        console.error("Erro ao buscar usuarios:", erro.message);
    }
}

// Chamada da função 'buscarUsuarios' para iniciar a requisição
buscarUsuarios();

//O que esse código faz no geral:
//Usa fetch() para fazer uma requisição GET para a URL da API jsonplaceholder, que retorna uma lista de usuários fictícios.
//Usa await para esperar a resposta e depois converter o resultado para JSON.
//Se a resposta não for OK (por exemplo, 404 ou 500), lança um erro personalizado.
//Se tudo correr bem, imprime os dados no console.
//Se algo der errado (erro de rede, erro no JSON, etc.), o catch captura e mostra a mensagem de erro.


Ex5:
// Declaração de uma função assíncrona chamada 'buscarUsuarios', que recebe um parâmetro 'id'
async function buscarUsuarios(id) {
    try {
        // Faz uma requisição HTTP GET para a API, usando o ID recebido na URL
        const res = await fetch(
            `https://jsonplaceholder.typicode.com/users/${id}`
        );

        // Verifica se a resposta da requisição foi bem-sucedida (códigos 200–299)
        if (!res.ok) {
            // Se não for, lança um erro com o código de status da resposta
            throw new Error(`Erro HTPP: ${res.status}`);
        }

        // Aguarda a conversão do corpo da resposta para JSON
        const dados = await res.json();

        // Exibe no console apenas o nome do usuário retornado
        console.log("nome:", dados.name);

        // Linha comentada que poderia exibir todo o objeto de dados recebido
        // console.log(dados);

    } catch (erro) {
        // Se ocorrer qualquer erro (na requisição ou no parse), exibe uma mensagem no console
        console.error("Erro ao buscar usuarios:", erro.message);
    }
}

// Chamada da função, passando o ID do usuário que deseja buscar (nesse caso, 1)
buscarUsuarios(1);


//O que esse código faz:
//Acessa a API pública jsonplaceholder.typicode.com para buscar o usuário com o ID informado.
//Se o usuário com o ID existir, exibe no console o nome dele.
//Se ocorrer erro (ex: ID inválido, sem internet, erro da API), exibe uma mensagem de erro.


Ex6:
// GET

// Função assíncrona que busca dados de um usuário por ID
async function buscarUsuarios(id) {
    try {
        // Faz a requisição GET para a API, com o ID especificado
        const res = await fetch(
            `https://jsonplaceholder.typicode.com/users/${id}`
        );

        // Verifica se a resposta não foi bem-sucedida (status fora da faixa 200-299)
        if (!res.ok) {
            throw new Error(`Erro HTTP: ${res.status}`);
        }

        // Converte o corpo da resposta em JSON
        const dados = await res.json();

        // Verifica se o objeto retornado está vazio (usuário não encontrado)
        if (!dados.name) {
            throw new Error("Usuário não encontrado.");
        }

        // Exibe no console o nome do usuário
        console.log("nome:", dados.name);

        // (Opcional) Exibir todos os dados
        // console.log(dados);

    } catch (erro) {
        // Trata erros de conversão JSON (não acontece nesse exemplo, mas é uma boa prática)
        if (erro.name === "SyntaxError") {
            console.error("Erro ao converter JSON:", erro.message);
        }

        // Exibe qualquer outro erro ocorrido
        console.error("Erro ao buscar usuário:", erro.message);
    }
}

// Chamada da função com um ID inválido (-1)
buscarUsuarios(-1);






