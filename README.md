[![Build status](https://travis-ci.org)]

## &lt;rula-expandable-card&gt;

`rula-expandable-card` is a web component inspired by a Material Design Card.
When the user interacts, the card grows to fill some or all of the screen along
with showing additional content.  The switch between the 'closed' and 'open'
states are nicely animated following Material guidelines.

An expandable card has two sections, the `header` and `content` slots.  Anything
in the `header` will be visible when the card is closed while the `content` is
what is made visible when the card is expanded.

The following code adds a simple expanding card with content in the header.

```html
<rula-expanable-card>
  <div slot="header">
    <h2>Here's a question</h2>
    <span>How much wood can a woodchuck chuck if a woodchuck chould chuck wood?</span>
  </div>
  <div slot="content">
    A woodchuck would chuck as much wood as a woodchuck could chuck if a woodchuck could chuck wood!
  </div>
<rula-expandable-card>
```
### Styling

The following custom properties and mxing are available for styling:

Custom propery | Description | Default
---------------|-------------|----------
`--rula-expandable-card-scrim` | Mixin applied to the scrim | `{}`
`--rula-expandable-card-header` | Style mixin for the header section | `{}`
`--rula-expandable-card-modal-bg` | Background colour of the expanded card | `#FFF`
`--rula-expandable-card-modal-content` | Mixin applied to the content slot | `{}` 
`--rula-expandable-card` | Mixin applied to `rula-expandable-card` | `{}`
