# ostrich-twister-prng.js
Pre-compiled Mersenne Twister pseudo-random number generator available as an npm javascript package. Generated using http://github.com/Sable/ostrich-twister-prng.

# Usage

    var twister = require('ostrich-twister-prng');
    twister.seed(1337);
    console.log(twister.random());
    
    # Replace JS random number generator with this one
    Math.random = twister.random;
    
# Use as a dependency in package.json

    "dependencies": { 
        "ostrich-twister-prng": "git://github.com/Sable/ostrich-twister-prng.js"
    }
