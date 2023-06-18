# Graded Assignment 2

1) Which of the following keywords can be used to declare a variable with global scope?
- [ ] let

- [x] var

- [ ] const

- [ ] All of the above
____
2) Which of the following statements is true regarding JavaScript language?

- [ ] JavaScript is a statically typed language.

- [x] JavaScript is a dynamically typed language.

- [ ] JavaScript is a weakly typed language.

- [ ] JavaScript is a strongly typed language.
____
3) Which of the following statement(s) is/are correct regarding JavaScript?

- [ ] It is a forgiving language like HTML.

- [ ] It inserts a semicolon after each statement automatically.

- [x] Blocks and functions both use { } for body contents.

- [ ] Blocks use { } but functions use indentation for body contents.
____
4) What will be the output of the following program?
```js
const obj = {
    name: 'Rohit',
    changeName: function (name) {
        this.name = name
    },
}

obj.changeName( 'Mohit' )
console.log(obj.name)
```
- [ ] undefined

- [ ] Rohit

- [x] Mohit

- [ ] null
____
5)Consider the following code snippet,

   const x = { name: 'rohit' }
   x.name = 'Mohit'

What will be the output of console.log(x.name)?

- [ ] It will throw a TypeError.

- [ ] Rohit

- [x] Mohit

- [ ] undefined
____
6) What will be the output of the following program?
```js
const obj = {
    name: 'Rohit',
    changeName: (name) => {
        this.name = name
    },
}

obj.changeName( 'Mohit' )
console.log(obj.name)
```
- [ ] undefined

- [x] Rohit

- [ ] Mohit

- [ ] null
____
7) What will be the output of the following program?
```js
const obj = {
    name: 'Rohit',
    arrowFunction: null,
    normalfunction: function () {
      this.arrowFunction = () => {
        console.log(this.name)
        }
    },
}

obj.normalfunction()
obj.arrowFunction()
```
- [x] Rohit

- [ ] Mohit

- [ ] undefined

- [ ] Syntax Error
____
8) Which of the following is correct output for the following code snippet?
```js
setTimeout(() => console.log('hello from setTimeOut one'), 0)
console.log('hello for main one')
setTimeout(() => console.log('hello from setTimeOut two'), 0)
console.log('hello for main two')
```
- [ ] 'hello from setTimeOut one'</br>
'hello for main one'</br>
'hello from setTimeOut two'</br>
'hello from main two'</br></br>

- [ ] 'hello for main one'</br>
'hello from setTimeOut one'</br>
'hello from main two'</br>
'hello from setTimeOut two'</br></br>

- [ ] 'hello for main one'</br>
'hello from main two'</br>
‘hello from setTimeOut two'</br>
'hello from setTimeOut one'</br></br>

- [x] 'hello for main one'</br>
'hello from main two'</br>
'hello from setTimeOut one'</br>
‘hello from setTimeOut two'</br>
____
9) Consider the following HTML document,
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <script>
      setTimeout(() => {
        document.getElementById('div1').style.backgroundColor = 'yellow'
      }, 0)
   </script>
   <title>Document</title>
 </head>
 <body>
  <div
    id="div1"
    style="height: 100px; width: 100px; background-color: red"
  ></div>
 </body>
</html>
```
What will be the background color of an element having ID ‘div1’ in the rendered webpage corresponding to this document?

- [ ] red

- [ ] black

- [x] yellow

- [ ] None of the above
____
10) Consider the following JavaScript program,
```js
let startNamePrinter = (name) => {
  let x = name.split('').reverse()
  let handler = setInterval(() => {
    let y = x.pop()
    console.log(y)
  }, 1000)
  
  setTimeout(() => {
    clearInterval(handler)
  }, (name.length + 1) * 1000)
}

startNamePrinter('orange')
```
What will be the last value shown on the console after 4 seconds?

- [ ] r

- [ ] a

- [x] n

- [ ] o
