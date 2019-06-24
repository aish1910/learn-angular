# angular-tb2jqq

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/angular-tb2jqq)

# Template syntax
* Angular's template syntax extends HTML and JavaScript
* To iterate over the predefined list of products, use the *ngFor directive. Put the *ngFor directive on a <div>, as shown below:

<code>

<h2>Products</h2>

<div *ngFor="let product of products">
</div>

</code>

* *ngFor is a "structural directive". Structural directives shape or reshape the DOM's structure, typically by adding, removing, and manipulating the elements to which they are attached. Any directive with an * is a structural directive.

# Interpolation

* To display the names of the products, use the interpolation syntax {{ }}. Interpolation renders a property's value as text.

<code>

<h2>Products</h2>

<div *ngFor="let product of products">

  <h3>
      {{ product.name }}
  </h3>

</div>

</code>

# Binding
* Each product name will be a link to product details. Add the anchor now, and set the anchor's title to be the product's name by using the property binding [ ] syntax, as shown below:

<code>

<h2>Products</h2>

<div *ngFor="let product of products">

  <h3>
    <a [title]="product.name + ' details'">
      {{ product.name }}
    </a>
  </h3>

</div>

</code>

* Interpolation {{ }} lets you render the property value as text; property binding [ ] lets you use the property value in a template expression.