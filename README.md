# css-notes
Notes for CSS

# CSS Selectors

## 1. Basic Selectors
| Selector | Description | Example | Matches |
|----------|-------------|---------|---------|
| `element` | Selects all elements of that type | `p { color: red; }` | All `<p>` |
| `.class` | Selects elements with a class | `.btn { background: blue; }` | `<button class="btn">` |
| `#id` | Selects a single element by ID | `#header { font-size: 20px; }` | `<div id="header">` |
| `*` | Universal selector (all elements) | `* { margin: 0; }` | All elements |

---

## 2. Grouping and Combining
| Selector | Example | Meaning |
|----------|---------|---------|
| `A, B` | `h1, h2 { color: blue; }` | Style multiple selectors |
| `A B` | `div p { color: gray; }` | Descendant selector (p inside div) |
| `A > B` | `div > p { font-weight: bold; }` | Direct child |
| `A + B` | `h1 + p { margin-top: 0; }` | Adjacent sibling |
| `A ~ B` | `h1 ~ p { color: red; }` | General sibling |

---

## 3. Pseudo-classes (State-based)
| Example | Description |
|---------|-------------|
| `a:hover` | When hovered |
| `a:active` | When clicked |
| `input:focus` | When focused |
| `li:first-child` | First child |
| `li:last-child` | Last child |
| `li:nth-child(2)` | Second child |
| `:not(selector)` | Negation |

---

## 4. Pseudo-elements (Part of an element)
| Example | Description |
|---------|-------------|
| `p::first-line` | First line of text |
| `p::first-letter` | First letter |
| `::before` | Content before element |
| `::after` | Content after element |


## Positioning
- absolute: Will be removed from the DOM. The other html elements treat it as it doesn't exists. Bahala ka san mo sya ilalagay.

- relative: Will take the value from the parent element and up in the heirarchy. Kung anong value ni parent ganun nadin sya.

- fixed: Will be removes from the DOM but it will scroll along with the page.
Susunod sa sayo kahit saan.

- static: default. Default!

- sticky: Just like fixed but it will only work with top attribute specified. It will start scrolling along with the page with the given top. Susunod sayo pag tinawag mona yung top attribute yon.

# Media query
- min-width: Will be applied when screen size is above to the specified unit.

- max-width: Will be applied when screen size is below to the specified unit.

