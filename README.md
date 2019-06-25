# Learn Angular

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/angular-tb2jqq)

# Template syntax
* Angular's template syntax extends HTML and JavaScript
* To iterate over the predefined list of products, use the *ngFor directive. Put the *ngFor directive on a <div>, as shown below:
```
<h2>Products</h2>
<div *ngFor="let product of products">
</div>
```
* *ngFor is a "structural directive". Structural directives shape or reshape the DOM's structure, typically by adding, removing, and manipulating the elements to which they are attached. Any directive with an * is a structural directive.

* *ngIf directive is used in case of consditional statements. In this example, the paragraph element is only created if the current product has a description, as illustrated below:

```
<p *ngIf="product.description">
    Description: {{ product.description }}
</p>
```

# Interpolation

* To display the names of the products, use the interpolation syntax {{ }}. Interpolation renders a property's value as text.
```
<h2>Products</h2>
<div *ngFor="let product of products">
  <h3>
      {{ product.name }}
  </h3>
</div>
```

# Property Binding
* Each product name will be a link to product details. Add the anchor now, and set the anchor's title to be the product's name by using the property binding [ ] syntax, as shown below:
```
<h2>Products</h2>
<div *ngFor="let product of products">
  <h3>
    <a [title]="product.name + ' details'">
      {{ product.name }}
    </a>
  </h3>
</div>
```

# Interpolation
* Interpolation {{ }} lets you render the property value as text; property binding [ ] lets you use the property value in a template expression.

# Event binding
Bind the button's click event to the share() event that we defined for you (in product-list.component.ts). Event binding is done by using ( ) around the event, as shown below:

```
<button (click)="share()">
    Share
</button>
```

# Components
Components define areas of responsibility in your UI that let you reuse these sets of UI functionality.
A component is comprised of three things:

 * A component class, which handles data and functionality. In the previous section, the product data and the    share() method were defined for you in the component class.
 * An HTML template, which determines what is presented to the user. In the previous section, you modified the   product list's HTML template to display the name, description, and a "Share" button for each product.
 * Component-specific styles that define the look and feel. The product list does not define any styles.

Our product app has 3 components defined:
* app-root is the application shell. This is the first component to load, and the parent of all other components. You can think of it as the base page.
* app-top-bar (blue background) is the store name and checkout button.
* app-product-list (purple box) is the product list that you modified in the previous section


* App is up and ready. Can be accesssed at - https://angular-tb2jqq.stackblitz.io/