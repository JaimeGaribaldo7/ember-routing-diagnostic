# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Inside each route, you can edit the template to display what you want to, and you can add a model hook to pass data.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}Back{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first route definition was used properly. When the Second route defition is creating a route in the same line as product, so for example, you can visit localhost/product, instead of the proper way; localhost/products/:product_id
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    Assuming this is a nested route, you can assume, it is the movie with an id of 123.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Inside a template, you would need to use an #each to itterate through each object or piece of data, and set it as whatever you use inside of the pipes.
    ```
