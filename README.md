## Grid Container

Create a grid container by setting the `display` property with a value of `grid` or `inline-grid`. All direct children of grid containers emphasized text> become grid items.

    display: grid;

>    Grid items are placed in rows by default and span the full width of
> the grid     container.
   
    display: inline-grid;
    
## Explicit Grid

Explicitly set a grid by creating columns and rows with the grid-template-columns and grid-template-rows` properties.

```
grid-template-rows: 50px 100px;
```

> A row track is created for each value specified for
> grid-template-rows. Track size values can be any non-negative, length
> value (px, %, em, etc.)
   
```
grid-template-columns: 90px 50px 120px;
```    
>Like rows, a column track is created for each value specified for grid-> template-columns.
```
grid-template-columns: 1fr 1fr 2fr;
```
> The `fr` unit helps create flexible grid tracks. It represents a
> fraction of the available space in the grid container (works like
> Flexbox’s unitless values).
```
grid-template-columns: 3rem 25% 1fr 2fr
```
## Minimum and Maximum Grid Track Sizes

Tracks sizes can be defined to have a minimum and/or maximum size with the `minmax()` function.


```
grid-template-rows:    minmax(100px, auto);
```
```
grid-template-columns: minmax(auto, 50%) 1fr 3em;
```

## Repeating Grid Tracks

Define repeating grid tracks using the `repeat()` notation. This is useful for grids with items with equal sizes or many items.

```
grid-template-rows:    repeat(4, 100px);
```

```
grid-template-columns: 30px repeat(3, 1fr) 30px
```

## Grid Gaps (Gutters)
The  `grid-column-gap`  and  `grid-row-gap`  properties create gutters between columns and rows.
Grid gaps are only created in between columns and rows, and not along the edge of the grid container 🙌 .

```
grid-row-gap: 20px;
```
```
grid-column-gap: 5rem;
```
```
grid-gap: 100px 1em
```
```
grid-gap: 2rem
```

## Positioning Items by Grid Line Numbers.
Grid lines are essentially lines that represent the start of, the end of, or between column and row tracks.

Each line, starting from the start of the track and in the direction of the grid, is numbered incrementally starting from 1.
