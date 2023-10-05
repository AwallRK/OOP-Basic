# OOP-Basic

Object Oriented Programming

- Object Literal
    - Create
    - Modify key value
- Class
    - Syntax
    - Naming convention
- Property (public)
- Instantiation
- Constructor
    - Assign value to property
    - Default parameter
- Method
    - Access Property
    - Calling another method
    - Chaining


Pengertian OOP > suatu paradigma yang menggunakan abstraksi dengan tujuan membuat suatu object nyata pada dunia nyata


OOP berkaitan dengan class dimana class merupakan suatu cetakan atau blueprint yang digunakan untuk membuat object itu sendiri.

- Object Literal

  - Create and Modify Key Value:

  ```
  let animal = {
      type : "cat",
      color : "black",
      foot : 4
  }

  // change the value of object
  animal.type = 'dog'
  console.log(animal)
  ```

- Class

  - Syntax :
  - Naming Convention :
    1. PascalCase
    2. Singular
    3. Name the Class with English Language
  - Property (public)
  - Instantiation
  - Constructor

  ```js
  //class without constructor
  class Animal {
    type = "rabit";
    color = "white";
    foot = 4;
  }

  console.log(Animal); // outputnya will be [class Animal] so if u wanna make an object from class you need to do Instantiation

  // Instantiation
  const newAnimal = new Animal();

  //notes > object created by declare a variable we can say it 'object literal', but object created by instantiation we can call it 'object instatiate'

  console.log(newAnimal); // Animal {type : 'rabit', color : 'white', foot: 4}

  // we will see the class name before the object if we create object use instantiation, if we created object literal the result only display object without anything before it.

  // class with constructor
  class Animal {
    //constructor was special method which will be invoke when class has made

    //constructor merupakan fungsi namun fungsi yang menempel pada class atau object disebut sebagai method
    constructor(type, color = 'black', foot = 4) { // constructor bisa diisi dengan parameter layaknya function bisa diisi kan jga default parameternya.

      this.type = type; // this. merujuk kepada property yang ada pada constructor
      this.color = color;
      this.foot = foot;
      this.fur = 'Fluffy' // property on constructor can be filled with statis value

      //method > function yang menempel pada class atau object
      catch(){ // penulisannya tidak perlu menambahkan key function langsung nama functionnya saja

        console.log(`let's catch the ${this.type}`) // memanggil property lain di dalam method perlu menggunakan this
        return this; // ini diperlukan agar function bisa dichaining
      }

      gotAll(){
        console.log(`caugth the ${this.type} with color ${this.color}`)
        return this;
      }
    }

    const newAnimal1 = new Animal('kuda', 'coklat', 4) // instantiation disesuaikan dengan parameter yang diperlukan oleh constuctor sebagai argument

    const newAnimal2 = new Animal('Kerbau', undefined, 4) // argument bisa diisi dengan undefined untuk menggunakan default parameter pada constructor

    //cara memanggil property pada constructor sama seperti memanggil property pada object, mengganti value object instantiate jg bsa diganti seperti object literal
    newAnimal1.type = 'illama'

    console.log(Animal1)

    //cara pemanggilan method yang ada di dalam class kalian tinggal menginstantiate classnya lalu panggil seperti object dengan menggunakan property dan diinvoke 

    newAnimal1.catch() // contoh pemanggilan method catch yang ada di dalam class Animal

    //cara pemanggilan method chaining seperti ini :
    newAnimal1.catch().gotAll()
  }
  ```
