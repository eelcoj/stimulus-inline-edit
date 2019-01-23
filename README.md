# Stimulus inline edit controller

A StimulusJS controller to add inline edit to input fields (**Rails-only**).

## Install

Assuming [StimulusJS](https://stimulusjs.org) is already installed. Add the `stimulus-inline-edit` module:

```bash
$ yarn add stimulus-inline-edit
```

or

```bash
$ npm install stimulus-inline-edit
```

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

## Contributing

Bug reports and pull requests are welcome on GitHub at <https://github.com/eelcoj/stimulus-inline-edit>.

## License

This package is available as open source under the terms of the MIT License.
