BitPacker
=========

**bit-packer** provides easy declarative way of analyzing the packed bit 
arrays. See an example:
        
        require "bit-packer"
        
        bp = BitPacker::new(7) do
            number (:alfa) {2}      # length of the entry in bits in block
            boolean :beta
        end
        
        p bp.data
        # will print out #<struct alfa=3, beta=true>
        
You can both read from data struct and write to it:

        bp.data.boolean = false
        bp.data.number = 2
        
        p bp.to_i
        # will print out 4

Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b 20101220-my-change`).
3. Commit your changes (`git commit -am "Added something"`).
4. Push to the branch (`git push origin 20101220-my-change`).
5. Create an [Issue][2] with a link to your branch.
6. Enjoy a refreshing Diet Coke and wait.

Copyright
---------

Copyright &copy; 2011 [Martin Kozák][3]. See `LICENSE.txt` for
further details.

[2]: http://github.com/martinkozak/bit-packer/issues
[3]: http://www.martinkozak.net/
