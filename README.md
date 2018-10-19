# Class Exercises

1.
  * Create a Human class that takes in a name and age.
  * Add the function `ageOneYear` that ages the human.
  * Add the function `eating`, that logs "mmm, mmm, mmm, I'm love'n it".
  * Create an instance of the Human class.
    * console log your humans age
    * call ageOneYear on your human
    * console log their age again.
    * call eating on your human.

    class Human {
     constructor(name, age){
       this.name = name;
       this.age = age;
     }

     ageOneYear(str){
       return this.age++
     }

      eating(str){
        return "mmm, mmm, mmm, I'm love'n it."
      }
    }


    let daniel = new Human("Daniel", 34)
    console.log(daniel.age)
    daniel.ageOneYear()
    console.log(daniel.age)
    console.log(daniel.eating())

2.
Write a class Vector that represents a vector in two-dimensional space.
It takes two number arguments: `x` and `y` parameters, which it should be saved to properties of the same name.

Give the Vector two methods, `plus` and `minus`, that take another vector as an argument and
returns a new vector that has the sum or difference of the two vectors’ (the one in `this` and the parameter) x and y values.

Add a method `getLength` to the prototype that computes the length of the vector ;
that is, the distance of the point (x, y) from the origin (0, 0).(a^2 + b^2 = c^2)


class Vector {
 constructor(x, y){
   this.x = x;
   this.y = y;
 }

 plus(vector){
   let a = this.x + vector.x;
    let b = this.y + vector.y;
     let v3 = new Vector(a,b)
     return v3;
 }

  minus(vector){
    let a = this.x - vector.x;
    let b = this.y - vector.y;
      let v4 = new Vector(a,b)
     return v4;
  }
  getLength(){
    let length = Math.hypot(this.x,this.y)
   return length;
  }
}


let v1 = new Vector(1, 2)
let v2 = new Vector(3, 4)
console.log(v1.plus(v2));
console.log(v1.minus(v2));
console.log(v2.getLength());
//holy god, you guys, it worked
