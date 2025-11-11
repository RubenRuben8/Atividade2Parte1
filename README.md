# Atividade2Parte1
Atividade de manipulação de String e JSON - Prof. Rhavy - P2 2025.2

## 1) JSON
JSON (JavaScript Object Notation) ou Notação de Objeto JavaScript é um tipo de arquivo de texto simples utilizado para transferir informações de forma eficiente e rápida.  
Ele se utiliza de uma formatação bem similar à sintaxe de objeto do JavaScript. É bastante utilizada por ser um arquivo leve que é transferido sem muito esforço por ser simplesmente texto, além de ser fácil ler tanto para um computador quanto para um usuário, assim sendo muito eficaz utilizar JSON para relizar troca de dados de uma aplicação para a outra.  

## 2) Conversão de JSON para JS e vice-versa
Arquivos JSON e os objetos criados em JavaScript são conversíveis entre si, criando flexibilidade entre eles.  
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
___
Agora quero converter esse objeto para JSON.  
Eu posso criar uma variável que seja meu objeto JS convertido em JSON!
```js
let vire_json = JSON.stringify(moveis);
console.log(vire_json); //saída -> {"sala":"sofá","cozinha":"geladeira","varanda":"cadeiras","banheiro":"chuveiro elétrico","quarto":"cama","custo":5400,"desconto":true}
console.log(typeof virre_json); //saida -> string
```
Note que a saída será um texto comum (string) normalmente com um parágrafo apenas, isso é o JSON.
____
E para converter JSON para JS, usamos o `JSON.pierce()`!

####
```js
//Esta é o JSON da variável 'vire_json':
{
        "sala":"sofá",
        "cozinha":"geladeira",
        "varanda":"cadeiras",
        "banheiro":"chuveiro elétrico",
        "quarto":"cama",
        "custo":5400.00,
        "desconto":true
}
```

Irei utilizar a própria conversão anterior para converter de volta a objeto.

```js
let vire_objeto = JSON.pierce(vire_json);
console.log(typeof vire_object); //saída -> object
```
> [!NOTE]
> Apesar de serem parecidos, tenha em mente que funções não funcionam em arquivos JSON!

## 3) Manipulações de string

### Verificando se "Script" existe na seguinte string:
`"JavaScript é baseada em ECMA Script"`

```js
let palavra = "JavaScript é baseada em ECMA Script";
let plv_script = "Script";
let tem_script;
let separar = palavra.split(" ");

for (let comparar of separar){

  if (comparar == plv_script){
    tem_script = true;
    break;
  }
  else{
    tem_script = false;
  }
}
```
> Crei a variável `palavra` com a palavra que desejo encontrar, uma variável booleana, e dividi a string `palavra` assim criando a array `separar`.
> utilizando _loop for...of_ eu criei a variável `comparar` que será uma string de cada vez dentro de `separar`.
> E criei uma condição: Se `comparar` for igual a `plv_script`, a booleana será _true_, caso não, será _false_


### Remover a palavra "JavaScript" e gerar uma nova string:

```js
let palavra = "JavaScript é baseada em ECMA Script";
let plv_script = "JavaScript";

let index_plv = palavra.indexOf(plv_script);
let nova_str = palavra.slice(index_plv, index_plv + plv_script.length);
console.log(nova_str);
```
> Mantive a variável `palavra`, coloquei `"JavaScript"` na variável `plv_script`. Criei uma variável que será o index inicial da palavra "JavaScript" (0), e uma outra variável que será a fatia da `palavra` que começa do index da palavra desejada, até o último index determinado pela soma entre o index incial da palavra, pelo tamanho da palavra.

### Substituir "baseada" por "tem origem"
```js
let palavra = "JavaScript é baseada em ECMA Script";
let plv_script = "é baseada";
let nova_string = palavra.replace(plv_script, "tem origem");
console.log(nova_string);
```
> `plv_script` tem valor `"é baseada"`, e criei uma nova variável que será a frase original porém com função `String.replace()` aplicada, onde o trecho `"é baseada"` será substituído por `"tem origem"`

### Qual a vantagem de usar template strings (``) em vez de concatenação com + para criar strings complexas?

A vantagem, é que com os acentos graves, você pode utilizar as aspas únicas e duplas dentro do texto da string sem problemas, evitando concatenação desnecessária, e além do mais, com a _interpolação_ `${}` permite que você use variáveis dentro da string.
