# objetivo do script:

## funções principais:

document.addEventListener("DOMContentLoaded", function(){loadTodos();})

garante que a função loadTodos() seja chamada quando o documento html
estiver completamente carregado, para que os elementos do DOM estejam disponiveis.

<hr></hr>

### loadTodos()
carrega a lista de tarefas do localStorage e as exibe na tela.
<br></br>
usa JSON.parse para converter os dados de String JSON de volta para um array.
<br></br>
cria elementos HTML para cada tarefa e os adiciona a lista.
<br></br>

<hr></hr>

### saveTodos()

Salva a lista de tarefas no localStorage.
<br></br>
Usa JSON.stringify para converter o array de tarefas em uma string JSON antes de salvar.

<hr></hr>

### createTodo(todo, index)

cria e retorna um elemento HTML para a tarefa adicionar funcionalidades de edição, salvamento, conclusão e exclusão.

<hr></hr>

### addTodo()

Adiciona uma nova tarefa à lista.
<br></br>
atualiza o localStorage com a nova lista de tarefas
<br></br>
recarrega a lista na tela

<hr></hr>

### updateTodoText(index, newText)

atualiza o texto de uma tarefa especifica e salva no localStorage

<hr></hr>

### updateTodoStatus(index, completed)

Atualiza o status de conclusão de uma tarefa especifica e salva no localStorage.

<hr></hr>

### deleteTodoItem(index)

remove uma tarefa da lista, atualiza o localStorage e recarrega a lista na tabela.

<hr></hr>

### função do localStorage

#### localStorage.getItem('todos');
recupera a lista de tarefas armazenada no localStorage como uma string JSON.

#### localStorage.setItem('todos', JSON.stringify(todos))
salva a lista de tarefas no localStorage como uma String JSON.

# funções de array utilizadas

#### JSON.parse(string):
converte uma String.JSON em um array de objetos.

#### JSON.stringify(array):
converte um array de objetos em uma String JSON.

#### Array.prototype.push(item):
adiciona um novo item ao final do array.

#### Array.prototype.slice(index, 1):
remove um item do array na posição especificada.

# Métodos de Array em JavaScriptAdição e Remoção de Elementos
push(element1, ..., elementN): Adiciona um ou mais elementos ao final do array e retorna o novo comprimento do array.

pop(): Remove o último elemento do array e retorna esse elemento.

unshift(element1, ..., elementN): Adiciona um ou mais elementos ao início do array e retorna o novo comprimento do array.

shift(): Remove o primeiro elemento do array e retorna esse elemento.
splice(start, deleteCount, item1, ..., itemN): Adiciona/remover elementos a partir de uma posição específica do array. Retorna um novo array contendo os elementos removidos.

Acesso e Pesquisa de Elementos

concat(array1, ..., arrayN): Retorna um novo array contendo todos os arrays ou valores passados como argumento.

slice(begin, end): Retorna uma cópia superficial de uma parte do array em um novo array.
indexOf(element, start): Retorna o primeiro índice onde o elemento pode ser encontrado no array, ou -1 se não estiver presente.

lastIndexOf(element, start): Retorna o último índice onde o elemento pode ser encontrado no array, ou -1 se não estiver presente.

includes(element, start): Determina se um array contém um determinado elemento, retornando true ou false.

Iteração e Transformação

forEach(callback): Executa uma dada função em cada elemento do array.
map(callback): Cria um novo array com os resultados da aplicação da função callback em cada elemento do array.

filter(callback): Cria um novo array com todos os elementos que passam no teste implementado pela função callback.

reduce(callback, initialValue): Aplica uma função acumuladora contra um acumulador e cada elemento do array (da esquerda para a direita) para reduzi-lo a um único valor.

reduceRight(callback, initialValue): Aplica uma função acumuladora contra um acumulador e cada elemento do array (da direita para a esquerda) para reduzi-lo a um único valor.
some(callback): Testa se ao menos um dos elementos no array passa no teste implementado pela função callback. Retorna true ou false.

every(callback): Testa se todos os elementos no array passam no teste implementado pela função callback. Retorna true ou false.

find(callback): Retorna o primeiro elemento do array que satisfaz a função callback. Caso contrário, retorna undefined.

findIndex(callback): Retorna o índice do primeiro elemento do array que satisfaz a função callback. Caso contrário, retorna -1.

Ordenação e Reversão

sort(compareFunction): Ordena os elementos do array e retorna o array.

reverse(): Inverte a ordem dos elementos do array no lugar. O primeiro elemento torna-se o último e o último torna-se o primeiro.

Outros Métodos Úteis

join(separator): Junta todos os elementos do array em uma string, separados por um separador especificado. Se não for especificado, o separador padrão é uma vírgula.

toString(): Retorna uma string representando o array especificado e seus elementos.

flat(depth): Retorna um novo array com todos os sub-arrays concatenados em um nível especificado.

flatMap(callback): Primeiro mapeia cada elemento usando uma função de mapeamento e, em seguida, achata o resultado em um novo array.

Exemplos de uso:

let fruits = ['apple', 'banana', 'cherry'];

