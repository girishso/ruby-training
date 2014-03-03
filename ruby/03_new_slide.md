!SLIDE
# Class #
* Name must start with Capital letter
* e.g. Person, Post, Comment

!SLIDE
    @@@ ruby
      class Car
        @@wheels = 4 # class variable

        def initialize(make, c)
          @make = make # instance variable
          @color = c
        end

        def move(to) # instance method
          "moved to #{to}"
        end

!SLIDE
    @@@ ruby
        def name=(name) # Basic setter method
          @name = name
        end

        def name # Basic getter method
          @name
        end

        def self.engine # Class method
          "Four Stroke"
        end

        attr_accessor: color
        attr_reader: make
      end

!SLIDE
    @@@ ruby
        zen = Car.new("Maruti", "red")
        zen.move "Pune" #=> parenthesis are not necessary
        zen.make = "Maruti Zen" #=> NoMethodError: undefined method `make='
        zen.name = "My Car!"

!SLIDE
## Inheritance ##
    @@@ ruby
      class SuperCar < Car
        def fly(to)
          "flew to #{to}"
        end
      end

      super_car = SuperCar.new "Super", "golden"
      super_car.make #=> "Super"
      super_car.fly "New York" #=> "Flew to New York"
      super_car.move "Boston" #=> "Moved to Boston"

!SLIDE bullets incremental
## Multiple Inheritance ##
* Not supported


!SLIDE bullets incremental
## Modules ##
* Used to group related classes
* Similar to _package_ in Java
* e.g. ActiveRecord:: Base
* Can't instantiate modules

!SLIDE
## Modules ##
    @@@ ruby
      module API
        def fetch
          HTTP.get('http://example.com/cars/:id', :id => id)
        end
      end
~~~SECTION:notes~~~

* used a lot in Rails sources
* extend => class method
* include => instance method

~~~ENDSECTION~~~

!SLIDE
## mixins ##
    @@@ ruby
      class Car
        include API
      end

      i10 = Car.new "Hyundai", "grey"
      i10.fetch #=> calls API#fetch method


!SLIDE
## mixins ##
    @@@ ruby
      class Car
        extend API
      end

      Car.fetch #=> calls API#fetch method
