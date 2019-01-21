# Stimulus inline edit component

A StimulusJS controller to add inline edit to Rails-powered input fields.
Add the controller to your project and add the specific html.

## Example
```html
  <p
    data-controller="inline-edit"
    data-inline-edit-model="user"
    data-inline-edit-name="email"
    data-inline-edit-input-class="input"
    data-target="inline-edit.source"
    data-action="click->inline-edit#toggle click@window->inline-edit#close"
   >
    <%= @user.email %>
  </p>
```

It assumes you add it in a show view (as it uses this URL to `POST/PATCH` to), eg. `users_controller#show`. You can change `data-inline-edit-model` and `data-inline-edit-name` to respectively change the model and its record/field.

Change `data-inline-edit-input-class` to add a class to the input field.
