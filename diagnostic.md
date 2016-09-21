# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
  A sign-up link on a page: route template goes to a form
      The link goes to a sign-up form: component
        The form is made up of components for individual input, ie email,
        password, confirm password.


    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    1. A component.js file, which states actions to performed on the component.
    2. Template.js, which is the UI for that component.  This could rendered
    directly or reference another template.
    3. A test file, which is used to verify that a path is functioning.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{my-contact contact=contact}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{each contact.numbers as |numbers|}}
      {{my-contact/my-phone numbers=numbers}}
    ```