// Adicionar elementos
fruits.push('date'); // ['apple', 'banana', 'cherry', 'date']
fruits.unshift('elderberry'); // ['elderberry', 'apple', 'banana', 'cherry', 'date']

// Remover elementos
fruits.pop(); // ['elderberry', 'apple', 'banana', 'cherry']
fruits.shift(); // ['apple', 'banana', 'cherry']

// Acessar e pesquisar elementos
let index = fruits.indexOf('banana'); // 1
let exists = fruits.includes('cherry'); // true

// Iteração e transformação
fruits.forEach(fruit => console.log(fruit)); // apple, banana, cherry
let uppercaseFruits = fruits.map(fruit => fruit.toUpperCase()); // ['APPLE', 'BANANA', 'CHERRY']

// Filtrar elementos
let filteredFruits = fruits.filter(fruit => fruit.startsWith('b')); // ['banana']

// Redução
let concatenatedFruits = fruits.reduce((acc, fruit) => acc + ' ' + fruit); // 'apple banana cherry'

// Ordenação e reversão
fruits.sort(); // ['apple', 'banana', 'cherry']
fruits.reverse(); // ['cherry', 'banana', 'apple']

// Outros métodos úteis
let fruitString = fruits.join(', '); // 'cherry, banana, apple'

# O Que é JSON?

é um formato de troca de dados leve e de fácil leitura para humanos e máquinas. É usado principalmente para transmitir dados entre um servidor e um cliente web como texto simples. JSON é uma linguagem independente, mas usa convenções familiares para programadores de linguagens C, como C++, C#, Java, JavaScript, Perl, Python, e muitas outras.Estrutura JSON
<br></br>
: Representados por {}, contêm um conjunto de pares chave-valor.
<br></br>
: Representados por [], contêm uma lista ordenada de valores.
<br></br>
: Podem ser strings, números, booleanos, nulos, objetos ou arrays.
<br></br>

## Exemplo de Uso

  Objeto JSON  
{
    "nome": "João",
    "idade": 30,
    "casado": true,
    "filhos": ["Ana", "Pedro"],
    "endereco": {
        "rua": "Rua Principal",
        "cidade": "São Paulo",
        "pais": "Brasil"
    }
}

  Array JSON[
    {
        "nome": "João",
        "idade": 30
    },
    {
        "nome": "Maria",
        "idade": 25
    }
]

Conversão entre JSON e Objetos JavaScriptConverter Objeto JavaScript para JSON
Usamos JSON.stringify para converter um objeto JavaScript em uma string JSON.

const pessoa = {
    nome: "João",
    idade: 30,
    casado: true,
    filhos: ["Ana", "Pedro"],
    endereco: {
        rua: "Rua Principal",
        cidade: "São Paulo",
        pais: "Brasil"
    }
};

const jsonString = JSON.stringify(pessoa);
console.log(jsonString);
// Saída: '{"nome":"João","idade":30,"casado":true,"filhos":["Ana","Pedro"],"endereco":{"rua":"Rua Principal","cidade":"São Paulo","pais":"Brasil"}}'

Converter JSON para Objeto JavaScript
Usamos JSON.parse para converter uma string JSON em um objeto JavaScript.

const jsonString = '{"nome":"João","idade":30,"casado":true,"filhos":["Ana","Pedro"],"endereco":{"rua":"Rua Principal","cidade":"São Paulo","pais":"Brasil"}}';

const pessoa = JSON.parse(jsonString);
console.log(pessoa.nome); // Saída: João
console.log(pessoa.filhos); // Saída: ["Ana", "Pedro"]


  Exemplo de Uso em um Projeto Web
Vamos considerar um exemplo onde um script JavaScript obtém dados JSON de um servidor e os exibe em uma página web.Exemplo de Uso com fetch API

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo JSON</title>
</head>
<body>
    <h1>Lista de Usuários</h1>
    <ul id="user-list"></ul>

    <script>
        // URL do endpoint que retorna um JSON
        const url = 'https://jsonplaceholder.typicode.com/users&#39;;

        // Função para carregar e exibir os usuários
        function loadUsers() {
            fetch(url)
                .then(response => response.json()) // Converte a resposta em JSON
                .then(data => {
                    const userList = document.getElementById('user-list');
                    userList.innerHTML = '';

                    // Itera sobre os dados e cria elementos de lista
                    data.forEach(user => {
                        const listItem = document.createElement('li');
                        listItem.textContent = `${user.name} - ${user.email}`;
                        userList.appendChild(listItem);
                    });
                })
                .catch(error => console.error('Erro ao carregar os usuários:', error));
        }

        // Carrega os usuários quando a página é carregada
        document.addEventListener('DOMContentLoaded', loadUsers);
    </script>
</body>
</html>

Explicação do Exemplo
: Usamos a função fetch para obter dados de um endpoint que retorna JSON.: Usamos response.json() para converter a resposta em um objeto JavaScript.: Criamos elementos <li> para cada usuário e os adicionamos à lista no DOM.Benefícios do JSON
: Formato compacto e de fácil leitura.
: Simples de gerar e analisar.
: Suportado por muitas linguagens de programação.
: Pode representar dados complexos de forma hierárquica.
