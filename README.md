[![Build status](https://travis-ci.org/ryersonlibrary/rula-expandable-card.svg?branch=master)](https://travis-ci.org/ryersonlibrary/rula-expandable-card)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/ryersonlibrary/rula-expandable-card)

## &lt;rula-expandable-card&gt;

`rula-expandable-card` is an elements combining aspects of Material Design 
[Cards](https://www.google.com/design/spec/components/cards.html) and
[Dialogs](https://www.google.com/design/spec/components/dialogs.html).
It displays static content in similar fashion to a Card, and when clicked by the
user it expands to fill the screen like a modal dialog while showing additional
content.

### Example

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="rula-expandable-card.html">
    <custom-style>
      <style is="custom-style">
        rula-expandable-card {
          height: 200px;
          width: 300px;
          padding: 25px;
          overflow: hidden;

          --rula-expandable-card-body: {
            align-items: flex-end;
            background-color: #002d72;
            border-radius: 2px;
            color: #ffffff;
            cursor: pointer;
            display: flex;
            font-size: 24px;
            justify-content: flex-start;
            padding: 16px;
          }
        }

        div[header] {
          @apply --rula-expandable-card-body;
          border-radius: 0;
        }

        div[content] {
          font-size: 18px;
          padding: 24px;
        }
      </style>
    </custom-style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<rula-expandable-card>
  <div main-content>
    <h2>Here's a question</h2>
    <span>How much wood can a woodchuck chuck if a woodchuck chould chuck wood?</span>
  </div>
  <div extra-content>
    A woodchuck would chuck as much wood as a woodchuck could chuck if a woodchuck could chuck wood!
  </div>
</rula-expandable-card>
```

### Structure 
A `rula-expandable-card` has three main parts:

```html
<div id="scrim"></div>
<div id="body"></div>
<div id="modal">
  <slot></slot>
</div>
```
 - `scrim` is used to hide the rest of the page when the card is open.
 - `body` displays everything in `[main-content]` and is what the user sees
 when the card is closed.
 - `modal` displays everything in both `[main-content]` and `[extra-content]`
 and is what the user sees when the card is open.


## Install

```
bower install --save rula-expandable-card
```

## Styling

The following custom properties and mxing are available for styling:

Custom propery | Description | Default
---------------|-------------|----------
`--rula-expandable-card-scrim` | Mixin applied to the background when the card is open | `{}`
`--rula-expandable-card-body` | Mixin applied to the body of the card when closed | `{}`
`--rula-expandable-card-modal` | Mixin applied to the modal container when open | `{}`
`--rula-expandable-card` | Mixin applied to the element | `{}`
