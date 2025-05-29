Structured Notes Generated from PDF
--- Note Block 1 ---
## APNA COLLEGE - Web Development (Level 1)
**I. HTML Structure/Layout**
* Provides the content and structure of a webpage.
**II. CSS (Cascading Style Sheets)**
* **Purpose:** Styles the HTML content (makeup/appearance).
* **Type:** Styling language (NOT a programming language).
* **Dependency:** Requires HTML content to style.
* **Basic Syntax:**
 ```css
 selector {
 property: value;
 }
 ```
 * **Selector:** The HTML element to style (e.g., `h1`).
 * **Property:** The aspect of the element to change (e.g., `color`).
 * **Value:** The setting for the property (e.g., `red`).
 * **Semicolon (;):** Terminates a property declaration (best practice to include).
**III. Including CSS Styles**
* **1. Inline Styles:**
 * Directly within the HTML element using the `style` attribute.
 * Example: `<h1 style="color: red;">Apna College</h1>`
 * **Cons:** Hard to maintain, not scalable.
* **2. Internal Styles:**
 * Within the `<style>` tag inside the `<head>` of the HTML document.
 * Example:
 ```html
 <head>
 <style>
 h1 {
 color: red;
 }
 </style>
 </head>
 ```
* **3. External Stylesheet (BEST PRACTICE):**
 * CSS rules are written in a separate `.css` file.
 * Linked to the HTML document using the `<link>` tag in the `<head>`.
 * **Benefits:** Reusable, maintainable, organized.
**IV. CSS Properties**
* **Color:** Sets the text (foreground) color.
 * Example: `color: red;`, `color: blue;`
* **Background-Color:** Sets the background color.
 * Example: `background-color: red;`, `background-color: green;`
**V. Color Systems**
* **RGB (Red, Green, Blue):** Specifies colors using red, green, and blue values (0-255).
 * Example: `color: rgb(255, 0, 0);` (Red), `color: rgb(0, 255, 0);` (Green)
* **Tip:** Use online color picker tools to find RGB values.
**VI. CSS Specificity**
* Inline styles override internal and external styles. (Most Specific)
--- Note Block 2 ---
## CSS Study Notes
**Color Systems:**
* **Hexadecimal (Hex):** `#rrggbb` (e.g., `#ff0000` (red), `#00ff00` (green)). Use Google Color
Picker for values.
**CSS Selectors:**
* **Universal Selector:** `* { }` (selects all elements)
* **Element Selector:** `h1 { }` (selects all `h1` elements)
* **Id Selector:** `#myId { }` (selects element with `id="myId"`)
* **Class Selector:** `.myClass { }` (selects elements with `class="myClass"`)
**Practice Set 1:**
* **Q1:** Create `h1`, `h2`, and `h3` elements, give them all class `"heading"`, and set the
`"heading"` class color to red.
* **Q2:** Set button background color:
 * Green: External CSS stylesheet
 * Blue: `<style>` tag (internal CSS)
 * Pink: Inline style
* **Q3:** Create a simple `div` with `id="box"`, add text content, and set background color to blue.
**Text Properties:**
* **`text-align`:** `left | right | center | start | end`
 * Aligns text within its *parent* element, not the entire page. `start` and `end` are for language
support (e.g., Arabic).
* **`text-decoration`:** `underline | overline | line-through | none`
 * Can also set style (wavy, dotted) and color (e.g., red).
 * `none` often used to remove underline from hyperlinks.
* **`font-weight`:** `normal | bold | bolder | lighter | 100 - 900`
 * Controls text darkness/lightness. Numeric values from 100 (thin) to 900 (bold).
* **`font-family`:** `font-family: arial, roboto;`
 * Specifies font(s) to use. Provide multiple font families as a fallback mechanism if the first font
is unavailable.
--- Note Block 3 ---
## CSS Study Notes
**I. Units:**
* **Pixels (px):** Absolute unit, most commonly used. 96px = 1 inch.
* Other absolute units (cm, mm, inch, etc.) exist but are less frequent.
**II. Text Properties:**
* **`line-height`:**
 * Values: px (e.g., `line-height: 2px`), unitless (e.g., `line-height: 3`), `normal`.
* **`text-transform`:**
 * Values: `uppercase`, `lowercase`, `capitalize`, `none`.
**III. Practice Questions:**
* **Q1:** Center a heading on the page and capitalize all text by default.
* **Q2:** Nested Divs:
 * Outer `div` (id: "outer"): `font-size: 25px;`
 * Inner `div` (id: "inner"): `font-size: 10px;`
