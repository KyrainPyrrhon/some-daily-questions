# some-daily-questions

## Currying

Currying is a functional programming technique where a function with multiple arguments is transformed into a series of functions, each taking a single argument.
简单来说就是将一个函数的参数拆解，传递给不同的函数去处理，再将其函数结果返回

为什么这类函数会被叫做“Currying Function” ?
- 为了纪念美国数学家Haskell Currying在Functional Programming做出的贡献

Currying Function会涉及到Anonymous Function, Higher Order Function和Closure

eg. Calculate the Volume of a Cuboid

- Regular Function:
  - ``` js
    function calculateVolume (length, breadth, height){
      return length * breadth * height
    }

    console.log(calculateVolume(4, 5, 6))
    ```

- Currying Function:
  - ``` js
    function calculateVolume (length) {
      return function (breadth) {
        return function (height) {
          return length * breadth * height
        }
      }
    }

    const volume = calculateVolume(4)(5)(6)

    console.log(volume)
    ```
