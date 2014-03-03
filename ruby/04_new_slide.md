!SLIDE bullets incremental
# Blocks #
* New creatures
* called _closures_ in other languages
* think _function pointers_ in C

!SLIDE
# Blocks #
    @@@ ruby
      [1, 2, 3].each do |e|
        puts e * e
      end
* _each_ implemented in Enumerable module

~~~SECTION:notes~~~

* default way to iterate over Array/Hash

~~~ENDSECTION~~~

!SLIDE execute
# Blocks #
    @@@ ruby
      [1, 2, 3].map {|e| e * 2}

!SLIDE execute
# Blocks #
    @@@ ruby
      (1..10).find_all {|e| e % 2 == 0}

~~~SECTION:notes~~~

* default way to iterate over Array/Hash

~~~ENDSECTION~~~