# Float
- Will place the element either on top, bottom, left, or right inside its parent element. It will be removed from the DOM of its parent element only but the other elements will respect its position. unlike to abosulute positioning. So sa madaling salita kunware nasa kwarto ka kahit san ka pumwesto sa kwarto ok lang lahat ng gamit don magaadjust kung san mo gusto. So basically yung float property bahala ka sa buhay mo magpalutang lutang sa loob ng kwarto parang ganon.
![float-sample](https://github.com/user-attachments/assets/34be4771-effd-4f38-bfef-3c1377c1d2f2)

# Units
- em: Will be relative to parent or the element itself. Generally used for margin, padding, and widths.
- rem: Will be relative to the browser font size. Generally used for sizes.
- %: Will be relative to the parent element.
- vh: Will be relative to the screen size. yung patayo ba.
- wv: Will relative to the screen size also. yung pahiga ba.
- px: The myth the legend px alam monato dapat aba.

# Isolation
- Will make an element to be isolated from other elements. Meaning that an element declared as isolated will block all the styles coming from other element styles. The most useful this property is when creating a visual effect on an targeted element. In tagalog iisolate nya sarili nya lahat mg makakaapekto sakanya eh dinya papansinin para maging unique sya (visual effect).
![isolation-sample](https://github.com/user-attachments/assets/d73f44f3-7bde-43a9-a386-97e075097408)

# Display
- flex: The flex system.
- none: none
- block: Will make child elements display each row. Its like every element will take the 100% percent of width.
- inline: Will literally put the element inside the where it is declared and will not respect the size of parent. width and height doesnt apply here.
- inline-block: Will put the element inside where it is declared with respect to the parent size.
- grid: The grid system.

# Text
- font-family: Calibri, etc...
- font-weight: bold, etc...
- font-size: size
- font-style: italic, etc...
- text-align: center, right, left, etc...
- text-decoration: underline, etc...
- line-height: Control space between each line.
- letter-spacing: Control space between individual character.
- text-transform: uppercase, etc...
- text-overflow: clip or ellipsis, etc...

# Variables
Declare it inside the :root. All variables goes inside the :root.
```
:root {
   --variable-name: value;
   // Other variables
}
```
To use it
```
element {
   color: var(--variable-name);
}
```

# Box model
![box-model-sample](https://github.com/user-attachments/assets/aa1a76ef-3d73-41fa-b11a-ea6bd281e9f8)

# Inheritance
## Properties that are auto-inherited.
- color
- font-size
- font-family
- line-height
- text-align
Meaning that all properties related to the text and fonts are inherited while properties related to box model, layout, and positioning are not.

## Properties that are not auto-inherited.
- width
- height
- margin
- padding
- border
- background-color
Meaning that some of the parent propertues are not applied automatically in its child.

# Pseudo classes and elements
## Classes
- :hover
- :active
- :focus
- :visited
- :nth-child(n)
- :nth-of-type(n)
- :first-child
- :last-child
- :not(selector)
- :disabled
- etc...

## Elements
- ::before
- ::after
- ::first-letter
- ::first-line
- ::selection
- etc...

# Break after and before
- Utilities for controlling how a column or page should break an element.

# Box decoration
- Use to control a element how it is going to be rendered as if it is a one continuous fragmnet or block.

- Used to control whether properties like background, border, border-image, box-shadow, clip-path, margin, and padding should be rendered as if the element were one continuous fragment, or distinct blocks.

# Object fit
![object-fit-sample](https://github.com/user-attachments/assets/87ea4efd-4106-49a1-b5c1-6cf437c1004d)


# Object position
![object-position-sample](https://github.com/user-attachments/assets/510320ef-01b9-4b96-a8b8-37d5c44b3463)

# Overflow
- Sometimes the content doesnt fit inside its parent container and the content overflow. You can control that with this property.
![overflow-sample](https://github.com/user-attachments/assets/263200b7-33c1-4415-995b-e4e9e035ea21)

# Overscroll
- Controls how the scroll behaves when scrollable boundary reached. Set this always to contain. Ang default nito eh after mareach yung end magsscroll na yung page. Pero pag contain pagka nareach nya yung end ng scrollable content eh ok na di mahsscroll yung page.
![overscroll-sample](https://github.com/user-attachments/assets/f14178e7-3439-48f5-8f22-513bb27b6ac6)

# Flex
Keep in mind that when you specify an element to be display:flex it will create a cross where the main axis is based on your flex-direction since flex direction defaults to row the main axis by default is vertical. when you set the flex direction to be column the main axis will be horizontal.
![flex-sample](https://github.com/user-attachments/assets/33faf235-7fa4-4143-a514-52ddfdcb7832)

- flex-direction: row; // The default is row and can be change with column.
- justify-content: Will control the elements in the main-axis.
- align-items: will control the elements in the cross axis.
- flex-wrap: Will control how the elements in the main axis should behave. wrap or no-wrap.
- flex-grow: Can be used only in child element. It defines how a certain element takes ups a space.
![flex-grow-sample](https://github.com/user-attachments/assets/84d95d63-3f37-49de-a7ac-694c4ac806ae)

- flex-shrink: Can be used only in child element. It defines how a certain element start to shink before other elements.

- flex-basis: Can be used only in child element. It used to redefine the size of child element.

- align-self: Can be use only in child element if want you a certain element to be special in its position.
- gap: add gap to every element. use this instead of margin or padding.


# Tricks
- Make your element below to other element para di nya matakpan yung ibamg element nasa likod sya ba.
```
z-index: -1
```
- Removes the annoying scrollbar in your dom.
```css
overflow: hidden
```

- Always apply this to all your css files. Just include it dont ask why. Trust me it will helps.
```
*,
*::before,
*::after {
    box-sizing: border-box;
}

* {
    margin: 0;
    padding: 0;
    overflow: hidden;
}
```

## Background Attachment
- Controls how thr bs behaves when scrolled.
- Fixed
- Scroll
![Uploading image.png…]()

## Background clip
- Set what should the background occupy in box model
![background-clip-sample](https://github.com/user-attachments/assets/c0f94f47-e8c0-48f3-b78e-d31e5b9d5a8a)

###### Now that you know the fundamentals of CSS we now talk about proper front end development. This topic is not that mandatatory to learn. Build a css project first explore it yourself.

# To properly build a website you need three things.
1. THINK
2. PLAN
3. RESEARCH
4. IMPLEMENT

As you can see almost the coding part the implement step is just 1 step. It is because when you do all the 1 - 3 step its like you are done almost 70 percent so that when you start coding you dont randomly placing items and redoing the design over and over again.

# Headers
- Should be what was the website or topic all about.
- What your user want in your website or topic.

# Colors
- Standard of 4 color with black and white as default. The other will be the main color of your website

# Section
- Every section must answer a USER question directly.
- Every section must be consistent and transparent on information you want to convey.
- Every section text must be simple and no bullshit just say what you website is doing

