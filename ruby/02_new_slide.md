!SLIDE bullets incremental
# Ruby Inroduction #

* ![Alt text](../images/matz.jpeg)
* Yukihiro Matsumoto _aka_ __Matz__

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

!SLIDE bullets incremental
## Ruby ##
* Automatic memory management _think Java GC_
* Written in C
* Open source
* Can be embedded in HTML, Javascript, CSS

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

!SLIDE execute
## String ##
    @@@ ruby
      "ruby"
      "rails"
