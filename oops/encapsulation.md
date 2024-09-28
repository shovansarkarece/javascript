# Encapsulation
## Necessity Of Encapsulation
- a) Grouping data and actions
- b) Hides Complexity
- c) Data Protection
- d)Controlled Access
- e)Enhance Maintainability
### Achieved Encapsulation using Different and following Methodology
- a) Encapsulation Using Closures
- b) Using Constructor Functions
- c) Using ES6 Classes.
## Encapsulation Using Closure
```
function createCounter(){
  let count = 0;
  return{
          increment:function(){
              count++;
          },
          decreement:function(){
              count--;
          },
          getCount:function(){
              return count;
          }
}
}
////const counter =  new createCounter();
const counter = createCounter();
counter.increment();
counter.increment();
counter.increment();
counter.increment();
counter.increment();
counter.decrement();
counter.decrement();
console.log(counter.getCount())
```
## Encapsulation Using ES6 Classes
```
function createCounter(){
  let #count = 0;
  return{
          increment(){
              this.#count++;
          },
          decreement(){
              this.#count--;
          },
          getCount(){
              return this.#count;
          }
}
}
////const counter =  new createCounter();
let counter = createCounter();
counter.increment();
counter.increment();
counter.increment();
counter.increment();
counter.increment();
counter.decrement();
counter.decrement();
console.log(counter.getCount())
```
