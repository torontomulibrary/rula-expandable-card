[![Build status](https://travis-ci.org/ryersonlibrary/rula-expandable-card.svg?branch=master)](https://travis-ci.org/ryersonlibrary/rula-expandable-card)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/ryersonlibrary/rula-expandable-card)

## &lt;rula-expandable-card&gt;

`rula-expandable-card` is a web component inspired by a Material Design Card.
When the user interacts, the card grows to fill some or all of the screen along
with showing additional content.  The switch between the 'closed' and 'open'
states are nicely animated following Material guidelines.

An expandable card has two sections, the `header` and `content` slots.  Anything
in the `header` will be visible when the card is closed while the `content` is
what is made visible when the card is expanded.

The following code adds a simple expanding card with content in the header.

<!---
```
<custom-element-demo>
	<template>
		<script src="../webcomponentsjs/webcomponents-lite.js"></script>
		<link rel="import" href="rula-expandable-card.html">
		<style>
			rula-expandable-card {
				--rula-expandable-card: {
					height: 200px;
					width: 300px;
					padding: 25px;
					overflow: hidden;
				}

				--rula-expandable-card-body: {
					align-items: flex-end;
					background-color: var(--rula-expandable-card-header-bg, #002d72);
					border-radius: 2px;
					color: var(--rula-expandable-card-header-text, #ffffff);
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
		<next-code-block></next-code-block>
	</template>
</custom-element-demo>
```
-->
```html
<rula-expandable-card>
  <div header>
    <h2>Here's a question</h2>
    <span>How much wood can a woodchuck chuck if a woodchuck chould chuck wood?</span>
  </div>
  <div content>
    A woodchuck would chuck as much wood as a woodchuck could chuck if a woodchuck could chuck wood!
  </div>
<rula-expandable-card>
```

## Install

```
bower install --save rula-expandable-card
```

## Styling

The following custom properties and mxing are available for styling:

Custom propery | Description | Default
---------------|-------------|----------
`--rula-expandable-card-scrim` | Mixin applied to the background when the card is open | `{}`
`--rula-expandable-card-header` | Style mixin for the header section | `{}`
`--rula-expandable-card-modal-bg` | Background colour of the expanded card | `#FFF`
`--rula-expandable-card-body` | Mixin applied to the body of the card when closed | `{}` 
`--rula-expandable-card` | Mixin applied to the element | `{}`
