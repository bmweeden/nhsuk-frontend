# Button

To discuss or contribute to this component, visit the [GitHub issue for this component](https://github.com/nhsuk/nhsuk-frontend/issues/203).

## Guidance

Find out more about the button component and when to use it in the [NHS digital service manual](https://beta.nhs.uk/service-manual/styles-components-patterns/buttons).

## Quick start examples

### Button

[Preview the button component](https://nhsuk.github.io/nhsuk-frontend/components/button/index.html)

#### HTML markup

```html
<button class="nhsuk-button" type="submit">
  Save and continue
</button>
```

#### Nunjucks macro

```
{% from 'components/button/macro.njk' import button %}

{{ button({
  "text": "Save and continue"
}) }}
```

---

### Button as a link

[Preview the button as a link component](https://nhsuk.github.io/nhsuk-frontend/components/button/link.html)

#### HTML markup

```html
<a href="/" role="button" draggable="false" class="nhsuk-button">
  Link button
</a>
```

#### Nunjucks macro

```
{% from 'components/button/macro.njk' import button %}

{{ button({
  "text": "Link button",
  "href": "/"
}) }}
```

---

### Button disabled

[Preview the button disabled component](https://nhsuk.github.io/nhsuk-frontend/components/button/disabled.html)

#### HTML markup

```html
<button class="nhsuk-button nhsuk-button--disabled" type="submit" disabled="disabled" aria-disabled="true">
  Disabled button
</button>
```

#### Nunjucks macro

```
{% from 'components/button/macro.njk' import button %}

{{ button({
  "text": "Disabled button",
  "disabled": true
}) }}
```

---

### Button secondary

[Preview the button secondary component](https://nhsuk.github.io/nhsuk-frontend/components/button/secondary.html)

#### HTML markup

```html
<button class="nhsuk-button nhsuk-button--secondary" type="submit">
  Find my location
</button>
```

#### Nunjucks macro

```
{% from 'components/button/macro.njk' import button %}

{{ button({
  "text": "Find my location",
  "classes": "nhsuk-button--secondary"
}) }}
```

---

### Button reverse

[Preview the button reverse component](https://nhsuk.github.io/nhsuk-frontend/components/button/reverse.html)

#### HTML markup

```html
<button class="nhsuk-button nhsuk-button--reverse" type="submit">
  Save and continue
</button>
```

#### Nunjucks macro

```
{% from 'components/button/macro.njk' import button %}

{{ button({
  "text": "Save and continue",
  "classes": "nhsuk-button--reverse"
}) }}
```

### Nunjucks arguments

The button Nunjucks macro takes the following arguments:

| Name                | Type     | Required  | Description             |
| --------------------|----------|-----------|-------------------------|
| **element**         | string   | No        | Whether to use an `input`, `button` or `a` element to create the button. In most cases you will not need to set this as it will be configured automatically if you use `href` or `html`. |
| **text (or) html**  | string   | Yes       | Text or HTML for the button or link. If `html` is provided, the `text` argument will be ignored and `element` will be automatically set to `button` unless `href` is also set, or it has already been defined. This argument has no effect if `element` is set to `input`.|
| **name**            | string   | Yes       | Name for the `input` or `button`. This has no effect on `a` elements. |
| **type**            | string   | Yes       | Type of `input` or `button` – `button`, `submit` or `reset`. Defaults to `submit`. This has no effect on `a` elements. |
| **value**           | string   | Yes       | Value for the `button` tag. This has no effect on `a` or `input` elements. |
| **disabled**        | boolean   | No       | Whether the button should be disabled. For button and input elements, `disabled` and `aria-disabled` attributes will be set automatically. |
| **href**           | string   | No       | The URL that the button should link to. If this is set, `element` will be automatically set to `a` if it has not already been defined. |
| **classes**         | string   | No        | Optional additional classes to add to the button element. Separate each class with a space. |
| **attributes**      | object   | No        | Any extra HTML attributes (for example data attributes) to add to the textarea tag. |

If you are using Nunjucks macros in production be aware that using `html` arguments, or ones ending with `html` can be a [security risk](https://developer.mozilla.org/en-US/docs/Glossary/Cross-site_scripting). Read more about this in the [Nunjucks documentation](https://mozilla.github.io/nunjucks/api.html#user-defined-templates-warning).

## Thanks to the Government Digital Service (GDS)

This component and documentation has been taken from [GOV.UK Frontend - Button component](https://github.com/alphagov/govuk-frontend/tree/master/package/components/button) with a few minor adaptations.
