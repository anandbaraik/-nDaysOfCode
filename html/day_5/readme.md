# CSS

Css is something that helps a html page look better & attractive. it works in conjuction with html to provide a nice look, style & structure.

# Ways to include css

```
- inline css
- internal css
- external css
```

> If a particular element has all 3 types of styles applied (inline,internal,external) then which one will be applied?
> <br>Ans : inline style has the highest priority then comes internal style & the exernal css file which has the least priority.

## Selectors in css

It is used to find/select html elements you want to style.

```
- simple selector (name, id, class, type)
- combiator (based on specific relationship between elements)
- psuedo-class selector (select elements based on certain state of an element)
- psuedo-element selector (select & style part of an element)
- attribute (based on attribute/attribute value)
```

## Css variable

Custom properties in css. variables are set once & then their values can be used throughout the document & it is case-sensitve.

Ex:

```
:root{
    --main-bg-color: blue;
}
```

To access the css variable, specify the name of the variable inside `var()`.

Ex:

```
#element__id{
    background-color:var(--main-bg-color);
}
```
