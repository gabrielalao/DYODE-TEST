# DYODE Developer Assessment Tool (BigCommerce)

Sketch, Image and Fonts are attached to the document

# [1] BigCommerce Proficiency Questions

## 1. Write a function with Stencil Utils that will return the contents of the cart object. With the response data, check if the a specific product exists in the cart. If true, then add a different product to the cart.

```javascript
// Loop product in product list
for (product in product_list) {
    utils.api.cart.getCart({}, (err, response) => {
        console.log(response);
        if (product in response) {
            //add item to cart api
            utils.api.cart.itemAdd(this, filterEmptyFilesFromFrom(new FormData(form)), (err, response) => {
                const errorMessage = err || response.data.error;
                $addToCartBtn
                    .val(originalBtnVal)
                    .prop('disabled', false);
                this.$overlay.hide();
                // Guard statement
                if (errorMessage) {
                    // Strip the HTML from the error message
                    const tmp = document.createElement('DIV');
                    tmp.innerHTML = errorMessage;
                    return showAlertModal(tmp.textContent || tmp.innerText);
                }
                // Open preview modal and update content
                if (this.previewModal) {
                    this.previewModal.open();

                    this.updateCartContent(this.previewModal, response.data.cart_item.id);
                } else {
                    this.$overlay.show();
                    // if no modal, redirect to the cart page
                    this.redirectTo(response.data.cart_item.cart_url || this.context.urls.cart);
                }
            });
        }
        console.log(err);
    }
}

```

## 2.Using Front Matter, declare the following properties to be utilized in a new store page. What restrictions should be known when writing Front Matter?

### ○ 15 top seller products, loop through with handlebars to display the name and price in an HTML structure for a carousel plugin.
```javascript
//Short code
---
carousel: true;
products:
    top_sellers:
        limit: 15
{{#each products.top_sellers}}
    <p>{{ name }}</p>
    <p>{{ price }}</p>
{{/each}}
    
```
### ○ Cart, loop through with handlebars and display each item names and prices if more than 1 item exists.
```javascript
cart:
  suggestions:
    limit: x

if(!is_empty(cart))
{
    {{#each cart.suggestions}}
        <p>{{ name }}</p>
        <p>{{ price }}</p>
    {{/each}}  
}
```
## 3.Write your own Custom page template to display the 15 top seller products and cart HTML from question #2. What file structure would your template have to be in? What is required to insure local dev does not break?

```javascript
"customLayouts": {
    "products": {},
}
  "products": {
    "product.html":"/test-url/"
}
```

`product.html file`
```script
carousel: true;
    products:
    top_sellers: 
        limit: 15 
    {{#each products.top_sellers}}
        <p>{{ name }}</p>
        <p>{{ price }}</p>
    {{/each}}
```
## 4. Describe how you would add a javascript plugin.

```html
{{inject "myProductName" product.title}}
<script>
`Note the lack of quotes around the jsContext handlebars helper, it becomes a string automatically.`
var jsContext = JSON.parse({{jsContext}}); 
`jsContext would output "{\"myProductName\": \"Sample Product\"}" which can feed directly into your JavaScript`
console.log(jsContext.myProductName); 
`Will output: Sample Product`
</script>
```

## 5. Describe the importance of Page composition and why the {{partial}} and {{block}} helpers are useful.

The page composition is important because there should be a lot of re-definings without this.
That's why {{block}} which define the content block and {{partial}} which use the base template are important.


# [2] Please develop a static (Not in BigCommerce) version of these mockups:

Using Vue.js implemented provided sketch

## HOW TO CHECK

- Download source code to your local

- `yarn install` to install the libraries

- `yarn start` to check

- You can check the UI on http://localhost:8080




Thanks for your checking.
