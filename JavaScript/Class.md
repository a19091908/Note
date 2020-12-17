# JavaScript Class
1. How to create a class
#### Method 1
<code>
var Person = function(name){
    console.log("initial a new person");
    this.name = name;
    this.sayHello = function(){
        console.log("Hello, " + this.name);
    }
} 
</code>

#### Method 2
<code>
class Person{
    
}

</code>

2. What is the prototype
    The prototype is like a chain or the ancestor.
    If the object does not have the certain property, it will find the property in the object's prototype. If it still does not find the property in the prototype, it will keep finding until the prototype is null.
    Example:
    If you have the Person Class, then 
    <code>
        var person1 = new Person("Justin"); //prototype chain: person1 -> Obeject
        var person2 = Object.create(person1); //prototype chain: person2 -> person1 -> Object
    </code>
