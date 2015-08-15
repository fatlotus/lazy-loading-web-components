Lazy Loaded Web Components
==========================

Current libraries (primarily Polymer), require that developers compile their
HTML and JavaScript with bower and import it into the page, before they can add
functionality into a page. I think this approach is bad, so I wrote this code to
demonstrate a model I think is easier to use.

The code in this repository implements lazy loading, which dramatically simplies
your life. Instead of endless `bower install` nonsense, simply add

    <link rel="import" href="https://cdn.com/my-library.html"/>

to the top of your page.

Doesn't this cause more roundtrips?
-----------------------------------

Yes, but HTTP/2 Push responses are a cleaner approach to that problem. While
the gzip'ed responses will be smaller, and so will have worse compression 
ratios, lazy components can be downloaded page-by-page, allowing for more 
granular downloads.

Can I use this code?
--------------------

Absolutely. This code is public domain, because I don't want to live in a world
where writing HTML requires installing something. Specifically:

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
