# Atividade2Parte1
Atividade de manipulação de String e JSON - Prof. Rhavy - P2 2025.2

## JSON
JSON (JavaScript Object Notation) ou Notação de Objeto JavaScript é um tipo de arquivo de texto simples utilizado para transferir informações de forma eficiente e rápida.  
Ele se utiliza de uma formatação bem similar à sintaxe de objeto do JavaScript. É bastante utilizada por ser um arquivo leve que é transferido sem muito esforço por ser simplesmente texto, além de ser fácil ler tanto para um computador quanto para um usuário, assim sendo muito eficaz utilizar JSON para relizar troca de dados de uma aplicação para a outra.  

## Conversão de JSON para JS e vice-versa
Tanto JSON quanto os objetos criados em JavaScript são conversíveis entre si, criando flexibilidade entre eles.  
A conversão é feita com o uso de duas funções, `JSON.stringify();` para converter objetos JS em textos JSON, e `JSON.pierce();` para converter textos JSON em objetos JS.  

**Exemplo:**
#### meu_codigo.js
```js
const moveis = {
        sala:"sofá",
        cozinha:"geladeira",
        varanda:"cadeiras",
        banheiro:"chuveiro elétrico",
        quarto:"cama",
        custo:5400.00,
        desconto:true
};
```
Aqui vemos uma variável constante chamada 'moveis' do tipo objeto que contém 7 chaves cada uma com seu único valor.  
____
Agora quero converter esse objeto para JSON.  
Eu posso criar uma variável que seja meu objeto JS convertido em JSON!
```js
let vire_json = JSON.stringify(moveis);
console.log(vire_json); //saída -> {"sala":"sofá","cozinha":"geladeira","varanda":"cadeiras","banheiro":"chuveiro elétrico","quarto":"cama","custo":5400,"desconto":true}
```
Note que a saída será um texto comum (string) normalmente com um parágrafo apenas, isso é o JSON.
____
E para converter JSON para JS, usamos o `JSON.pierce()`!

####
```js
//Esta é a string da variável 'vire_json':
{
        "sala":"sofá",
        "cozinha":"geladeira",
        "varanda":"cadeiras",
        "banheiro":"chuveiro elétrico",
        "quarto":"cama",
        "custo":5400.00,
        "desconto":true
}

//irei utilizar a própria conversão anterior para converter de volta a objeto.
let vire_objeto = JSON.pierce(inforrrmacoes.json);
console.log(typeof vire_object); //saída -> object
```
