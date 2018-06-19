# CSS

## Css grid

#### Glossary

* `grid` | `cell`: parent | child, if the child is another grid it's a `content`, if not an `item`
* `track`: 1 column or 1 row of your grid
* `line`: tracks divisor, by default it's a `number`, an arbitrary name can be added
* `fr`: fraction of your grid, based on columns/rows length
* `span`: size of a child element, it's followed by a `line-name` or a `number`

#### Parent properties:

* `grid-auto-columns`
* `grid-auto-rows`

```scss
.grid {
    grid-auto-columns: fit-content(400px);
    grid-auto-columns: min-content;
    grid-auto-columns: max-content;
    grid-auto-columns: minmax(max-content, 2fr);
}
```

* `grid-template-columns`
* `grid-template-rows`

> `<track-size>` can be a length, a percentage, or a fraction<br>
> `<line-name>` an arbitrary name

```scss
.grid {
    grid-template-columns: <track-size> ... | <line-name> <track-size> ...;
    grid-template-rows: <track-size> ... | <line-name> <track-size> ...;

    // simple
    grid-template-columns: auto 50px 40px;
    grid-template-rows: 25% 100px auto;

    // with line names
    grid-template-columns: [first] auto [col4-start] 50px [five] 40px [end];
    grid-template-rows: [row1-start] 25% [row1-end] 100px [third-line] auto [last-line];

    // multiple line names
    grid-template-rows: [row1-start] 25% [row1-end row2-start] 25% [row2-end];

    // line names using repeat()
    grid-template-columns: repeat(3, 20px [col-start]);
    // which is equivalent to
    grid-template-columns: [col-start] 20px [col-start] 20px [col-start] 20px;
}
```

* `fr`
* `minmax()`
* `span`

- fr - minmax
- minimax() con grid-auto-rows
- repeat + auto-fill and auto-fit
- repeat(auto-fill, 50px)
- repeat(auto-fill, repeat(50px))
- repeat(auto-fill, minmax(150px, 1fr))
- Auto-fit
- repeat(auto-fit, minmax(150px, 1fr))

```scss
```

* `repeat()`
* `auto-fill`
* `auto-fit`

```scss
```

* `grid-gap`
* `grid-column-gap`
* `grid-row-gap`


```scss
```

* `grid-auto-flow`
* `grid-auto-flow: row;`
* `grid-auto-flow: column;`
* `grid-auto-flow: dense;`
* `grid-auto-flow: row dense;`
* `grid-auto-flow: column dense;`

```scss
```

* `grid-template-areas`

```scss
.grid {
    grid-template-areas: "<grid-area-name> | . | none"
}
```

* `justify-items`
* `align-items`
* `place-items`

```scss
.container {
    justify-items: start | end | center | stretch;
}
```

* `justify-content`
* `align-content`
* `place-content`

```scss
.container {
    justify-content:
}
```

### Children properties:

!> `float`, `display: inline-block`, `display: table-cell`, `vertical-align` and `column-*` properties have no effect on a grid item.

---

* `grid-column-start`
* `grid-column-end`
* `grid-row-start`
* `grid-row-end`

>`<line>` can be a number to refer to a numbered grid line, or a name to refer to a named grid line<br>
>`span <number>` the item will span across the provided number of grid tracks<br>
>`span <name>` the item will span across until it hits the line<br>
>`auto` indicates auto-placement, an automatic span, or a default span of one

```scss
grid-column-start: <number> | <name> | span <number> | span <name> | auto
grid-column-end: <number> | <name> | span <number> | span <name> | auto
grid-row-start: <number> | <name> | span <number> | span <name> | auto
grid-row-end: <number> | <name> | span <number> | span <name> | auto

    // simple
    grid-column-start: 2;
    grid-column-end: five;
    grid-row-start: row1-start;
    grid-row-end: 3;

    // if you are using something like
    grid-template-columns: repeat(3, 20px [col-start]);
    // get the singol line with additional number
    grid-column-start: col-start 2;

// Shorthand for grid-column-start + grid-column-end, and grid-row-start + grid-row-end
grid-column: <start-line> / <end-line> | <start-line> / span <value>;
grid-row: <start-line> / <end-line> | <start-line> / span <value>;

    grid-column: 3 / span 2;
    grid-row: third-line / 4;
```

* `order`: <number>

* `grid-area`

* `justify-self`

* `align-self`
* `place-self`