!SLIDE bullets incremental
# Blocks #
* New creatures
* called _closures_ in other languages
* think _function pointers_ in C

!SLIDE small
# Blocks #
    @@@ ruby
      def div
        puts "<div>"
        puts yield
        puts "</div>"
      end

      def p
        puts "<p>"
        puts yield
        puts "</p>"
      end

      div do
        p {"paragraph 1"}
        p {"paragraph 2"}
      end
~~~SECTION:notes~~~

* demo
* no writing methods that accept block
* but lots of methods calling that accept the block

~~~ENDSECTION~~~

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

!SLIDE
# Blocks #
    @@@ ruby
      {a: "AA", b: "bb", c: "CC"}.each_pair do |key, value|
        puts value
      end

!SLIDE execute
# Blocks #
    @@@ ruby
      %w(ruby php java).map {|language| language.upcase}

!SLIDE execute small
# Blocks #
    @@@ ruby
      [1, 2, 3, 4].inject(0) { |result, element| result + element }

!SLIDE execute
# Blocks #
    @@@ ruby
      (1..10).find_all {|e| e % 2 == 0}

