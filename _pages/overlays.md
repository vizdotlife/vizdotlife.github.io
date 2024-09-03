---
layout: page
title: 
permalink: /overlays/
---


Below is documentation for Overlay filters. 


<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); /* Responsive columns */
        gap: 10px;
        padding: 10px;
    }
    .grid-item {
        background-color: #f0f0f0;
        border: 1px solid #ccc;
        padding: 15px;
        text-align: center;
        border-radius: 5px;
        box-sizing: border-box; /* Ensures padding is included in width */
        font-size: 1rem; /* Adjusts font size for better readability */
    }
    .grid-item a {
        text-decoration: none;
        color: #333;
        font-weight: bold;
        display: block; /* Makes the link fill the grid item */
        width: 100%;
        height: 100%;
    }
    .grid-item a:hover {
        color: #007acc;
    }
    @media (max-width: 600px) {
        .grid-item {
            font-size: 0.875rem; /* Adjust font size for smaller screens */
        }
    }
</style>

<div class="grid-container">
    <div class="grid-item"><a href="#cutout_circle">cutout_circle</a></div>
    <div class="grid-item"><a href="#cutout_diamond">cutout_diamond</a></div>
    <div class="grid-item"><a href="#cutout_heart">cutout_heart</a></div>
    <div class="grid-item"><a href="#cutout_hexagon">cutout_hexagon</a></div>
    <div class="grid-item"><a href="#cutout_oval">cutout_oval</a></div>
    <div class="grid-item"><a href="#cutout_square">cutout_square</a></div>
    <div class="grid-item"><a href="#cutout_star">cutout_star</a></div>
    <div class="grid-item"><a href="#cutout_triangle">cutout_triangle</a></div>

</div>

<a id="cutout_circle"></a>

# Circle Cutout Overlay Filter

## Description
The **Circle Cutout Overlay** filter applies a circular mask to an image, preserving the content inside the circle and optionally filling the outside with a specified color. This effect is useful for creating focused, vignette-style images.

## Properties

### color
- **Description**: The color used to fill the area outside the circle.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the circular mask.

---

[Back to Top](#)

---

<a id="cutout_diamond"></a>


# Diamond Cutout Overlay Filter

## Description
The **Diamond Cutout Overlay** filter applies a diamond-shaped mask to an image, preserving the content inside the diamond and optionally filling the outside with a specified color. This effect is useful for creating focused, geometric-style images.

## Properties

### color
- **Description**: The color used to fill the area outside the diamond.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the diamond-shaped mask.

---

[Back to Top](#)

---

<a id="cutout_heart"></a>


# Heart Cutout Overlay Filter

## Description
The **Heart Cutout Overlay** filter applies a heart-shaped mask to an image, preserving the content inside the heart and optionally filling the outside with a specified color. This effect is often used for creating romantic or sentimental images.

## Properties

### fill_color
- **Description**: The color used to fill the area outside the heart.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the heart-shaped mask.

---

[Back to Top](#)

---

<a id="cutout_hexagon"></a>

# Hexagon Cutout Overlay Filter

## Description
The **Hexagon Cutout Overlay** filter applies a hexagon-shaped mask to an image, preserving the content inside the hexagon and optionally filling the outside with a specified color. This effect is useful for creating geometric, stylized images.

## Properties

### color
- **Description**: The color used to fill the area outside the hexagon.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the hexagon-shaped mask.

---

[Back to Top](#)

---

<a id="cutout_oval"></a>


# Oval Cutout Overlay Filter

## Description
The **Oval Cutout Overlay** filter applies an oval-shaped mask to an image, preserving the content inside the oval and optionally filling the outside with a specified color. This effect is useful for creating vignette or portrait-style images.

## Properties

### color
- **Description**: The color used to fill the area outside the oval.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the oval-shaped mask.

---

[Back to Top](#)

---

<a id="cutout_square"></a>

# Square Cutout Overlay Filter

## Description
The **Square Cutout Overlay** filter applies a square-shaped mask to an image, preserving the content inside the square and optionally filling the outside with a specified color. This effect is useful for creating focused, framed images.

## Properties

### color
- **Description**: The color used to fill the area outside the square.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the square-shaped mask.

---

[Back to Top](#)

---

<a id="cutout_star"></a>

# Star Cutout Overlay Filter

## Description
The **Star Cutout Overlay** filter applies a star-shaped mask to an image, preserving the content inside the star and optionally filling the outside with a specified color. This effect is often used for creating celebratory or thematic images.

## Properties

### color
- **Description**: The color used to fill the area outside the star.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the star-shaped mask.

---

[Back to Top](#)

---

# Triangle Cutout Overlay Filter

## Description
The **Triangle Cutout Overlay** filter applies a triangle-shaped mask to an image, preserving the content inside the triangle and optionally filling the outside with a specified color. This effect is useful for creating geometric, stylized images.

## Properties

### color
- **Description**: The color used to fill the area outside the triangle.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the area outside the triangle-shaped mask.

---

[Back to Top](#)

---

# Frame and Matte Filter

## Description
The **Frame and Matte** filter adds a customizable frame and matte to the image, creating a classic picture framing effect.

## Properties

### frame_width
- **Description**: The width of the frame surrounding the image.
- **Value Type**: `Integer`
- **Usage**: Increase to make the frame wider.

### matte_width
- **Description**: The width of the matte inside the frame.
- **Value Type**: `Integer`
- **Usage**: Increase to make the matte wider.

### frame_color
- **Description**: The color of the frame.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the frame.

### matte_color
- **Description**: The color of the matte.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the matte.

---

[Back to Top](#)

---

# Number Overlay Filter

## Description
The **Number Overlay** filter overlays a number onto the image, often used for batch processing or indexing.

## Properties

### box_size
- **Description**: The size of the box around the number.
- **Value Type**: `Integer`
- **Usage**: Adjust to change the size of the overlay box.

### position_x
- **Description**: The X-coordinate for the position of the number.
- **Value Type**: `Integer`
- **Usage**: Adjust to move the number horizontally.

### position_y
- **Description**: The Y-coordinate for the position of the number.
- **Value Type**: `Integer`
- **Usage**: Adjust to move the number vertically.

### font_size
- **Description**: The font size of the number.
- **Value Type**: `Integer`
- **Usage**: Increase to make the number larger.

### box_color
- **Description**: The color of the box around the number.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color of the overlay box.

### text_color
- **Description**: The color of the number text.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color of the number.

---

[Back to Top](#)

---

# Watermark Filter

## Description
The **Watermark** filter overlays a text watermark onto the image.

## Properties

### watermark_text
- **Description**: The text to be used as the watermark.
- **Value Type**: `String`
- **Usage**: Provide the text to overlay on the image.

### watermark_position_x
- **Description**: The X-coordinate for the position of the watermark.
- **Value Type**: `Integer`
- **Usage**: Set the horizontal position of the watermark.

### watermark_position_y
- **Description**: The Y-coordinate for the position of the watermark.
- **Value Type**: `Integer`
- **Usage**: Set the vertical position of the watermark.

### watermark_opacity
- **Description**: The opacity of the watermark.
- **Value Type**: `Float`
- **Usage**: Increase to make the watermark more visible.

### watermark_color
- **Description**: The color of the watermark text.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color of the watermark text.

---

[Back to Top](#)

---