* **Q3:** (Referencing "Practice Set 2", specific details unclear in source material).
**IV. Box Model:**
* Components: **Content, Padding, Border, Margin**
 * **Content:** Default `height` and `width` determine the content area size.
 * `height`: `div { height: 50px; }`
 * `width`: `div { width: 50px; }`
 * **Border:**
 * Properties: `border-width`, `border-style`, `border-color`.
 * `border-style` values: `solid`, `dotted`, `dashed`.
 * Example: `border-width: 2px; border-style: solid; border-color: black;`
 * **Shorthand:** `border: 2px solid black;`
 * **`border-radius`:** Rounds the corners of an element's outer border edge.
 * Example: `border-radius: 10px;` , `border-radius: 50%;`
--- Note Block 4 ---
## CSS Box Model: Padding & Margin
**Padding:** Space *inside* an element, between content and border.
* Individual properties: `padding-top`, `padding-right`, `padding-bottom`, `padding-left`
* Shorthand: `padding: top right bottom left;` (clockwise)
 * Example: `padding: 1px 2px 3px 4px;`
 * All sides equal: `padding: 50px;`
**Margin:** Space *outside* an element, separating it from other elements.
* Individual properties: `margin-top`, `margin-right`, `margin-bottom`, `margin-left`
* Shorthand: `margin: top right bottom left;` (clockwise)
 * Example: `margin: 1px 2px 3px 4px;`
 * All sides equal: `margin: 50px;`
## Display Property
* **`inline`:** Takes only necessary space; ignores width/height and some margin/padding.
* **`block`:** Takes full available width; starts on a new line.
* **`inline-block`:** Like `inline`, but allows setting width, height, margin, and padding.
* **`none`:** Removes element from the document flow; no space is reserved.
## Visibility vs. Display: None
* **`visibility: hidden;`:** Hides the element, but *reserves* its space.
* **`display: none;`:** Hides the element and *does not* reserve its space.
## RGBA & Opacity
* **`opacity: 0 to 1;`:** Controls the transparency of an element.
* **`RGBA(red, green, blue, alpha);`:** Specifies color with an alpha (transparency) value. Alpha
ranges from 0 (fully transparent) to 1 (fully opaque).
 * Example: `color: rgba(255, 0, 0, 0.5);` (red with 50% opacity)
 * Example: `color: rgba(255, 0, 0, 1);` (red with full opacity)
## Practice Questions (Key Elements)
* **Q1:** Create div: `height: 100px; width: 100px; background-color: green; border-radius: 50%;`
(Creates a green circle)
* **Q2:** Create navbar with:
 * Background Colors: `#f08804` (yellow), `#0f1111` (black)
 * Height: `60px`
 * Text size: `25px`
 * Gap between links: `200px`
 * Elements: Anchor tags (links)
--- Note Block 5 ---
## Webpage Layout Study Notes
**I. Basic Structure:**
* Create a webpage with:
 * Header (includes pre-existing navbar)
 * Content Area (containing 3 divs)
 * Footer
**II. Div Styling (Content Area):**
* Each div:
 * `height: 100px;`
 * `width: 100px;`
 * Border
**III. Div Styling (Advanced):**
* Each div:
 * Different background color
 * Background opacity: `0.5`
**IV. Content Area Height:**
* Set an appropriate height for the content area.
**V. CSS Units - Relative:**
* **Percentage (%)**:
 * Relative to parent element's size. Example: `width: 33%;`
 * Can also be relative to other properties, but less common.
 * Example: `margin-left: 50%;`
 * Example: Parent & child divs, h1 child shows 50% of parent.
