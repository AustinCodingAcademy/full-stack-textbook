![](http://static1.squarespace.com/static/538f3fcde4b05c5fecc7a40e/t/538f48a4e4b00d94e8c253b3/1453396632576/?format=400w)
# Full Stack Textbook
## Lesson Four
### Object Oriented Programming in PHP

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
    
    function __construct($color) {
        $this->color = $color;
    }
}

$blueCar = new Car('blue');

echo $blueCar->color;
echo "\n";

$aFewCars = Car::makeAFew();
echo count($aFewCars);
echo "\n";

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
        echo "\n";
    }
}

$threeCarGarage = new Garage(3);

$threeCarGarage->add($blueCar);

$threeCarGarage->add($aFewCars[0]);
$threeCarGarage->add($aFewCars[1]);
$threeCarGarage->add($aFewCars[2]);
```
