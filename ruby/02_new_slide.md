!SLIDE bullets incremental
# Ruby Inroduction #

* ![Alt text](../images/matz.jpeg)
* Yukihiro Matsumoto _aka_ __Matz__

!SLIDE bullets incremental
## Ruby ##
* Interpreted language
* Automatic memory management _think Java GC_
* Written in C
* Open source
* Can be embedded in HTML, Javascript, CSS

!SLIDE
## fully object oriented;  everything is an object. ##
    @@@ Ruby
      3.times { puts "Meee!!" }

!SLIDE
## Everything is an object. ##
    @@@ ruby
      3.class #=> Fixnum
      3.0.class #=> Float
      "Hello".class #=> String
      'hi'.class #=> String

      # Special values are objects too
      nil.class #=> NilClass
      true.class #=> TrueClass
      false.class #=> FalseClass
!SLIDE
## Edit any class or method anywhere ##
    @@@ ruby
      class String
        def palindrome?
          self == self.reverse
        end
      end

!SLIDE
## Ruby - Types ##
### Duck Typing ###
    @@@ ruby
      name = "manish"
      age = 24
      height = 60.7

!SLIDE
## String ##
    @@@ ruby
      name = 'manish'
      welcome = "Welcome, " + name
        #=> Welcome, manish

      welcome = "Welcome, #{name}"
        #=> Welcome, manish

      welcome = "Welcome, " + 3
        #=> TypeError: can't convert Fixnum into String

      welcome = "Welcome, " + 3.to_s
        #=> Welcome, 3

      welcome = "Welcome, #{3}"
        #=> Welcome, 3

!SLIDE
## Symbols ##
    @@@ ruby
      :name
      :email

!SLIDE execute
## Arrays ##

### Zero based index ###

    @@@ ruby
      array = [1, 2, 3, 4, 5]
      array = ["hello", 27, [10, 20]]
      array[0] #=> "hello"
      array << 30

!SLIDE execute
## Hashes ##
    @@@ ruby
      h = {user: 'girish',
          email: 'girish@cuberoot.in'}
      h['mobile']= '98232372321'
      h[:email]

!SLIDE execute
## Hashes old syntax ##
### ruby 1.8.x ###
    @@@ ruby
      h = {:user => 'girish',
          :email => 'girish@cuberoot.in'}


!SLIDE execute
## Control Structures ##
    @@@ ruby
      if 1 == 0
        "impossible"
      elsif 1 == 1
        "now you're talking"
      end

!SLIDE execute
## Control Structures ##
    @@@ ruby
      "now you're talking" if 1 == 1

!SLIDE execute
## Control Structures ##
    @@@ ruby
      i = 10
      "non-zero" unless i == 0


!SLIDE execute
## Control Structures ##
    @@@ ruby
      case 11
        when 0..10
          "tens"
        when 10..20
          "twentys"
        when 20..30
          "thirties"
        else
          "lots"
      end
~~~SECTION:notes~~~

* can be any object

~~~ENDSECTION~~~

!SLIDE
## Control Structures ##
    @@@ ruby
      for e in [1, 2, 3] do
        puts e * 2
      end
!SLIDE
## Methods ##
    @@@ ruby
      def square(n)
        return n * n
      end
      square(2) #=> 4
      square 3 #=> 9

!SLIDE
## Methods ##
    @@@ ruby
      def sum(x, y)
        x + y #=> implicit return
      end
      sum 2, 5 #=> 7


!SLIDE bullets incremental
## Ruby Conventions ##
* Class names begin with upper case letters.
* Method and variable names use lower case.
* Class names use camel case  __ActiveRecord__
* Method and variable names separate words with underscores.
* __def show_person__
* __@little_girl__


!SLIDE bullets incremental
## Ruby Conventions ##
* 2 space indentation
* methods that answer some query, append __"?"__
* e.g. def palindrome?