* **Em (em)**:
 * Relative to *element's own font size*.
 * Example: `font-size: 0.5em;` (child font size is half of parent's).
 * For `padding` & `margin`, relative to the *same element's* font size.
 * Example: Paragraph & div showcasing em differences.
 * Application: Button with border & font-size; transition `border-radius` from `px` to `em` for
consistent shape.
* **Rem (Root Em)**:
 * Relative to *root (html) element's font size*.
 * Example: `font-size: 0.5em;` (child font size is half of root's).
 * For `padding` & `margin`, relative to the *root element's* font size.
 * Example: Paragraph & div showcasing rem differences.
 * Application: Button with border & font-size; transition `border-radius` from `px` to `em` for
consistent shape.
* **Viewport Units:**
 * `vh`: Relative to 1% of viewport height.
 * `vw`: Relative to 1% of viewport width.
--- Note Block 6 ---
## CSS Positioning & Background: Study Notes
**I. Position Property:** Defines how an element is positioned.
* **Syntax:** `position: static | relative | absolute | fixed | sticky;`
 * **`static` (Default):** Standard document flow. `top`, `right`, `bottom`, `left`, and `z-index` have
no effect.
 * **`relative`:** Positioned relative to its *normal* (static) position. `top`, `right`, `bottom`, `left`,
and `z-index` work.
 * **`absolute`:** Positioned relative to its *closest positioned ancestor* (an ancestor with a
`position` other than `static`). Removed from normal document flow.
 * **`fixed`:** Positioned relative to the browser window/viewport. Removed from normal
document flow. Stays in the same place even on scroll.
 * **`sticky`:** Positioned based on the user's scroll position.
**II. Z-Index:** Controls the stacking order of overlapping elements.
* **Syntax:** `z-index: auto | <number>;`
 * `auto` (default): Equivalent to `0`.
 * `<number>`: Can be positive, negative, or zero. Higher values are closer to the viewer.
* Elements with a higher `z-index` value appear on top of elements with lower values.
**III. Background Image:** Sets an image as the background of an element.
* **Syntax:** `background-image: url("image.jpeg");`
**IV. Background Size:** Determines how the background image is sized within its container.
* **Syntax:** `background-size: cover | contain | auto;`
 * `cover`: Fills the entire container, potentially cropping the image.
 * `contain`: Fits the entire image within the container, potentially leaving empty space.
 * `auto`: Uses the image's original size.
--- Note Block 7 ---
## Flexbox Study Notes
**Definition:** One-dimensional layout model for arranging items in rows or columns.
**Key Concepts:**
* **Flex Container:** Parent element with `display: flex;`
* **Flex Item:** Child elements within the flex container.
* **Main Axis:** Axis along which flex items are primarily arranged (determined by `flex-direction`).
* **Cross Axis:** Axis perpendicular to the main axis.
**Flexbox Direction (`flex-direction`):**
* `row` (default): Items arranged horizontally (left to right).
* `row-reverse`: Items arranged horizontally (right to left).
* `column`: Items arranged vertically (top to bottom).
* `column-reverse`: Items arranged vertically (bottom to top).
**Flex Container Properties:**
* **`justify-content`:** Alignment along the *main* axis.
 * `flex-start`: Items aligned to the start of the main axis.
 * `flex-end`: Items aligned to the end of the main axis.
 * `center`: Items centered along the main axis.
 * `space-evenly`: Items evenly distributed along the main axis with equal space around them.
* **`flex-wrap`:** Handling overflow along the main axis.
 * `nowrap`: Items stay in a single line (default).
 * `wrap`: Items wrap to the next line if they overflow.
 * `wrap-reverse`: Items wrap to the previous line if they overflow.
* **`align-items`:** Alignment along the *cross* axis (within each line).
* **`align-content`:** Alignment of lines (or multiple rows/columns) along the *cross* axis. Controls
spacing *between* lines.
**Flex Item Properties:**
* **`align-self`:** Alignment along the *cross* axis for a *single item*. Overrides `align-items`.
* **`flex-grow`:** How much the item will grow relative to other flex items if there is available space.
(Values: 0, 1, 2, 3...). 0 = doesn't grow.
* **`flex-shrink`:** How much the item will shrink relative to other flex items if there is not enough
space. (Values: 0, 1, 2, 3...). 0 = doesn't shrink.
--- Note Block 8 ---
## Study Notes: Flexbox & Media Queries
**I. Flexbox**
* **Navbar Layout:**
 * Create a `<ul>` with four `<li>` containing `<a>` tags for navigation links.
 * Use flexbox on the `<ul>` to display the `<li>` in a single line with equal spacing.
* **Centering:** Use flexbox to horizontally and vertically center a `<div>` inside another `<div>`.
* **Alignment Priority:** `align-self` has higher priority than `align-items`.
**II. Media Queries (Responsive Design)**
* **Purpose:** Create responsive websites that adapt to different screen sizes and orientations.
* **Why Important:** Users access websites on diverse devices (laptops, phones, tablets) with
varying screen resolutions and orientations (portrait/landscape).
* **`@media` Rule:**
 * Used to apply different CSS styles based on screen size or other media features.
 * Example:
 ```css
 @media (width: 600px) {
 div {
 background-color: red;
 }
 }
 @media (min-width: 600px) {
 div {
 background-color: red;
 }
 }
 ```
 * The first query applies styles when the screen width is exactly 600px.
 * The second query applies styles when the screen width is 600px or more.
--- Note Block 9 ---
**Media Queries: Responsive Design**
* **Problem:** Websites need to look good on a variety of devices with different screen sizes and
orientations (portrait/landscape).
* **Solution:** Use responsive design with Media Queries in CSS. Media queries allow styles to be
applied conditionally based on device characteristics.
**Syntax Example:**
```css
@media (min-width: 200px) and (max-width: 300px) {
 div {
 background-color: red;
 }
}
```
**Common Use Cases (Practice Set):**
* Change `div` color based on viewport width:
 * `< 300px`: Green
 * `300px - 400px`: Pink
 * `400px - 600px`: Red
 * `> 600px`: Blue
**Note:** While Media Queries are considered more advanced CSS and may not be used
*constantly*, understanding them is crucial.
--- Note Block 10 ---
## CSS Transitions & Transforms: Study Notes
**I. CSS Transitions:**
* **Purpose:** Animate changes between two element states (e.g., hover).
* **Components:**
 * `transition-property`: The CSS property to animate (e.g., `font-size`, `width`).
 * `transition-duration`: Length of the transition (e.g., `2s`, `4ms`).
 * `transition-timing-function`: Determines the transition's speed curve (e.g., `ease-in`,
`ease-out`, `linear`, `steps`).
 * `transition-delay`: Time to wait before the transition starts (e.g., `2s`, `4ms`).
* **Shorthand:** `transition: property duration timing-function delay;`
 * Example: `transition: font-size 2s ease-in-out 0.2s;`
**II. CSS Transforms:**
* **Purpose:** Apply 2D & 3D transformations to elements.
* **Types:**
 * **Rotate:** Rotates an element. Uses angles (degrees are common). `transform:
rotate(45deg);` Affects content inside the element.
 * **Scale:** Resizes an element.
 * `transform: scale(2);` (Enlarges by factor of 2)
 * `transform: scale(0.5);` (Shrinks by factor of 0.5)
 * `transform: scaleX(0.5);` (Scales horizontally)
 * `transform: scaleY(0.5);` (Scales vertically)
 * `transform: scale(1, 2);` (Scales horizontally by 1, vertically by 2)
 * **Translate:** Moves an element.
 * `transform: translate(20px);` (Moves horizontally)
 * `transform: translateX(20px);` (Moves horizontally)
 * `transform: translateY(20px);` (Moves vertically)
 * `transform: translate(20px, 50px);` (Moves horizontally and vertically)
 * Units can be `px`, `%`, `em`, `rem`, etc. Negative values are allowed.
 * **Skew:** Skews an element (distorts at an angle).
 * `transform: skew(30deg);`
--- Note Block 11 ---
**Animation (CSS)**
* **@keyframes:** Defines animation sequences.
 * Example:
 ```css
 @keyframes myName {
 from { font-size: 20px; }
 to { font-size: 40px; }
 }
 ```
 * Can also use percentages (0%, 50%, 100%) instead of `from` and `to`.
* **Animation Properties (Individual):**
 * `animation-name`: Name of the `@keyframes` animation to use.
 * `animation-duration`: Time for one animation cycle (e.g., `2s`).
 * `animation-timing-function`: Animation speed curve (e.g., `linear`, `ease`).
 * `animation-delay`: Delay before the animation starts (e.g., `3s`).
 * `animation-iteration-count`: Number of times the animation repeats (e.g., `3`, `infinite`).
 * `animation-direction`: Direction of animation playback (e.g., `normal`, `reverse`, `alternate`).
* **Animation Shorthand:** Combines multiple animation properties.
 * Syntax: `animation: name duration timing-function delay iteration-count direction;`
 * Example: `animation: myName 2s linear 3s infinite normal;`
**Creating a CSS Loader (Example)**
1. **Create a Circular Div:** Style a `div` with a circular shape and a thick border on one side (e.g.,
top, bottom, left, or right).
2. **Create Spinning Animation:** Use `@keyframes` to define an animation that rotates the `div`
from 0 degrees to 360 degrees.
3. **Apply Animation:** Add the `animation` property to the loader element, setting the duration to
`infinite`.
