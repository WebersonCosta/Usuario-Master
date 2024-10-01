# Usuário-Master
Projeto desenvolvido como exemplo do Curso Completo de JavaScript na Udemy.com.


# USUÁRIO MASTER

### Função preventDefault();


Evita o Envio do Formulário e permite que você valide os dados ou faça outras operações antes de decidir o que fazer com eles.

---

### JSON


JSON é um formato baseado em pares de chave-valor. Por exemplo:

```javascript
{
  "nome": "João",
  "idade": 30,
  "email": "joao@example.com"
}
```
---

### Promise


Uma promessa é um objeto que representa a eventual conclusão ou falha de uma operação assíncrona e seu valor resultante. Ela pode estar em um dos seguintes estados:

- **Pendente (Pending)**: Estado inicial, quando a operação ainda não foi concluída.
- **Cumprida (Fulfilled)**: A operação foi concluída com sucesso.
- **Rejeitada (Rejected)**: A operação falhou.

---

### Operador spread

O **spread operator** (operador de espalhamento) em JavaScript é representado por três pontos (...) e é usado para expandir ou "espalhar" elementos de um array ou propriedades de um objeto em um novo contexto. Ele é bastante útil para copiar arrays ou objetos, combinar dados e passar argumentos em funções

#### Exemplos de Uso

- Espalhando Elementos de um Array
Você pode usar o spread operator para criar uma cópia de um array ou para combinar arrays:
```javascript

const array1 = [1, 2, 3];
const array2 = [4, 5, 6];

// Copiando um array
const arrayCopy = [...array1];
console.log(arrayCopy); // [1, 2, 3]

// Combinando arrays
const combinedArray = [...array1, ...array2];
console.log(combinedArray); // [1, 2, 3, 4, 5, 6]

```

- Espalhando Propriedades de um Objeto
O spread operator também pode ser usado com objetos para copiar ou combinar propriedades:

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

// Copiando um objeto
const objCopy = { ...obj1 };
console.log(objCopy); // { a: 1, b: 2 }

// Combinando objetos
const combinedObj = { ...obj1, ...obj2 };
console.log(combinedObj); // { a: 1, b: 3, c: 4 }

```

Note que, ao combinar objetos, se houver propriedades com o mesmo nome, a última sobrescreverá as anteriores.

- Passando Argumentos para Funções
O spread operator pode ser utilizado para passar elementos de um array como argumentos para uma função:

```javascript

const numbers = [1, 2, 3];

function sum(a, b, c) {
  return a + b + c;
}

// Usando o spread operator
const result = sum(...numbers);
console.log(result); // 6

```

---

### Object.assign

O **Object.assign** é um método que é usado para copiar as propriedades de um ou mais objetos para um objeto de destino. Ele é muito útil para a criação de novos objetos a partir de objetos existentes, facilitando a combinação de propriedades e a criação de cópias de objetos.

#### Sintaxe

```javascript

Object.assign(destino, ...fontes);

```

- destino: O objeto que receberá as propriedades.
- ...fontes: Um ou mais objetos cujas propriedades serão copiadas para o objeto de destino.

#### Exemplo de uso

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const resultado = Object.assign({}, obj1, obj2);
console.log(resultado); // { a: 1, b: 3, c: 4 }

```

---

### Object.assign X Operador spread

É comum confundir o operador spread (...) com o Object.assign, pois ambos são usados para manipular objetos, mas eles têm algumas diferenças importantes. Vamos explorar cada um deles para ajudar a esclarecer.

1. Operador Spread **(...)**
- Sintaxe: Usa três pontos (...) antes do objeto.
- Copia as propriedades de um objeto para um novo objeto.
- Retorna um novo objeto sem modificar o original.
- Permite fácil combinação de objetos.

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3 };

// Usando o operador spread
const combinedSpread = { ...obj1, ...obj2 };
console.log(combinedSpread); // { a: 1, b: 2, c: 3 }

// obj1 e obj2 permanecem inalterados
console.log(obj1); // { a: 1, b: 2 }
console.log(obj2); // { c: 3 }

```

2. **Object.assign()**
- Sintaxe: Usa Object.assign(destino, ...fontes).
- Copia as propriedades de um ou mais objetos de origem para um objeto de destino.
- Modifica o objeto de destino (ele não cria um novo objeto, a menos que você o passe como um objeto vazio).
- Retorna o objeto de destino.

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3 };

// Usando Object.assign
const combinedAssign = Object.assign({}, obj1, obj2);
console.log(combinedAssign); // { a: 1, b: 2, c: 3 }

// obj1 e obj2 permanecem inalterados
console.log(obj1); // { a: 1, b: 2 }
console.log(obj2); // { c: 3 }

```

#### Diferenças Principais
1. Imutabilidade:

- O operador spread cria um novo objeto, enquanto Object.assign() pode modificar o objeto de destino.

2. Retorno:

- O spread operator sempre retorna um novo objeto, enquanto Object.assign() retorna o objeto de destino.

3. Combinação de Objetos:

- O spread operator é mais conciso e legível para combinar objetos.

4. Combinação com Arrays:

- O operador spread também pode ser usado para arrays, enquanto Object.assign() é específico para objetos.

#### Quando Usar Cada Um

- Use spread quando você quiser criar cópias de objetos de forma mais simples e legível.

- Use Object.assign() quando precisar mesclar objetos e não se importar em modificar um objeto de destino.

---

### sessionStorage


é uma **API** de armazenamento web do JavaScript, que permite armazenar dados no navegador do usuário. A principal característica do sessionStorage é que ele mantém os dados apenas durante a sessão do navegador. Isso significa que os dados armazenados nele estão disponíveis enquanto a aba ou janela do navegador estiver aberta, mas serão perdidos assim que a aba for fechada.

---

### localStorage


O localStorage é outra **API** de armazenamento web do JavaScript, que permite armazenar dados no navegador do usuário de forma persistente. Ao contrário do sessionStorage, os dados armazenados no localStorage permanecem disponíveis mesmo após o fechamento da aba ou do navegador, até que sejam explicitamente removidos.

---

### Função map


A função map é um método de array que permite transformar cada elemento de um array em um novo valor, criando um novo array com esses valores transformados. Ele é muito útil para realizar operações em todos os elementos de um array sem modificar o original.
