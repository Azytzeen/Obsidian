#programowanie #HTML #CSS 
In (web) development, we have a lot of **rules and conventions** when it comes to naming things.

For example, we named our main HTML file `index.html`. This is NOT something you have to do - it's just a common convention. And some hosting providers might require that name, in order to serve your files successfully. But in general, you could've named it `My First File.html` as well. Nonetheless, it is recommended to stick to such common conventions.

The question is: **How do you name your second, third etc. HTML files? And how you should you name your CSS files?**

For **HTML files**, it's generally a good idea to give them names that **describe the main purpose** or content of the page that will be loaded.

For example, if you have a HTML file that will display the shopping cart content of a user, `cart.html` might be a fitting name. The HTML file that is responsible for displaying a bunch of online shop products might be named `products.html`.

For **CSS files**, you typically either have a file that belong to a specific HTML file or you have global CSS files (that are used in multiple / all HTML files):

-   For page-specific CSS files, it's a good idea to repeat the HTML filename (e.g. `cart.css` holds the styles for `cart.html`).
    
-   For CSS files that belong to multiple HTML files, you might want to choose general names like base.css or describe the general purpose of the HTML files to which the CSS file belongs, like `online-shop.css` for both the `cart.html` and `products.html` files.
    

There's also one **important characteristic** which you maybe noticed about all these filenames: They are **all lowercase.**

And that's important! Whilst it's technically not required, it is a **very common convention** that you name your files **all-lowercase**, with **no special characters** except for dashes (`-`). If your file name consists of multiple words, you should NOT separate them with blanks (whitespace) but instead use dashes. So use `online-shop.html` instead of `Online Shop.html`.