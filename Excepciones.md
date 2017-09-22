
# Excepciones


## Manejo server

### DAO

La clase de acceso a datos deberá consumir algún backend SAM a través de una clase SamXXXXService determinada, por ejemplo SamHostService, SamSPService, etc.
A nivel de DAO retornaremos algunas de la sigs. excepciones:

- DataAccessException: en caso que haya ocurrido un error de comunicaciones, etc. Algo que impida la correcta ejecución del requerimiento.

- NotOkException: en caso que se detecte un error de negocio retornado por el servicio consumido (trx, sp, ws, etc). 

```java
try {
	cuentasDao.getSaldoByCuenta(cuenta);
} catch (NotOKException e) {
	if (e.getExceptionCode == "RAH00024") {
		saldo=0.00;
	}
}
```



### Service
El service asociado a un circuito funcional deberá realizar el catch de las excepciones NotOkException cuando necesite hacer un manejo específico de las respuestas obtenidas. 

<i class="icon-file"></i>##Manejo front-end




# H1 Headers (Underline)


## H2 Header (Underline)

### H3 Header



# Blockquotes

> Blockquotes



# Links

[Links](http://localhost/)

[Links with title](http://localhost/ "link title")

`<link>` : <https://github.com>

[Reference link][id/name] 

[id/name]: http://link-url/




# Code Blocks (multi-language) & highlighting

## Inline code

`$ npm install marked`

## Code Blocks (Indented style)

Indented 4 spaces, like `<pre>` (Preformatted Text).

    <?php
        echo "Hello world!";
    ?>
    
Code Blocks (Preformatted text):

    | First Header  | Second Header |
    | ------------- | ------------- |
    | Content Cell  | Content Cell  |
    | Content Cell  | Content Cell  |

## Javascript　

```javascript
function test(){
	console.log("Hello world!");
}

var testBox = box();
testBox.add("jQuery").remove("jQuery");
```

## HTML code

```html
<!DOCTYPE html>
<html>
    <head>
        <mate charest="utf-8" />
        <title>Hello world!</title>
    </head>
    <body>
        <h1>Hello world!</h1>
    </body>
</html>
```



# Images

Image:

![](https://pandao.github.io/editor.md/examples/images/4.jpg)

> Follow your heart.
  


# Listas 

## Unordered list (plus sign and nested)
                
+ Item A
+ Item B
    + Item B 1
    + Item B 2
    + Item B 3

## Ordered list
                
1. Item A
2. Item B
3. Item C
             
## GFM task list

- [x] GFM task list 1
- [x] GFM task list 2
- [ ] GFM task list 3
    - [ ] GFM task list 3-1
    - [ ] GFM task list 3-2
- [ ] GFM task list 4
    - [ ] GFM task list 4-1
	     
	     


# Tablas

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |


| Function name | Description                    |
| ------------- | ------------------------------ |
| `help()`      | Display the help window.       |
| `destroy()`   | **Destroy your computer!**     |




            
