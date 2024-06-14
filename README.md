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
: Adiciona um ou mais elementos ao final do array e retorna o novo comprimento do array.
<br></br>
: Remove o último elemento do array e retorna esse elemento.
<br></br>
: Adiciona um ou mais elementos ao início do array e retorna o novo comprimento do array.
<br></br>
: Remove o primeiro elemento do array e retorna esse elemento.
<br></br>
: Adiciona/remover elementos a partir de uma posição específica do array. Retorna um novo array contendo os elementos removidos.
Acesso e Pesquisa de Elementos
<br></br>
: Retorna um novo array contendo todos os arrays ou valores passados como argumento.
<br></br>
: Retorna uma cópia superficial de uma parte do array em um novo array.
<br></br>
: Retorna o primeiro índice onde o elemento pode ser encontrado no array, ou -1 se não estiver presente.
<br></br>
: Retorna o último índice onde o elemento pode ser encontrado no array, ou -1 se não estiver presente.
<br></br>
: Determina se um array contém um determinado elemento, retornando true ou false.
Iteração e Transformação
<br></br>
: Executa uma dada função em cada elemento do array.
<br></br>
: Cria um novo array com os resultados da aplicação da função callback em cada elemento do array.
<br></br>
: Cria um novo array com todos os elementos que passam no teste implementado pela função callback.
<br></br>
: Aplica uma função acumuladora contra um acumulador e cada elemento do array (da esquerda para a direita) para reduzi-lo a um único valor.
<br></br>
: Aplica uma função acumuladora contra um acumulador e cada elemento do array (da direita para a esquerda) para reduzi-lo a um único valor.
<br></br>
: Testa se ao menos um dos elementos no array passa no teste implementado pela função callback. Retorna true ou false.
<br></br>
: Testa se todos os elementos no array passam no teste implementado pela função callback. Retorna true ou false.
<br></br>
: Retorna o primeiro elemento do array que satisfaz a função callback. Caso contrário, retorna undefined.
<br></br>
: Retorna o índice do primeiro elemento do array que satisfaz a função callback. Caso contrário, retorna -1.
Ordenação e Reversão
<br></br>
: Ordena os elementos do array e retorna o array.
<br></br>
: Inverte a ordem dos elementos do array no lugar. O primeiro elemento torna-se o último e o último torna-se o primeiro.
Outros Métodos Úteis
<br></br>
: Junta todos os elementos do array em uma string, separados por um separador especificado. Se não for especificado, o separador padrão é uma vírgula.
<br></br>
: Retorna uma string representando o array especificado e seus elementos.
<br></br>
: Retorna um novo array com todos os sub-arrays concatenados em um nível especificado.
<br></br>
: Primeiro mapeia cada elemento usando uma função de mapeamento e, em seguida, achata o resultado em um novo array.
<br></br>

## Exemplos de uso:

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
