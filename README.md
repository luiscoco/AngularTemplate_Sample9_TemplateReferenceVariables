# template-reference-variables

In Angular, template reference variables are used to reference elements, components, or directives within a template. They provide a way to access and manipulate those elements or components programmatically.

To create a template reference variable, you can use the # symbol followed by a name of your choice. This variable can then be used anywhere within the template to refer to the corresponding element or component.

Here's a simple example to illustrate the usage of template reference variables:

```typescript
<input type="text" #nameInput>
<button (click)="sayHello(nameInput.value)">Say Hello</button>
```

In this example, we have an input field and a button. The #nameInput template reference variable is associated with the input field. When the button is clicked, the sayHello() method is called with the value of the input field as a parameter. The nameInput.value expression retrieves the value of the input field using the template reference variable.

Here's the corresponding component code:

```typescript
@Component({
  selector: 'app-example',
  template: `...` // Template code from the previous example
})
export class ExampleComponent {
  sayHello(name: string) {
    console.log(`Hello, ${name}!`);
  }
}
```

In this component code, the sayHello() method is defined, which takes the name parameter and logs a greeting message to the console.

Template reference variables can also be used with other elements or components, not just input fields. For example, you can use them with components to access their methods or properties. Here's an example:

```typescript
<app-child-component #childComponent></app-child-component>
<button (click)="childComponent.someMethod()">Call Child Method</button>
```

In this example, the #childComponent template reference variable is associated with the app-child-component. When the button is clicked, the someMethod() method of the child component is called.

Template reference variables provide a convenient way to interact with elements or components in Angular templates, enabling you to perform various operations and access their properties or methods.
