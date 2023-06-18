# Graded Assignment 2

1) Which of the following shows the correct output, if the program written below is executed?

      let a = [75, 55, 22, 5]; </br>
      console.log(a.sort());
      
- [ ] []

- [ ] Error

- [x] [5, 22, 55, 75]

- [ ] [22, 5, 55, 75]
____
2) What will be the output of the following program?
```js
a = {
    name: 'Abhi',
    age: 22
};

b = [];
for (let i = 0; i < 3; i++){
    b.push(a)
}

b[1].name = 'Akshay';
console.log(b[0].name);
```
- [ ] Abhi

- [x] Akshay

- [ ] undefined

- [ ] ReferenceError
____
3) Which of the following shows the correct output, if the program written below is executed?
```js
const a = {
    name: 'Abhi',
    age: 22
};

b = [];
for (let i = 0; i < 3; i++){
    b.push({...a})
}

b[1].name = 'Akshay';
console.log(b[0].name);
```
- [x] Abhi

- [ ] Akshay

- [ ] Undefined

- [ ] ReferenceError
____
4) Consider the following program,
```js
x = [1, 2, 3, 4, 5, 6]
y = [...x, 7, 8, 9]
z = y.filter((x) => x % 2 == 0)
     .map((i) => i * i)
     .reduce((a, i) => a + i, (a = 0))
console.log(z)
```
What will be the output of the program?

- [ ] 100

- [x] 120

- [ ] 140

- [ ] 160
____
5) What will be the output of the following program?
```js
const obj = {
    x: 1,
    y: 1,
    set nums(xCommay) {
        numbers = xCommay.split(',')
        this.x = numbers[0]
        this.y = numbers[1]
    },
    get nums() {
        return this.x + ',' + this.y
    },
    xPowery: function () {
        let result = 1
        for (let i = 1; i <= this.y; i++) {
            result = result * this.x
        }
        return result
    },
}
obj.nums = '2,3'
console.log(obj.xPowery())
```
- [ ] 6

- [ ] 5

- [x] 8

- [ ] None of the above
____
6) What will be the output of the following program?
```js
const ePowerx = {
    x: 1,
    n: 1,
    set parameters(param) {
        param = param.split(' ')
        this.x = param[0]
        this.n = param[1]
    },
    get uptoNterms() {
        let result = 1
        let y = 1
        for (let i = 1; i < this.n; i++) {
            y = y * this.x
            result = result + y
        }
        return result
    },
}
ePowerx.parameters = '2 3'
console.log(ePowerx.uptoNterms)
```
- [ ] 3

- [ ] 5

- [x] 7

- [ ] 15
____
7) What will be the output of the following program?
```js
const course = {
    courseName: 'Modern Application Development 2',
    courseCode: 'mad2',
}

const student = {
    __proto__: course,
    studentName: 'Rakesh',
    studentCity: 'Delhi',
}

const { courseName } = student
console.log(courseName)
```
- [ ] Undefined

- [x] Modern Application Development 2

- [ ] Will throw syntax error

- [ ] None of the above
____
8) Consider the following,

Index.html:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>Document</title>
    </head>
    <body>
        <div id="div1" style="background-color: red"></div>
    </body>
    <script src="script.js"></script>
</html>
```
script.js
```js
var height = 0
var width = 0
var divStyle = document.getElementById('div1').style
let res = setInterval(() => {
    height += 50
    width += 50
    divStyle.height = height + 'px'
    divStyle.width = width + 'px'
    console.log(height)
}, 1000)

setTimeout(() => {
    clearInterval(res)
}, 10050)
```
Assuming that the index.html and script.js are kept inside the same directory, then what will be the  height of the HTML element having ID ‘div1’ after 20 seconds, if rendered using a browser?

- [ ] 500px

- [x] 1000px

- [ ] 0px

- [ ] None of the above
____
9) Consider the following HTML document,

Index.html:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>Document</title>
        <script src="module1.js" type="module"></script>
    </head>
    <body>
        <div id="div1" style="border: 2px solid black"></div>
    </body>
</html>
```
module1.js
```js
import { divStyle1, divStyle2 } from './module2.js'
divStyle1.width = "50px"
const div1Style = document.getElementById('div1').style
div1Style.backgroundColor = divStyle1.color
div1Style.height = divStyle2.height
div1Style.width = divStyle1.width
```
module2.js
```js
export const divStyle1 = {
    color: 'red',
    height: '100px',
    width: '100px',
}

export const divStyle2 = {
    color: 'green',
    height: '50px'
}
```
Assuming that the index.html, module1.js, and module2.js are kept inside the same directory, then what will be the background color, height and width of the HTML element having ID ‘div1, if rendered using a browser?

- [ ] Red, 100px, 100px

- [x] Red, 50px, 50px

- [ ] Green, 50px, 100px

- [ ] Green, 50px, 50px
____
10) What will be the output of the following program?

```js
api = { A: 'Application', P: 'Programming', I: 'Interface' }
const standsFor = (x) => {
    for (const [k, v] of Object.entries(api)) {
        if (k != x) {
            return v
        }
    }
}

console.log(standsFor('A'))
```
- [ ] Application

- [x] Programming

- [ ] Interface

- [ ] A
