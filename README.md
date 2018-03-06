# CSS Variables Polyfill
A basic polyfill for CSS Variables/custom-properties

This is an attempt at a very basic [CSS variables (custom properties)](https://drafts.csswg.org/css-variables/) polyfil. In reality this is more of a partial polyfill as it will not cover variables inside of variables, DOM scoping or anything else "fancy". Just taking variables declared anywhere in the CSS and then re-parsing the CSS for var() statements and replacing them in browsers that don't natively support CSS variables.

According to [caniuse.com](https://caniuse.com/#feat=css-variables), of current browsers only IE, Edge and Opera Mini do not support CSS variables. This polyfil appears to work on all three really well. I don't see why this wouldn't work on older browsers as well, but I haven't been able to test it on them yet.