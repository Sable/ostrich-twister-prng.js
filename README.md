# ostrich-twister-prng.js
Pre-compiled Mersenne Twister pseudo-random number generator available as an npm javascript package. Generated using http://github.com/Sable/ostrich-twister-prng.

# Usage

    var twister = require('ostrich-twister-prng');
    console.log(twister.random());
    
    # Replace JS random number generator with this one
    Math.random = twister.random;

    # Use in the same way as the MATLAB rand() function
    twister.rand(1,10)
    
# Use as a dependency in package.json

    "dependencies": { 
        "ostrich-twister-prng": "git://github.com/Sable/ostrich-twister-prng.js"
    }

# Use as a Wu-Wei dependency inside implementation.json

    "dependencies": [
        {
            "source": "https://github.com/Sable/ostrich-twister-prng.js.git",
            "destination": { "file": "./twister" }
        }
    ]

Inside the runner file:

    var twister = require('./twister/ostrich-twister-prng.js');
    console.log(twister.random());
    
# Use as a universal module with requireJS

    requirejs['/path/to/ostrich-twister-prng-UMD.js'](function (prng) {
        console.log(prng.random());
    })
    
    
