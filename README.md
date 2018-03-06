# CSS Variables Polyfill
A basic polyfill for CSS Variables/custom-properties

This is an attempt at a very basic [CSS variables (custom properties)](https://drafts.csswg.org/css-variables/) polyfil. In reality this is more of a partial polyfill as it will not cover variables inside of variables, DOM scoping or anything else "fancy". Just taking variables declared anywhere in the CSS and then re-parsing the CSS for var() statements and replacing them in browsers that don't natively support CSS variables.

According to [caniuse.com](https://caniuse.com/#feat=css-variables), of current browsers only IE, Edge and Opera Mini do not support CSS variables. This polyfil appears to work on all three really well. I don't see why this wouldn't work on older browsers as well, but I haven't been able to test it on them yet.

## Todo
- Verify cross domain working or not (it is working from dropbox)
- Option to wait to apply anything until all <link>s are parsed or inject what we have and update as each <link> returns
- Need to test on a more complex CSS file
- Option to save parsed file in local/session storage so there isn't a delay on additional page loads. Could only do it for links (with URLs to use as keys) and style blocks with IDs of some sort
- Need to test more complex values like rgba(255,0,0,0.5); and something with !important
- Try multiple links
- Local links
- Ajax driven site, or CSS added later the top of the stack