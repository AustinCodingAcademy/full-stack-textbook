![](http://static1.squarespace.com/static/538f3fcde4b05c5fecc7a40e/t/538f48a4e4b00d94e8c253b3/1453396632576/?format=400w)
# Full Stack Textbook
## Lesson Four
### Object Oriented Programming in PHP

The theory of Object Oriented Programming (OOP) can be broken down into to familiar concepts: the abstract vs the concrete.
A `class` is considered abstract. It's an idea, a classification. A `Car` is an idea. The necessary pieces an object must have to be considered a `Car` instance is that the object must have a color (ex. `'blue'`, and have four wheels, etc.
```php
class Car {
    public $numberWheels = 4;
    public $color = 'blue';
}
```
No cars exist yet. Only an idea of what one would be like if it were to appear. It is only a thought at this point. Let's create our first car.

```php
$blueCar = new Car();
```
Boom! Out of nowhere a car appears. It is blue, and it has four wheels. Now this car is not a `Car` class, it is merely an _instance_ of a `Car`.

What if we want cars of different colors? Let's change the `class` definition to allow for variable colors. We can utilize the special `__contruct()` function. This function is __inherit__ in every `class`, it is automatically ran when a new _instance_ is created. Any arguments passed in when creating a `new` _instance_ will be passed into `__construct()`

```php
class Car {
    public $numberWheels = 4;
    public $color;
    
    public function __construct($color) {
        $this->color = $color;
    }
}

$blueCar = new Car('blue');
echo $blueCar->color; //=> 'blue'
```
You can see here that I can access the future _instance_, whether it be created yet or not, with the `$this` keyword. Attributes will automatically be _inherited_ by the _instance_ from the `class`.

Some times we want to just through some functions or attributes that are not concerned with the _instance_ at all. Maybe the `Car` `class` wants to make some instances of itself. We can call these `static` functions with the double colon `::`.

```php
class Car {
    public $numberWheels = 4;
    public $color;
    
    static public function makeAFew() {
        return [
            new Car('green'),
            new Car('yellow'),
            new Car('orange'),
            new Car('pink')
        ];
    }
    
    public function __construct($color) {
        $this->color = $color;
    }
}

$aFewCars = Car::makeAFew();
echo count($aFewCars); //=> 4
```

`class`es and _objects_ can interact with each other, too. Take a look at this example:

```php
class Car {
    public $numberWheels = 4;
    public $color;
    
    static public function makeAFew() {
        return [
            new Car('green'),
            new Car('yellow'),
            new Car('orange'),
            new Car('pink')
        ];
    }
    
    public function __construct($color) {
        $this->color = $color;
    }
}

$blueCar = new Car('blue');

echo $blueCar->color; //=> 'blue'

$aFewCars = Car::makeAFew();
echo count($aFewCars); //=> 4

class Garage {
    public $size;
    public $cars = [];

    public function __construct($size) {
        $this->size = $size;
    }
    
    public function howManyCars() {
        return count($this->cars);
    }
    
    public function add($car) {
        if (count($this->cars) < $this->size) {
            $this->cars[] = $car;
            echo count($this->cars);
        } else {
            echo "Sorry, we're full";
        }
    }
}

$threeCarGarage = new Garage(3);

$threeCarGarage->add($blueCar); //=> 1

$threeCarGarage->add($aFewCars[0]); //=> 2
$threeCarGarage->add($aFewCars[1]); //=> 3
$threeCarGarage->add($aFewCars[2]); //=> "Sorry, we're full"
```
