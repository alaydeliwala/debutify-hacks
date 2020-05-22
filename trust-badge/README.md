# Trust Badge

Use the instructions below to add a trust badge below your add to cart.

## Setup
1. Upload your trust badge to your store files.
2. Create a new file under snippets/ called `trust-badge.liquid` in your shopify theme code
3. Copy code from `trust-badge.liquid` into your shopify theme code
2. Add the following code to snippets/product-template.liquid
``` html
</div>

{% include "trust-badge", position: "product" %}

{% unless product.description == blank or section.settings.show_description == false %}

```
