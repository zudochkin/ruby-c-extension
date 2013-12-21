# Write your first C extension for Ruby

### Step-by-step instruction

1. Clone repository
2. `cd static_libs; cc -Wall -c hello_user.c` compile into its opbject file
3. Now that we have the class file compiled into an object file, we then need to pack it into a static library `ar rcs libexample.a hello_user.o`
4. `cp libexample.a ../ext/wrap_c_example/lib`
5. `cd ../ext/wrap_c_example`
6. `ruby extconf.rb`
7. `make`
8. `make install`

### Using

1. `irb`
2. `require 'wrap_c_example_c'`
3. `WrapCExample::Greeting.new('Dude').hello`
