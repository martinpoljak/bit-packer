BitPacker
=========

**bit-packer** provides easy declarative way of analyzing the packed bit
arrays. See an example:

```ruby
require "bit-packer"

bp = BitPacker::new(7) do
    number (:alfa) {2}      # length of the entry in bits in block
    boolean :beta
end

p bp.data
# will print out #<struct alfa=3, beta=true>
```

You can both read from data struct and write to it:

```ruby
bp.data.boolean = false
bp.data.number = 2

p bp.to_i
# will print out 4
```

Copyright
---------

Copyright &copy; 2011 &ndash; 2015 [Martin Poljak][3]. See `LICENSE.txt` for
further details.

[2]: http://github.com/martinkozak/bit-packer/issues
[3]: http://www.martinpoljak.net/
