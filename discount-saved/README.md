# Discount Saved

Use the instructions below to display amount or percentage saved next to your item price.

## Setup
1. Create a new file under `snippets/` called `discount-saved.liquid` in your shopify theme code
2. Copy code from `discount-saved.liquid` into your newly created `snippets/discount-saved.liquid` file in your Shopify theme code
3. Add the following code to snippets/product-template.liquid
``` html
<span id="ProductPrice"
                      class="product-single__price{% if on_sale %} on-sale{% endif %}"
                      itemprop="price"
                      content="{{ current_variant.price | divided_by: 100.00 }}"
                      {% unless current_variant.available %}aria-hidden="true"{% endunless %}>
                      {{ current_variant.price | money }}
                    </span>{% include "discount-saved" %}
                  {% endif %}
                  {% if settings.position_currency_converter == "product" %}{% include "currency-selector" %}{% endif %}
                </div>

```
