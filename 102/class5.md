**Design Websites with CSS**

1.**What is the purpose of CSS?** *It is for the presentation and layout of webpages.*

2.**What are the three ways to insert CSS into your project?** *inline, internal, & external.*

3.**Write an example of a CSS rule that would give all `<p>` elements=== red text.** *`<p>` {color: red}*

**Vocab**
CSS
+ CSS stands for Cascading Style Sheets. It is a stylesheet language used to describe the presentation of a document written in HTML or XML, defining how elements on a web page should be displayed in terms of layout, colors, fonts, and other visual features.
RGB
+ RGB stands for Red, Green, and Blue. It is a color model used in various electronic displays, such as computer monitors and TVs, as well as in digital imaging. Colors are created by combining different intensities of these three primary colors. When combined in various ways, RGB can produce a wide range of colors.
HSL
+ HSL stands for Hue, Saturation, and Lightness. It is a color model used in computer graphics and web design to represent colors in a way that is more intuitive than the RGB model.

+ Hue represents the type of color (e.g., red, blue, yellow) and is measured in degrees (0° to 360°) on the color wheel.
+ Saturation refers to the intensity or purity of the color, where 100% is fully saturated (pure color) and 0% is grayscale.
+ Lightness refers to the brightness of the color, ranging from 0% (black) to 100% (white).
*HSL is often used in design because it allows for easier manipulation of color tones, shades, and brightness than the RGB model.*
Hex codes
+ Hex codes (or hexadecimal color codes) are a way of representing colors in web design and digital graphics using a six-digit, base-16 (hexadecimal) format. They are primarily used in HTML, CSS, and other design languages to specify colors.

 + A hex code begins with a # followed by six characters, which can be digits (0–9) or letters (A–F). These six characters represent the RGB (Red, Green, Blue) color values in hexadecimal form.

The format is #RRGGBB, where:

- RR is the red component.
- GG is the green component.
- BB is the blue component.
- Each pair of characters ranges from 00 (no intensity) to FF (full intensity).

For example:

#FFFFFF represents white (full red, green, and blue).
#000000 represents black (no red, green, or blue).
#FF5733 is a shade of orange.
Hex codes allow designers to specify exact colors for web elements, ensuring consistent appearance across platforms.

Layout
+ In design and web development, layout refers to the arrangement and organization of visual elements (such as text, images, buttons, and other content) on a page or screen. It determines how different components are positioned and how they relate to one another within the space.

In the context of web design or CSS, layout defines the structure of a web page. This includes:

- Positioning of elements (e.g., headers, footers, sidebars, main content areas).
- Spacing (margins, padding, and the gap between elements).
- Alignment of text, images, and other components.
- Flow of content, particularly how elements respond and adjust to different screen sizes (responsive design).

Rules
 + In CSS, rules (or rule sets) are the fundamental building blocks that define how HTML elements should be styled on a web page. Each rule specifies the style properties that should be applied to one or more elements.
+ A CSS rule consists of two main parts:

+ Selector: Defines which HTML element(s) the rule applies to. It can target elements by tag name, class, ID, attribute, or a combination of these.
+ Declaration block: Contains one or more declarations, enclosed in curly braces {}, where each declaration specifies a CSS property and its corresponding value.

**Key Components**:
*Selector*: Targets the HTML elements to be styled.
*Property*: Specifies what aspect of the element (e.g., color, font size, margin) is being modified.
*Value*: Defines how the property is styled (e.g., the actual color, size, etc.).

Selectors
+ A selector in CSS is a pattern used to target and select specific HTML elements that you want to style. It defines which elements the style rules will apply to. Selectors allow you to choose elements based on their tag names, classes, IDs, attributes, and other characteristics.
    -type slector- tag selector `<p>`
    - class example `.class_of_element`
    - id selector- targets single element with specific `<id>` ex: `#unique_id`
    -universal selctor `<*>` means ALL
    -Attribute Selector: Targets elements based on the presence or value of an attribute 
            input[type="text"] {
    border: 1px solid black;}
    - Descendant Selector: Targets elements that are nested inside a specific element. This is written by separating selectors with a space