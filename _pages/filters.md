---
layout: page
title: 
permalink: /filters/
---

<iframe src="https://player.vimeo.com/video/344009812" width="320" height="180" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

Below is documentation on each filter. 


[Go to anaglyph_3d](#anaglyph_3d)  
[Go to annotations_yolov8](#annotations_yolov8)  
[Go to ascii_art](#ascii_art)  
[Go to background_removal_kmeans](#background_removal_kmeans)  
[Go to bg_removal_grabcut](#bg_removal_grabcut)  
[Go to bg_removal_human](#bg_removal_human)  
[Go to bilateral](#bilateral)  
[Go to blueprint](#blueprint)  
[Go to blur](#blur)  
[Go to canny_edge_detection](#canny_edge_detection)  
[Go to cartoon](#cartoon)  
[Go to charcoal_sketch](#charcoal_sketch)  
[Go to chrome](#chrome)  
[Go to color_histogram](#color_histogram)  
[Go to color_palette](#color_palette)  
[Go to color_palette_layover](#color_palette_layover)  
[Go to color_quantization](#color_quantization)  
[Go to contains_text](#contains_text)  
[Go to contour](#contour)  
[Go to crystallize](#crystallize)  
[Go to cutout_circle](#cutout_circle)  
[Go to cutout_diamond](#cutout_diamond)  
[Go to cutout_heart](#cutout_heart)  
[Go to cutout_hexagon](#cutout_hexagon)  
[Go to cutout_oval](#cutout_oval)  
[Go to cutout_square](#cutout_square)  
[Go to cutout_star](#cutout_star)  
[Go to cutout_triangle](#cutout_triangle)  
[Go to cyberpunk](#cyberpunk)  
[Go to denoise](#denoise)  
[Go to depth_map](#depth_map)  
[Go to depth_map_v2](#depth_map_v2)  
[Go to detail](#detail)  
[Go to diffuse_glow](#diffuse_glow)  
[Go to dotted_halftone](#dotted_halftone)  
[Go to edge_enhance](#edge_enhance)  
[Go to emboss](#emboss)  
[Go to engrave](#engrave)  
[Go to extrude_3d](#extrude_3d)  
[Go to eye_detection](#eye_detection)  
[Go to face_detection](#face_detection)  
[Go to find_edges](#find_edges)  
[Go to fire](#fire)  
[Go to fisheye](#fisheye)  
[Go to frosted_glass](#frosted_glass)  
[Go to gaussian_blur](#gaussian_blur)  
[Go to gaussian_splatter](#gaussian_splatter)  
[Go to glass_distortion](#glass_distortion)  
[Go to glitch_art](#glitch_art)  
[Go to heatmap](#heatmap)  
[Go to high_pass](#high_pass)  
[Go to hsv](#hsv)  
[Go to invert_colors](#invert_colors)  
[Go to kaleidoscope](#kaleidoscope)  
[Go to laplacian](#laplacian)  
[Go to limit_rows](#limit_rows)  
[Go to median_blur](#median_blur)  
[Go to mosaic](#mosaic)  
[Go to motion_blur](#motion_blur)  
[Go to motion_detection](#motion_detection)  
[Go to negative](#negative)  
[Go to number_overlay](#number_overlay)  
[Go to object_isolation](#object_isolation)  
[Go to object_isolation_adv](#object_isolation_adv)  
[Go to object_largest_isolation](#object_largest_isolation)  
[Go to old_photo](#old_photo)  
[Go to pencil_sketch](#pencil_sketch)  
[Go to pixel_sort](#pixel_sort)  
[Go to pixelate](#pixelate)  
[Go to posterize](#posterize)  
[Go to primary_color](#primary_color)  
[Go to pytorch_edge_detection](#pytorch_edge_detection)  
[Go to rainbow](#rainbow)  
[Go to replace_color](#replace_color)  
[Go to retro_tv](#retro_tv)  
[Go to ripple](#ripple)  
[Go to rotation](#rotation)  
[Go to seamless_texture](#seamless_texture)  
[Go to search_tags](#search_tags)  
[Go to sepia](#sepia)  
[Go to sharpen](#sharpen)  
[Go to solarize](#solarize)  
[Go to swirl](#swirl)  
[Go to tritone](#tritone)  
[Go to vignette](#vignette)  
[Go to vortex](#vortex)  
[Go to watermark](#watermark)  
[Go to xray](#xray)







# Anaglyph 3D Filter



## Description
The **Anaglyph 3D** filter creates a stereoscopic 3D effect by shifting and recoloring the image's red, green, and blue channels. This effect is commonly used for creating images that can be viewed with red-cyan 3D glasses, giving the impression of depth.

## Properties

### shift_amount
- **Description**: Determines how much the image channels are shifted relative to each other.
- **Value Type**: Integer
- **Usage**: A higher value increases the separation between channels, enhancing the 3D effect but potentially causing more distortion.

### red_weight
- **Description**: Adjusts the intensity of the red channel.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Modify this value to balance the red channel’s contribution to the final image.

### blue_weight
- **Description**: Adjusts the intensity of the blue channel.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Modify this value to balance the blue channel’s contribution to the final image.

### green_weight
- **Description**: Adjusts the intensity of the green channel.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Modify this value to balance the green channel’s contribution to the final image.

### shift_direction
- **Description**: Specifies the direction in which the image channels are shifted.
- **Value Type**: String (options: "horizontal", "vertical")
- **Usage**: Choose "horizontal" for a side-to-side shift or "vertical" for an up-and-down shift.

### color_tuning
- **Description**: Applies additional color tuning to the final anaglyph image.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Use this to fine-tune the colors, especially when creating more subtle or exaggerated 3D effects.

---

[Back to Top](#)

---

# Annotations YOLOv8 Filter

## Description
The **Annotations YOLOv8** filter uses the YOLOv8 object detection model to detect objects within an image and annotate them with bounding boxes and labels.

## Properties

### confidence_threshold
- **Description**: The confidence threshold for keeping detected objects.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Only objects detected with confidence above this threshold will be annotated.

### nms_threshold
- **Description**: The threshold for non-maxima suppression, used to eliminate overlapping bounding boxes.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Higher values reduce the number of overlapping boxes.

### box_color
- **Description**: The color of the bounding box.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Defines the color of the boxes drawn around detected objects.

### text_color
- **Description**: The color of the label text.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Defines the color of the text labels for detected objects.

### font_scale
- **Description**: The scale of the text labels.
- **Value Type**: Float
- **Usage**: Adjusts the size of the text labels.

### box_thickness
- **Description**: The thickness of the bounding box lines.
- **Value Type**: Integer
- **Usage**: Defines the thickness of the lines for the bounding boxes.

---

[Back to Top](#)

---

# ASCII Art Filter

## Description
The **ASCII Art** filter converts an image into an artistic representation using ASCII characters. This effect is often used to create stylized, text-based versions of images.

## Properties

### ascii_chars
- **Description**: A custom set of characters used to represent pixel intensities.
- **Value Type**: String
- **Usage**: Define a string of characters where each character represents a different level of brightness.

### ascii_scale
- **Description**: The scale factor for the ASCII output.
- **Value Type**: Integer
- **Usage**: Larger values result in fewer characters, with each character representing more pixels.

### ascii_invert
- **Description**: Inverts the character mapping so that dark areas use brighter characters and vice versa.
- **Value Type**: Boolean
- **Usage**: Set to True to invert the character mapping.

### ascii_font_size
- **Description**: The size of the font used to render the ASCII characters.
- **Value Type**: Integer
- **Usage**: Adjust the font size for the ASCII art.

### ascii_brightness
- **Description**: Adjusts the brightness of the grayscale image before converting it to ASCII.
- **Value Type**: Float
- **Usage**: Modify this value to increase or decrease the overall brightness of the ASCII art.

### ascii_font_color
- **Description**: The color used for the ASCII characters.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Define the color for the characters in the ASCII art.

### ascii_background_color
- **Description**: The background color for the ASCII art image.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the background behind the ASCII characters.

---

[Back to Top](#)

---

# Background Removal K-Means Filter

## Description
The **Background Removal K-Means** filter uses K-Means clustering to segment an image and remove the background, replacing it with a specified color.

## Properties

### k_clusters
- **Description**: The number of clusters used in K-Means clustering.
- **Value Type**: Integer
- **Usage**: Higher values create more distinct regions in the image.

### max_iterations
- **Description**: The maximum number of iterations for the K-Means algorithm.
- **Value Type**: Integer
- **Usage**: Increase this value to allow the algorithm more time to converge.

### epsilon
- **Description**: The convergence threshold for K-Means clustering.
- **Value Type**: Float
- **Usage**: Smaller values make the algorithm more precise but slower.

### attempts
- **Description**: The number of attempts the algorithm makes to perform clustering.
- **Value Type**: Integer
- **Usage**: Increase this value for better clustering results.

### invert_mask
- **Description**: Inverts the mask created by K-Means, swapping the foreground and background.
- **Value Type**: Boolean
- **Usage**: Set to True to invert the mask and swap the foreground and background areas.

### background_color
- **Description**: The color used to replace the background.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the background after the original background is removed.

### kmeans_flag
- **Description**: The flag for the K-Means algorithm, determining the initialization method.
- **Value Type**: String (options: "RANDOM_CENTERS", "PP_CENTERS")
- **Usage**: Choose "RANDOM_CENTERS" for random initialization or "PP_CENTERS" for more accurate initialization.

---

[Back to Top](#)


# Background Removal GrabCut Filter

## Description
The **Background Removal GrabCut** filter uses the GrabCut algorithm enhanced with object detection to remove the background from images. This technique is effective for isolating objects in the foreground while replacing the background with a specified color.

## Properties

### confidence_threshold
- **Description**: The confidence threshold for object detection.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Objects detected with confidence above this threshold are used for background removal.

### iter_count
- **Description**: The number of iterations for the GrabCut algorithm.
- **Value Type**: Integer
- **Usage**: Increase this value to allow the GrabCut algorithm more time to refine the mask.

### resize_factor
- **Description**: The factor by which the image is resized for faster processing.
- **Value Type**: Float
- **Usage**: Smaller values reduce processing time but may decrease accuracy.

### morph_operations
- **Description**: Specifies whether to apply morphological operations to refine the mask.
- **Value Type**: Boolean
- **Usage**: Set to True to apply operations such as erosion and dilation to improve the mask.

### background_color
- **Description**: The color used to replace the background.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the background after the original background is removed.

---

[Back to Top](#)

---

# Background Removal Human Filter

## Description
The **Background Removal Human** filter isolates human figures from the background using a combination of object detection and the DeepLabV3 segmentation model. The background can be replaced with a specified color, making it useful for applications like virtual backgrounds.

## Properties

### confidence_threshold
- **Description**: The confidence threshold for object detection.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Objects detected with confidence above this threshold are used for background removal.

### iter_count
- **Description**: The number of iterations for the GrabCut algorithm.
- **Value Type**: Integer
- **Usage**: Increase this value to allow the GrabCut algorithm more time to refine the mask.

### resize_factor
- **Description**: The factor by which the image is resized for faster processing.
- **Value Type**: Float
- **Usage**: Smaller values reduce processing time but may decrease accuracy.

### background_color
- **Description**: The color used to replace the background.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color to fill the background after the original background is removed.

### box_expansion
- **Description**: Expands the bounding boxes around detected humans to ensure the entire figure is captured.
- **Value Type**: Float
- **Usage**: Increase this value to include more of the surroundings in the mask.

### use_deeplab
- **Description**: Specifies whether to use the DeepLabV3 model for more accurate segmentation.
- **Value Type**: Boolean
- **Usage**: Set to True to enable the DeepLabV3 model for enhanced segmentation accuracy.

---

[Back to Top](#)

---

# Bilateral Filter

## Description
The **Bilateral Filter** is a noise-reducing filter that preserves edges. It smooths images while maintaining sharp edges, making it useful for applications like cartooning and noise reduction in photos.

## Properties

### diameter
- **Description**: The diameter of the pixel neighborhood used for filtering.
- **Value Type**: Integer
- **Usage**: Larger values increase the neighborhood size, affecting more pixels.

### sigma_color
- **Description**: The filter’s sensitivity to color differences.
- **Value Type**: Float
- **Usage**: Higher values smooth regions with similar colors, preserving edges more effectively.

### sigma_space
- **Description**: The filter’s sensitivity to spatial differences.
- **Value Type**: Float
- **Usage**: Higher values smooth across larger areas, affecting more distant pixels.

---

[Back to Top](#)

---

# Blueprint Filter

## Description
The **Blueprint Filter** creates a blueprint-like effect by inverting the colors, applying edge detection, and mapping the result to a color map. This filter is useful for stylizing images in a technical or artistic manner.

## Properties

### intensity
- **Description**: Adjusts the intensity of the inversion effect.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Higher values increase the intensity of the inversion, creating a stronger blueprint effect.

### colormap
- **Description**: Specifies the color map applied to the inverted image.
- **Value Type**: String
- **Usage**: Choose a color map like "HOT", "COOL", or "JET" to apply different color schemes to the blueprint.

### edge_detection
- **Description**: Toggles edge detection before applying the blueprint effect.
- **Value Type**: Boolean
- **Usage**: Set to True to enhance edges in the image, making the blueprint effect more pronounced.

### edge_threshold
- **Description**: The threshold for edge detection.
- **Value Type**: Integer
- **Usage**: Lower values detect more edges, while higher values focus on stronger edges.

### smoothing
- **Description**: Applies Gaussian smoothing before processing the image.
- **Value Type**: Float
- **Usage**: Increase this value to smooth the image, reducing noise before applying the blueprint effect.

---

[Back to Top](#)

---

# Blur Filter

## Description
The **Blur Filter** applies a blurring effect to an image, softening its appearance. This can be used to reduce noise, create depth of field effects, or prepare images for further processing.

## Properties

### blur_radius
- **Description**: The radius of the blur effect.
- **Value Type**: Float
- **Usage**: Larger values increase the blur, softening more of the image.

### blur_mode
- **Description**: Specifies the type of blur to apply (e.g., Gaussian, Box).
- **Value Type**: String (options: "GAUSSIAN", "BOX", "BLUR")
- **Usage**: Choose the blur mode based on the desired effect. "GAUSSIAN" provides a natural blur, while "BOX" is faster.

### blur_quality
- **Description**: The quality of the blur effect.
- **Value Type**: Integer
- **Usage**: Higher values increase the quality but may slow down processing.

### blur_apply_to_alpha
- **Description**: Specifies whether to apply the blur to the alpha (transparency) channel.
- **Value Type**: Boolean
- **Usage**: Set to True to blur the alpha channel along with the color channels.

---

[Back to Top](#)

---

# Canny Edge Detection Filter

## Description
The **Canny Edge Detection** filter detects edges in an image using the Canny algorithm. It is widely used in image processing to identify boundaries and enhance features in images.

## Properties

### threshold1
- **Description**: The first threshold for the hysteresis procedure.
- **Value Type**: Integer
- **Usage**: Lower values detect more edges, but may include noise.

### threshold2
- **Description**: The second threshold for the hysteresis procedure.
- **Value Type**: Integer
- **Usage**: Higher values focus on strong edges, reducing noise.

### aperture_size
- **Description**: The aperture size for the Sobel operator.
- **Value Type**: Integer
- **Usage**: Typical values are 3, 5, or 7. Larger values detect broader edges.

### l2_gradient
- **Description**: Specifies whether to use a more accurate L2 gradient for edge detection.
- **Value Type**: Boolean
- **Usage**: Set to True for more accurate edge detection at the cost of processing speed.

### line_color
- **Description**: The color of the detected edges.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color for the edges detected by the algorithm.

### background_color
- **Description**: The color used to fill areas without detected edges.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color for the background areas of the image.

---

[Back to Top](#)

---

# Cartoon Filter

## Description
The **Cartoon Filter** transforms an image into a cartoon-like version by smoothing colors and enhancing edges. This effect is often used to create stylized, comic book-style images.

## Properties

### bilateral_d
- **Description**: The diameter of the pixel neighborhood used in the bilateral filter.
- **Value Type**: Integer
- **Usage**: Larger values increase the smoothing effect, which is key to the cartoon look.

### sigma_color
- **Description**: The filter’s sensitivity to color differences.
- **Value Type**: Float
- **Usage**: Higher values increase the smoothing of colors, preserving edges.

### sigma_space
- **Description**: The filter’s sensitivity to spatial differences.
- **Value Type**: Float
- **Usage**: Higher values smooth across larger areas, affecting more distant pixels.

### median_blur_size
- **Description**: The size of the kernel used for the median blur.
- **Value Type**: Integer
- **Usage**: Higher values reduce noise more effectively but may blur details.

### block_size
- **Description**: The size of the neighborhood used for adaptive thresholding.
- **Value Type**: Integer
- **Usage**: Smaller values detect more edges, creating a more detailed cartoon effect.

### c_value
- **Description**: A constant subtracted from the mean or weighted mean in adaptive thresholding.
- **Value Type**: Float
- **Usage**: Adjust this value to fine-tune the edge detection for the cartoon effect.

### edge_thickness
- **Description**: The thickness of the edges in the cartoon effect.
- **Value Type**: Integer
- **Usage**: Larger values produce thicker edges, enhancing the cartoon appearance.

### red_tint
- **Description**: Adjusts the red tint of the final image.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Modify this value to increase or decrease the red tones in the cartoon image.

### green_tint
- **Description**: Adjusts the green tint of the final image.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Modify this value to increase or decrease the green tones in the cartoon image.

### blue_tint
- **Description**: Adjusts the blue tint of the final image.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Modify this value to increase or decrease the blue tones in the cartoon image.

---

[Back to Top](#)

---

# Charcoal Sketch Filter

## Description
The **Charcoal Sketch** filter converts an image into a charcoal-style sketch by emphasizing edges and using grayscale tones. This effect is ideal for creating artistic, hand-drawn appearances.

## Properties

### blur_radius
- **Description**: The radius of the Gaussian blur applied to the image.
- **Value Type**: Integer
- **Usage**: Larger values create smoother transitions in the sketch.

### scale_factor
- **Description**: The scaling factor used in the division method to create the sketch effect.
- **Value Type**: Float
- **Usage**: Adjust this value to control the contrast and intensity of the sketch.

### contrast
- **Description**: Adjusts the contrast of the final sketch image.
- **Value Type**: Float
- **Usage**: Higher values increase the contrast, making the sketch more defined.

### brightness
- **Description**: Adjusts the brightness of the final sketch image.
- **Value Type**: Float
- **Usage**: Modify this value to increase or decrease the overall brightness of the sketch.

### tint_color
- **Description**: The color used to tint the final sketch image.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Apply a color tint to the sketch to give it a specific hue.

### sketch_color
- **Description**: The color of the sketch lines.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Define the color of the lines in the sketch.

### background_color
- **Description**: The color of the background in the sketch image.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the background color for the sketch, usually a light tone.

---

[Back to Top](#)

---

# Chrome Filter

## Description
The **Chrome Filter** applies a metallic chrome effect to an image by enhancing edges, adjusting brightness and contrast, and applying a color map. This effect is often used to create a shiny, reflective appearance.

## Properties

### colormap_type
- **Description**: Specifies the type of color map applied to the image.
- **Value Type**: String
- **Usage**: Choose a color map like "HOT", "COOL", or "JET" to apply different color schemes.

### intensity
- **Description**: Adjusts the intensity of the chrome effect.
- **Value Type**: Float (0.0 to 1.0)
- **Usage**: Higher values increase the intensity, making the chrome effect more pronounced.

### brightness
- **Description**: Adjusts the brightness of the image.
- **Value Type**: Float
- **Usage**: Modify this value to increase or decrease the overall brightness.

### contrast
- **Description**: Adjusts the contrast of the image.
- **Value Type**: Float
- **Usage**: Higher values increase the contrast, enhancing the chrome effect.

### tint_color
- **Description**: The color used to tint the final chrome image.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Apply a color tint to the chrome effect to give it a specific hue.

### edge_enhancement
- **Description**: Toggles the enhancement of edges in the image.
- **Value Type**: Boolean
- **Usage**: Set to True to enhance edges, making the chrome effect more defined.

---

[Back to Top](#)

---

# Color Histogram Filter

## Description
The **Color Histogram** filter calculates and displays the color histogram of an image. This visualization shows the distribution of colors in the image, which is useful for analyzing image content and color balance.

## Properties

### hist_bins
- **Description**: The number of bins used for the histogram.
- **Value Type**: Integer
- **Usage**: Higher values provide more detailed histograms but may increase noise.

### hist_range_min
- **Description**: The minimum range value for the histogram.
- **Value Type**: Integer
- **Usage**: Set the lower bound for the histogram range.

### hist_range_max
- **Description**: The maximum range value for the histogram.
- **Value Type**: Integer
- **Usage**: Set the upper bound for the histogram range.

### hist_height
- **Description**: The height of the histogram display.
- **Value Type**: Integer
- **Usage**: Increase this value to make the histogram taller.

### hist_width
- **Description**: The width of the histogram display.
- **Value Type**: Integer
- **Usage**: Increase this value to make the histogram wider.

### line_thickness
- **Description**: The thickness of the histogram lines.
- **Value Type**: Integer
- **Usage**: Increase this value to make the histogram lines thicker.

### line_color_r
- **Description**: The color of the red channel line.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the line representing the red channel in the histogram.

### line_color_g
- **Description**: The color of the green channel line.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the line representing the green channel in the histogram.

### line_color_b
- **Description**: The color of the blue channel line.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the line representing the blue channel in the histogram.

### background_color
- **Description**: The background color of the histogram display.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the background behind the histogram lines.

---

[Back to Top](#)

---

# Color Palette Filter

## Description
The **Color Palette** filter extracts the most dominant colors from an image and displays them as a color palette. This is useful for color analysis and creating consistent color schemes.

## Properties

### n_colors
- **Description**: The number of dominant colors to extract.
- **Value Type**: Integer
- **Usage**: Increase this value to extract more colors for the palette.

### display_width
- **Description**: The width of each color block in the palette.
- **Value Type**: Integer
- **Usage**: Adjust this value to control the width of each color block.

### display_height
- **Description**: The height of the color palette display.
- **Value Type**: Integer
- **Usage**: Adjust this value to control the height of the palette display.

### resize_factor
- **Description**: The factor by which the image is resized for faster processing.
- **Value Type**: Float
- **Usage**: Smaller values reduce processing time but may decrease accuracy.

### sorting
- **Description**: Specifies how to sort the colors in the palette (e.g., by frequency, brightness).
- **Value Type**: String (options: "Frequency", "Brightness")
- **Usage**: Choose "Frequency" to sort by how often each color appears, or "Brightness" to sort by brightness.

### border_width
- **Description**: The width of the border between color blocks.
- **Value Type**: Integer
- **Usage**: Increase this value to make the borders between colors thicker.

### border_color
- **Description**: The color of the border between color blocks.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the borders in the palette.

### rotation
- **Description**: Specifies the orientation of the palette (e.g., horizontal, vertical).
- **Value Type**: String (options: "Horizontal", "Vertical")
- **Usage**: Choose "Horizontal" for a horizontal palette or "Vertical" for a vertical one.

### include_rgb
- **Description**: Specifies whether to include the RGB values inside the color blocks.
- **Value Type**: Boolean
- **Usage**: Set to True to display RGB values within each color block.

---

[Back to Top](#)


# Color Palette Layover Filter

## Description
The **Color Palette Layover** filter extracts the most dominant colors from an image and overlays them as a color palette on the image itself. This is useful for visualizing the color distribution directly on the image.

## Properties

### n_colors
- **Description**: The number of dominant colors to extract.
- **Value Type**: Integer
- **Usage**: Increase this value to extract more colors for the palette.

### display_width
- **Description**: The width of each color block in the palette.
- **Value Type**: Integer
- **Usage**: Adjust this value to control the width of each color block.

### display_height
- **Description**: The height of the color palette display.
- **Value Type**: Integer
- **Usage**: Adjust this value to control the height of the palette display.

### resize_factor
- **Description**: The factor by which the image is resized for faster processing.
- **Value Type**: Float
- **Usage**: Smaller values reduce processing time but may decrease accuracy.

### sorting
- **Description**: Specifies how to sort the colors in the palette (e.g., by frequency, brightness).
- **Value Type**: String (options: "Frequency", "Brightness")
- **Usage**: Choose "Frequency" to sort by how often each color appears, or "Brightness" to sort by brightness.

### border_width
- **Description**: The width of the border between color blocks.
- **Value Type**: Integer
- **Usage**: Increase this value to make the borders between colors thicker.

### border_color
- **Description**: The color of the border between color blocks.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Set the color of the borders in the palette.

### rotation
- **Description**: Specifies the orientation of the palette (e.g., horizontal, vertical).
- **Value Type**: String (options: "Horizontal", "Vertical")
- **Usage**: Choose "Horizontal" for a horizontal palette or "Vertical" for a vertical one.

### include_rgb
- **Description**: Specifies whether to include the RGB values inside the color blocks.
- **Value Type**: Boolean
- **Usage**: Set to True to display RGB values within each color block.

### position
- **Description**: Specifies the position of the palette overlay on the image.
- **Value Type**: String (options: "Top Left", "Top Right", "Bottom Left", "Bottom Right", "Center")
- **Usage**: Choose the position where the palette will be overlaid on the image.

---

[Back to Top](#)

---

# Color Quantization Filter

## Description
The **Color Quantization** filter reduces the number of colors in an image by applying K-Means clustering. This effect is useful for artistic purposes and for reducing the complexity of images for certain applications.

## Properties

### K
- **Description**: The number of colors to reduce the image to.
- **Value Type**: Integer
- **Usage**: Increase this value to retain more colors in the image.

### criteria_type
- **Description**: The type of criteria used for the K-Means algorithm.
- **Value Type**: String (options: "EPS", "MAX_ITER", "EPS + MAX_ITER")
- **Usage**: Choose the criteria based on the desired convergence method.

### max_iterations
- **Description**: The maximum number of iterations for the K-Means algorithm.
- **Value Type**: Integer
- **Usage**: Higher values allow the algorithm more time to converge.

### epsilon
- **Description**: The convergence threshold for the K-Means algorithm.
- **Value Type**: Float
- **Usage**: Smaller values make the algorithm more precise but slower.

### attempts
- **Description**: The number of attempts the algorithm makes to perform clustering.
- **Value Type**: Integer
- **Usage**: Increase this value for better clustering results.

### color_space
- **Description**: The color space used for the quantization.
- **Value Type**: String (options: "RGB", "LAB", "HSV")
- **Usage**: Choose the color space based on the desired color manipulation.

### dithering
- **Description**: Specifies whether to apply dithering to the quantized image.
- **Value Type**: Boolean
- **Usage**: Set to True to apply dithering, which can help to reduce banding in the quantized image.

### concurrency
- **Description**: Specifies the number of threads used for concurrent processing.
- **Value Type**: Integer
- **Usage**: Increase this value to speed up processing on multi-core systems.

---

[Back to Top](#)

---

# Contains Text Filter

## Description
The **Contains Text** filter checks whether the filename of the current image contains specific text. This is useful for selectively processing images based on their filenames.

## Properties

### contains_text
- **Description**: A comma-separated list of text strings to search for in the filename.
- **Value Type**: String
- **Usage**: Enter text strings that the filter will search for in the image filenames.

---

[Back to Top](#)

---

# Contour Filter

## Description
The **Contour** filter detects and emphasizes the contours of objects within an image. This effect is useful for artistic rendering and edge detection.

## Properties

### sensitivity
- **Description**: Adjusts the sensitivity of the contour detection.
- **Value Type**: Float
- **Usage**: Higher values increase the contrast of the contours.

### line_thickness
- **Description**: The thickness of the contour lines.
- **Value Type**: Integer
- **Usage**: Increase this value to make the contour lines thicker.

### invert
- **Description**: Specifies whether to invert the contour colors.
- **Value Type**: Boolean
- **Usage**: Set to True to invert the colors of the contours.

### smoothness
- **Description**: Applies Gaussian smoothing to the image before contour detection.
- **Value Type**: Float
- **Usage**: Higher values increase the smoothness, reducing noise in the contours.

### blend_original
- **Description**: Blends the original image with the contour image.
- **Value Type**: Float
- **Usage**: Higher values retain more of the original image in the final result.

### threshold
- **Description**: Applies a threshold to the grayscale image before contour detection.
- **Value Type**: Integer
- **Usage**: Higher values increase the threshold, reducing the amount of detected contours.

### concurrency
- **Description**: Specifies the number of threads used for concurrent processing.
- **Value Type**: Integer
- **Usage**: Increase this value to speed up processing on multi-core systems.

---

[Back to Top](#)

---

# Crystallize Filter

## Description
The **Crystallize** filter transforms an image into a mosaic of crystal-like shapes using K-Means clustering. This effect is useful for creating stylized, abstract versions of images.

## Properties

### crystallize_clusters
- **Description**: The number of crystal shapes to create.
- **Value Type**: Integer
- **Usage**: Higher values create more, smaller crystals.

### criteria_type
- **Description**: The type of criteria used for the K-Means algorithm.
- **Value Type**: String (options: "EPS", "MAX_ITER", "EPS + MAX_ITER")
- **Usage**: Choose the criteria based on the desired convergence method.

### max_iterations
- **Description**: The maximum number of iterations for the K-Means algorithm.
- **Value Type**: Integer
- **Usage**: Higher values allow the algorithm more time to converge.

### epsilon
- **Description**: The convergence threshold for the K-Means algorithm.
- **Value Type**: Float
- **Usage**: Smaller values make the algorithm more precise but slower.

### attempts
- **Description**: The number of attempts the algorithm makes to perform clustering.
- **Value Type**: Integer
- **Usage**: Increase this value for better clustering results.

### color_space
- **Description**: The color space used for the crystallization.
- **Value Type**: String (options: "RGB", "LAB", "HSV")
- **Usage**: Choose the color space based on the desired color manipulation.

### dithering
- **Description**: Specifies whether to apply dithering to the crystallized image.
- **Value Type**: Boolean
- **Usage**: Set to True to apply dithering, which can help to reduce banding in the crystallized image.

### concurrency
- **Description**: Specifies the number of threads used for concurrent processing.
- **Value Type**: Integer
- **Usage**: Increase this value to speed up processing on multi-core systems.

---

[Back to Top](#)

---

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

# Cyberpunk Filter

## Description
The **Cyberpunk** filter applies a stylized, futuristic effect to images using color manipulation, edge enhancement, and glow effects. This effect is inspired by the neon-lit aesthetic of the cyberpunk genre.

## Properties

### shadow_colors
- **Description**: Colors used for shadows in the image.
- **Value Type**: List[Tuple (R, G, B)]
- **Usage**: Define up to two colors to be applied to the shadow areas.

### highlight_colors
- **Description**: Colors used for highlights in the image.
- **Value Type**: List[Tuple (R, G, B)]
- **Usage**: Define up to two colors to be applied to the highlight areas.

### blur_radius
- **Description**: The radius of the Gaussian blur applied to the image.
- **Value Type**: Integer
- **Usage**: Larger values create a stronger glow effect.

### blend_mode
- **Description**: Specifies the blend mode used to combine the layers (e.g., SCREEN, OVERLAY, MULTIPLY).
- **Value Type**: String
- **Usage**: Choose a blend mode to define how the layers are combined.

### opacity
- **Description**: The opacity of the final blended image.
- **Value Type**: Float
- **Usage**: Higher values make the blend more prominent.

### desaturation
- **Description**: Desaturates the image before applying the cyberpunk effect.
- **Value Type**: Float
- **Usage**: Higher values reduce the overall saturation, creating a more subdued effect.

---

[Back to Top](#)

---

# Denoise Filter

## Description
The **Denoise** filter reduces noise in an image while preserving important details. This effect is particularly useful for cleaning up images that have been captured in low light or with high ISO settings.

## Properties

### h
- **Description**: The strength of the denoising for the luminance component.
- **Value Type**: Float
- **Usage**: Higher values result in stronger denoising.

### h_for_color
- **Description**: The strength of the denoising for the color components.
- **Value Type**: Float
- **Usage**: Higher values result in stronger denoising for colors.

### template_window_size
- **Description**: The size of the template window used in denoising.
- **Value Type**: Integer
- **Usage**: Larger values use more pixels to denoise each part of the image.

### search_window_size
- **Description**: The size of the search window used in denoising.
- **Value Type**: Integer
- **Usage**: Larger values allow the algorithm to find more similar patches for denoising.

### color_tint
- **Description**: The color tint applied to the denoised image.
- **Value Type**: Tuple (R, G, B)
- **Usage**: Apply a color tint to adjust the overall hue of the denoised image.

### intensity
- **Description**: The intensity of the denoising effect.
- **Value Type**: Float
- **Usage**: Higher values apply stronger denoising.

---

[Back to Top](#)


# Detail Filter

## Description
The **Detail** filter enhances the fine details in an image. It is useful for bringing out texture and subtle elements that might otherwise be lost.

## Properties

### detail_intensity
- **Description**: The intensity of the detail enhancement.
- **Value Type**: `Float`
- **Usage**: Increase to enhance more details.

### edge_threshold
- **Description**: Sensitivity of edge detection during detail enhancement.
- **Value Type**: `Float`
- **Usage**: Lower values increase sensitivity to edges.

### smoothness
- **Description**: Smoothness of the result, reducing noise while enhancing details.
- **Value Type**: `Float`
- **Usage**: Increase to smooth out the enhanced details.

### contrast_adjustment
- **Description**: Adjustment to the contrast of the enhanced image.
- **Value Type**: `Float`
- **Usage**: Increase to boost contrast in the details.

### color_enhancement
- **Description**: Adjustment to the color saturation of the enhanced image.
- **Value Type**: `Float`
- **Usage**: Increase to enhance color vibrancy in the details.

---

[Back to Top](#)

---

# Diffuse Glow Filter

## Description
The **Diffuse Glow** filter adds a soft, glowing effect to the image, reminiscent of a dreamy or ethereal atmosphere.

## Properties

### glow_intensity
- **Description**: The intensity of the glow effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the glow more prominent.

### blur_radius
- **Description**: The radius of the blur applied to create the glow.
- **Value Type**: `Integer`
- **Usage**: Larger values create a softer, more diffused glow.

### blend_factor
- **Description**: The blending factor between the original image and the glow effect.
- **Value Type**: `Float`
- **Usage**: Higher values blend more of the glow effect into the image.

### tint_color
- **Description**: The color used to tint the glow effect.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set a color to tint the glow.

### inverted_mask
- **Description**: Whether to invert the mask used to create the glow.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the glow effect.

---

[Back to Top](#)

---

# Dotted Halftone Filter

## Description
The **Dotted Halftone** filter creates a halftone effect using dots to represent different shades of gray, giving a retro or print-like appearance.

## Properties

### halftone_block_size
- **Description**: The size of the pixel neighborhood for adaptive thresholding.
- **Value Type**: `Integer`
- **Usage**: Larger values result in larger dots.

### halftone_C_value
- **Description**: The constant subtracted from the mean in adaptive thresholding.
- **Value Type**: `Float`
- **Usage**: Adjust to control the dot intensity.

### halftone_threshold_type
- **Description**: The method used for adaptive thresholding.
- **Value Type**: `String` (options: `"MEAN_C"`, `"GAUSSIAN_C"`)
- **Usage**: Choose the method that gives the desired effect.

### halftone_dot_color
- **Description**: The color of the dots.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the halftone dots.

### halftone_background_color
- **Description**: The background color for the halftone effect.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the background color behind the dots.

### halftone_dot_size
- **Description**: The multiplier for the size of the dots.
- **Value Type**: `Float`
- **Usage**: Increase to make the dots larger.

---

[Back to Top](#)

---

# Edge Enhance Filter

## Description
The **Edge Enhance** filter sharpens the edges within an image, making details more pronounced.

## Properties

### edge_enhance_strength
- **Description**: The strength of the edge enhancement.
- **Value Type**: `Float`
- **Usage**: Increase to make edges more defined.

### edge_enhance_blend
- **Description**: The blending factor between the enhanced edges and the original image.
- **Value Type**: `Float`
- **Usage**: Higher values blend more of the edge enhancement into the image.

### edge_detection_method
- **Description**: The method used for detecting edges.
- **Value Type**: `String`
- **Usage**: Choose the method based on the desired effect.

### edge_sharpening
- **Description**: Whether to apply additional sharpening after edge enhancement.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to apply additional sharpening.

### edge_enhance_type
- **Description**: The type of edge enhancement applied (`EDGE_ENHANCE` or `EDGE_ENHANCE_MORE`).
- **Value Type**: `String`
- **Usage**: Choose the type based on how strong you want the enhancement.

---

[Back to Top](#)

---

# Emboss Filter

## Description
The **Emboss** filter creates a three-dimensional effect that makes the image look as though it has been embossed.

## Properties

### emboss_direction
- **Description**: The direction of the emboss effect.
- **Value Type**: `String`
- **Usage**: Choose the direction of the light source for the emboss.

### emboss_strength
- **Description**: The strength of the emboss effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the emboss more pronounced.

### emboss_blend
- **Description**: The blending factor between the original image and the embossed effect.
- **Value Type**: `Float`
- **Usage**: Higher values blend more of the emboss effect into the image.

### emboss_softness
- **Description**: The smoothness of the emboss effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the emboss softer and less sharp.

### emboss_apply_to_alpha
- **Description**: Whether to apply the emboss effect to the alpha channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to apply embossing to the alpha channel.

---

[Back to Top](#)

---

# Engrave Filter

## Description
The **Engrave** filter simulates the appearance of an engraved image, adding texture and depth.

## Properties

### engrave_blur_radius
- **Description**: The radius of the blur applied to the engraving.
- **Value Type**: `Integer`
- **Usage**: Larger values result in a softer engraving.

### engrave_blur_sigma_x
- **Description**: The horizontal intensity of the blur.
- **Value Type**: `Float`
- **Usage**: Increase for more horizontal blur.

### engrave_blur_sigma_y
- **Description**: The vertical intensity of the blur.
- **Value Type**: `Float`
- **Usage**: Increase for more vertical blur.

### engrave_intensity
- **Description**: The intensity of the engraving effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the engraving deeper and more pronounced.

### engrave_inversion
- **Description**: Whether to invert the grayscale image before engraving.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the image before applying the engraving.

### engrave_color
- **Description**: The color applied to the engraved lines.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the engraved lines.

### engrave_background_color
- **Description**: The background color for the engraving effect.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the background color behind the engraved lines.

---

[Back to Top](#)

---

# Extrude 3D Filter

## Description
The **Extrude 3D** filter creates a three-dimensional extrusion effect, adding depth and shadow to make parts of the image appear raised.

## Properties

### extrude_depth
- **Description**: The depth of the extrusion effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the extrusion deeper.

### extrude_edge_sharpness
- **Description**: The sharpness of the edges of the extrusion.
- **Value Type**: `Float`
- **Usage**: Increase for sharper edges.

### extrude_light_direction
- **Description**: The direction of the light source for the extrusion.
- **Value Type**: `String`
- **Usage**: Choose the direction of the light for the shadow effects.

### extrude_light_intensity
- **Description**: The intensity of the light applied to the extrusion.
- **Value Type**: `Float`
- **Usage**: Increase for stronger light and shadow contrast.

### extrude_colorize
- **Description**: Whether to apply a color tint to the extrusion.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to add a color tint.

### extrude_color_tint
- **Description**: The color tint applied to the extrusion.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color tint for the extrusion.

### extrude_height_map_strength
- **Description**: The strength of the height map used to create the extrusion.
- **Value Type**: `Float`
- **Usage**: Increase to enhance the height map effect.

### extrude_smoothness
- **Description**: The smoothness of the extrusion.
- **Value Type**: `Float`
- **Usage**: Increase to make the extrusion smoother.

### extrude_mode
- **Description**: The direction of the extrusion, either inward or outward.
- **Value Type**: `String` (options: `"Inward"`, `"Outward"`)
- **Usage**: Choose the mode based on the desired effect.

---

[Back to Top](#)

---

# Eye Detection Filter

## Description
The **Eye Detection** filter detects eyes in an image and can optionally draw bounding boxes around them. This is useful for applications that require facial feature detection.

## Properties

### eye_detection_draw_bounding_boxes
- **Description**: Whether to draw bounding boxes around detected eyes.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to draw bounding boxes.

### eye_detection_bounding_box_color
- **Description**: The color of the bounding boxes.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the bounding boxes.

### eye_detection_bounding_box_thickness
- **Description**: The thickness of the bounding boxes.
- **Value Type**: `Integer`
- **Usage**: Increase to make the bounding boxes thicker.

### eye_detection_scale_factor
- **Description**: The scale factor for the eye detection algorithm.
- **Value Type**: `Float`
- **Usage**: Adjust to control how the algorithm scales the image.

### eye_detection_min_neighbors
- **Description**: The minimum number of neighbors each eye should have in order to be retained.
- **Value Type**: `Integer`
- **Usage**: Increase to reduce false positives.

### eye_detection_min_size
- **Description**: The minimum size of eyes to detect.
- **Value Type**: `Tuple (Width, Height)`
- **Usage**: Set the minimum size for detected eyes.

---

[Back to Top](#)

---

# Face Detection Filter

## Description
The **Face Detection** filter detects faces in an image using MTCNN (Multi-task Cascaded Convolutional Networks) and can optionally draw bounding boxes around them.

## Properties

### face_detection_confidence_threshold
- **Description**: The confidence threshold for detecting faces.
- **Value Type**: `Float`
- **Usage**: Set the minimum confidence level for a face to be considered valid.

### face_detection_draw_bounding_boxes
- **Description**: Whether to draw bounding boxes around detected faces.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to draw bounding boxes.

### face_detection_bounding_box_color
- **Description**: The color of the bounding boxes.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the bounding boxes.

### face_detection_box_thickness
- **Description**: The thickness of the bounding boxes.
- **Value Type**: `Integer`
- **Usage**: Increase to make the bounding boxes thicker.

### face_detection_max_faces
- **Description**: The maximum number of faces to detect.
- **Value Type**: `Integer`
- **Usage**: Set a limit on the number of faces to detect.

---

[Back to Top](#)

---

# Find Edges Filter

## Description
The **Find Edges** filter detects and highlights the edges in an image, creating a sharp, defined look.

## Properties

### edge_detection_algorithm
- **Description**: The algorithm used for edge detection.
- **Value Type**: `String` (options: `"FIND_EDGES"`, `"SOBEL"`, `"PREWITT"`)
- **Usage**: Choose the algorithm based on the desired edge effect.

### edge_threshold
- **Description**: The sensitivity threshold for edge detection.
- **Value Type**: `Float`
- **Usage**: Lower values increase edge sensitivity.

### edge_enhancement
- **Description**: Whether to enhance the edges after detection.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to enhance the detected edges.

### edge_smoothness
- **Description**: The smoothness of the edges.
- **Value Type**: `Float`
- **Usage**: Increase to smooth out the edges.

### edge_apply_to_alpha
- **Description**: Whether to apply edge detection to the alpha channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to apply edge detection to the alpha channel.

---

[Back to Top](#)

---

# Fire Filter

## Description
The **Fire** filter applies a fiery effect to an image using color mapping, intensity adjustments, and optional tinting.

## Properties

### fire_colormap_type
- **Description**: The type of colormap used to create the fire effect.
- **Value Type**: `String`
- **Usage**: Choose a colormap type that gives the desired fiery appearance.

### fire_intensity
- **Description**: The intensity of the fire effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the fire effect more prominent.

### fire_contrast
- **Description**: The contrast adjustment applied before the fire effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the fire effect more dramatic.

### fire_brightness
- **Description**: The brightness adjustment applied before the fire effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the fire effect brighter.

### fire_overlay_strength
- **Description**: The strength of the overlay between the original image and the fire effect.
- **Value Type**: `Float`
- **Usage**: Higher values make the fire effect more dominant.

### fire_color_tint
- **Description**: The color tint applied to the fire effect.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color tint for the fire effect.

### fire_invert_colors
- **Description**: Whether to invert the colors of the fire effect.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the colors.

---

[Back to Top](#)

---

# Fisheye Filter

## Description
The **Fisheye** filter simulates a fisheye lens effect, creating a wide-angle distortion that warps the image in a circular manner.

## Properties

### fisheye_intensity
- **Description**: The intensity of the fisheye effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the fisheye effect more pronounced.

### fisheye_lens_distortion
- **Description**: The level of distortion applied to the lens.
- **Value Type**: `Float`
- **Usage**: Increase for more extreme lens distortion.

### fisheye_center_shift_x
- **Description**: The horizontal shift of the fisheye center.
- **Value Type**: `Float`
- **Usage**: Adjust to shift the fisheye effect horizontally.

### fisheye_center_shift_y
- **Description**: The vertical shift of the fisheye center.
- **Value Type**: `Float`
- **Usage**: Adjust to shift the fisheye effect vertically.

### fisheye_edge_behavior
- **Description**: How the edges are handled in the fisheye effect.
- **Value Type**: `String` (options: `"Constant"`, `"Reflect"`)
- **Usage**: Choose how to treat the edges of the fisheye effect.

### fisheye_fov
- **Description**: The field of view for the fisheye effect.
- **Value Type**: `Float`
- **Usage**: Adjust to change the scope of the fisheye distortion.

### fisheye_border_color
- **Description**: The color used for the border of the fisheye effect.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for the borders created by the fisheye distortion.

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

# Frosted Glass Filter

## Description
The **Frosted Glass** filter adds a frosted effect to the image, simulating the appearance of looking through frosted glass.

## Properties

### frost_intensity
- **Description**: The amount of distortion applied to the image.
- **Value Type**: `Integer`
- **Usage**: Increase for more intense frost effect.

### frost_blur_radius
- **Description**: The smoothness of the frost effect.
- **Value Type**: `Float`
- **Usage**: Larger values create a softer frost.

### frost_random_seed
- **Description**: The seed for randomizing the frost effect.
- **Value Type**: `Integer`
- **Usage**: Change to get a different frost pattern.

### frost_tint_color
- **Description**: The tint color applied to the frost effect.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color to tint the frosted effect.

### frost_opacity
- **Description**: The opacity of the frost effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the frost more opaque.

### frost_apply_to_alpha
- **Description**: Whether to apply the frost effect to the alpha channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to apply the frost effect to the alpha channel.

---

[Back to Top](#)

---

# Gaussian Blur Filter

## Description
The **Gaussian Blur** filter softens the image using a Gaussian blur, which is useful for reducing noise or creating a soft focus effect.

## Properties

### gaussian_blur_radius
- **Description**: The radius of the blur.
- **Value Type**: `Integer`
- **Usage**: Increase for a stronger blur.

### gaussian_blur_sigma_x
- **Description**: The standard deviation of the blur in the X direction.
- **Value Type**: `Float`
- **Usage**: Adjust to control the blur's spread horizontally.

### gaussian_blur_sigma_y
- **Description**: The standard deviation of the blur in the Y direction.
- **Value Type**: `Float`
- **Usage**: Adjust to control the blur's spread vertically.

### gaussian_blur_apply_to_alpha
- **Description**: Whether to apply the blur to the alpha channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to blur the alpha channel.

### gaussian_blur_edge_behavior
- **Description**: How the edges are handled during the blur.
- **Value Type**: `String` (options: `"Reflect"`, `"Constant"`)
- **Usage**: Choose the edge handling method.

### gaussian_blur_blend_mode
- **Description**: The blending mode used to control the blur intensity.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the blur into the image.

---

[Back to Top](#)

---

# Gaussian Splatter Filter

## Description
The **Gaussian Splatter** filter applies random splatters of Gaussian blur across the image, creating a chaotic, painterly effect.

## Properties

### splatter_count
- **Description**: The number of splatters applied to the image.
- **Value Type**: `Integer`
- **Usage**: Increase to add more splatters.

### splatter_min_radius
- **Description**: The minimum radius of each splatter.
- **Value Type**: `Integer`
- **Usage**: Set the smallest size for splatters.

### splatter_max_radius
- **Description**: The maximum radius of each splatter.
- **Value Type**: `Integer`
- **Usage**: Set the largest size for splatters.

### splatter_min_blur_strength
- **Description**: The minimum blur strength for each splatter.
- **Value Type**: `Integer`
- **Usage**: Set the weakest blur for splatters.

### splatter_max_blur_strength
- **Description**: The maximum blur strength for each splatter.
- **Value Type**: `Integer`
- **Usage**: Set the strongest blur for splatters.

### splatter_colorize
- **Description**: Whether to colorize the splatters.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to add color to the splatters.

### splatter_color_tint
- **Description**: The color tint applied to the splatters.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color tint for the splatters.

### splatter_random_seed
- **Description**: The seed for randomizing splatter positions and sizes.
- **Value Type**: `Integer`
- **Usage**: Change to get different splatter patterns.

### splatter_randomness
- **Description**: The randomness mode for splatters.
- **Value Type**: `String` (options: `"Consistent"`, `"Dynamic"`)
- **Usage**: Set to `Consistent` for predictable results, `Dynamic` for variability.

---

[Back to Top](#)


---

# Glass Distortion Filter

## Description
The **Glass Distortion** filter applies a distortion effect to the image, simulating the appearance of looking through a distorted glass surface.

## Properties

### glass_distortion_intensity
- **Description**: The intensity of the distortion effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the distortion effect more pronounced.

### glass_distortion_frequency
- **Description**: The frequency of the distortion pattern.
- **Value Type**: `Integer`
- **Usage**: Adjust to control the spacing of distortion waves.

### glass_offset_x
- **Description**: The horizontal offset applied to the distortion.
- **Value Type**: `Float`
- **Usage**: Adjust to shift the distortion horizontally.

### glass_offset_y
- **Description**: The vertical offset applied to the distortion.
- **Value Type**: `Float`
- **Usage**: Adjust to shift the distortion vertically.

### glass_blend_original
- **Description**: The blending ratio of the distorted image with the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### glass_distortion_shape
- **Description**: The shape of the distortion pattern.
- **Value Type**: `String` (options: `"Sine"`, `"Cosine"`, `"Random"`)
- **Usage**: Choose the shape that best suits the desired effect.

### glass_concurrency
- **Description**: The number of threads used for processing the distortion.
- **Value Type**: `Integer`
- **Usage**: Increase to improve processing speed by using more threads.

---

[Back to Top](#)

---

# Glitch Art Filter

## Description
The **Glitch Art** filter applies a glitchy, digital distortion to the image, often used for artistic effects or to simulate digital corruption.

## Properties

### glitch_channel_shift_intensity
- **Description**: The intensity of the color channel shifts.
- **Value Type**: `Integer`
- **Usage**: Increase to create more pronounced channel displacements.

### glitch_number_of_shifts
- **Description**: The number of times the channels are shifted.
- **Value Type**: `Integer`
- **Usage**: Increase to apply more shifts for a more chaotic effect.

### glitch_channel_selection
- **Description**: The color channels affected by the glitch.
- **Value Type**: `String` (options: `"Red"`, `"Green"`, `"Blue"`, `"All"`)
- **Usage**: Choose which channels to apply the glitch effect to.

### glitch_noise_intensity
- **Description**: The intensity of random noise added to the image.
- **Value Type**: `Integer`
- **Usage**: Increase to add more noise.

### glitch_frequency
- **Description**: The frequency of the glitch effect.
- **Value Type**: `Integer`
- **Usage**: Adjust to control how often the glitch occurs.

### glitch_color_inversion
- **Description**: Whether to invert the colors in the image before applying the glitch.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the colors.

### glitch_random_seed
- **Description**: The seed used for randomization.
- **Value Type**: `Integer`
- **Usage**: Set to achieve consistent random results.

---

[Back to Top](#)

---

# Heatmap Filter

## Description
The **Heatmap** filter transforms an image into a heatmap, using color gradients to represent intensity.

## Properties

### heatmap_colormap_type
- **Description**: The type of colormap applied to the image.
- **Value Type**: `String`
- **Usage**: Choose a colormap that best represents the desired intensity gradient.

### heatmap_intensity
- **Description**: The intensity of the heatmap effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the heatmap more vivid.

### heatmap_contrast
- **Description**: The contrast adjustment before applying the heatmap.
- **Value Type**: `Float`
- **Usage**: Increase to enhance the contrast in the heatmap.

### heatmap_brightness
- **Description**: The brightness adjustment before applying the heatmap.
- **Value Type**: `Float`
- **Usage**: Increase to brighten the heatmap effect.

### heatmap_overlay_strength
- **Description**: The strength of the overlay between the heatmap and the original image.
- **Value Type**: `Float`
- **Usage**: Increase to make the heatmap more dominant.

### heatmap_invert_colors
- **Description**: Whether to invert the colors of the heatmap.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the heatmap colors.

### heatmap_smoothing
- **Description**: The amount of smoothing applied to the heatmap.
- **Value Type**: `Float`
- **Usage**: Increase to smooth the heatmap.

---

[Back to Top](#)

---

# High Pass Filter

## Description
The **High Pass** filter highlights high-frequency details in an image, often used to enhance edges and fine details.

## Properties

### high_pass_kernel_size
- **Description**: The size of the kernel used for the high-pass filter.
- **Value Type**: `Integer`
- **Usage**: Increase to apply the filter to a larger area.

### high_pass_kernel_strength
- **Description**: The strength of the kernel, affecting how strongly edges are enhanced.
- **Value Type**: `Float`
- **Usage**: Increase to enhance edges more strongly.

### high_pass_contrast
- **Description**: The contrast adjustment after applying the high-pass filter.
- **Value Type**: `Float`
- **Usage**: Increase to make details more pronounced.

### high_pass_brightness
- **Description**: The brightness adjustment after applying the high-pass filter.
- **Value Type**: `Float`
- **Usage**: Increase to brighten the image after filtering.

### high_pass_blend
- **Description**: The blending ratio between the high-pass filtered image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### high_pass_edge_enhancement
- **Description**: Whether to apply additional edge enhancement.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to enhance edges further.

---

[Back to Top](#)

---

# HSV Filter

## Description
The **HSV** filter manipulates the hue, saturation, and value of an image, providing detailed control over its color properties.

## Properties

### hsv_hue_shift
- **Description**: The amount to shift the hue.
- **Value Type**: `Float`
- **Usage**: Adjust to change the overall color tone.

### hsv_saturation_scale
- **Description**: The scaling factor for saturation.
- **Value Type**: `Float`
- **Usage**: Increase to make colors more vivid.

### hsv_value_scale
- **Description**: The scaling factor for brightness (value).
- **Value Type**: `Float`
- **Usage**: Increase to make the image brighter.

### hsv_hue_rotation
- **Description**: The rotation applied to the hue.
- **Value Type**: `Float`
- **Usage**: Adjust to rotate the hue spectrum.

### hsv_invert_hue
- **Description**: Whether to invert the hue values.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the hue.

### hsv_grayscale
- **Description**: Whether to convert the image to grayscale.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to remove color from the image.

---

[Back to Top](#)

---

# Invert Colors Filter

## Description
The **Invert Colors** filter inverts the colors of the image, creating a photographic negative effect.

## Properties

### invert_red
- **Description**: Whether to invert the red channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the red channel.

### invert_green
- **Description**: Whether to invert the green channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the green channel.

### invert_blue
- **Description**: Whether to invert the blue channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the blue channel.

### invert_alpha
- **Description**: Whether to invert the alpha (transparency) channel.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the alpha channel.

### invert_intensity
- **Description**: The intensity of the inversion effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the inversion effect stronger.

### invert_color_filter
- **Description**: The color filter applied after inversion.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color filter to apply to the inverted image.

### invert_blend_original
- **Description**: The blending ratio between the inverted image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

---

[Back to Top](#)

---

# Laplacian Edge Detection Filter

## Description
The **Laplacian Edge Detection** filter highlights edges in the image, useful for detecting boundaries and contours.

## Properties

### laplacian_kernel_size
- **Description**: The size of the kernel used for the Laplacian filter.
- **Value Type**: `Integer`
- **Usage**: Increase to apply the filter to a larger area.

### laplacian_scale
- **Description**: The scaling factor applied to the filter.
- **Value Type**: `Float`
- **Usage**: Increase to make edges more pronounced.

### laplacian_delta
- **Description**: The delta value added to the results.
- **Value Type**: `Float`
- **Usage**: Adjust to control the baseline intensity of the edge detection.

### laplacian_conversion_to_grayscale
- **Description**: Whether to convert the image to grayscale before applying the filter.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to apply the filter to a grayscale version of the image.

### laplacian_edge_enhancement
- **Description**: Whether to enhance the detected edges.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to enhance edges further.

### laplacian_blending_with_original
- **Description**: The blending ratio between the edge-detected image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

---

[Back to Top](#)

---

# Limit Rows Filter

## Description
The **Limit Rows** filter allows processing only a limited number of rows based on the current image index, useful for batch processing.

## Properties

### limit_rows
- **Description**: The maximum number of rows to process.
- **Value Type**: `Integer`
- **Usage**: Set the limit for the number of rows to process.

---

[Back to Top](#)

---

# Median Blur Filter

## Description
The **Median Blur** filter applies a median blur to the image, useful for reducing noise while preserving edges.

## Properties

### median_blur_radius
- **Description**: The radius of the blur.
- **Value Type**: `Integer`
- **Usage**: Increase for a stronger blur.

### median_preserve_edges
- **Description**: Whether to preserve edges during the blur.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to retain edge details.

### median_color_shift
- **Description**: The amount of color shift applied to the blurred image.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color shift to apply.

### median_blend
- **Description**: The blending ratio between the blurred image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### median_randomize_intensity
- **Description**: Whether to randomize the intensity of the blur.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` for a variable blur intensity.

### median_smoothing
- **Description**: The amount of smoothing applied to the blurred image.
- **Value Type**: `Float`
- **Usage**: Increase to smooth the image further.

---

[Back to Top](#)

---

# Mosaic Filter

## Description
The **Mosaic** filter pixelates the image by resizing it to a smaller resolution and then scaling it back up, creating a mosaic effect.

## Properties

### mosaic_block_size
- **Description**: The size of the blocks in the mosaic.
- **Value Type**: `Integer`
- **Usage**: Increase to make the blocks larger and the mosaic effect more pronounced.

### mosaic_interpolation
- **Description**: The interpolation method used when resizing the image.
- **Value Type**: `String` (e.g., `"INTER_NEAREST"`, `"INTER_LINEAR"`)
- **Usage**: Choose the interpolation method that best suits the desired effect.

### mosaic_blend
- **Description**: The blending ratio between the mosaic image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### mosaic_colorize
- **Description**: Whether to apply a color tint to the mosaic.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to colorize the mosaic.

### mosaic_color_tint
- **Description**: The color tint applied to the mosaic.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color tint for the mosaic.

---

[Back to Top](#)

---

# Motion Blur Filter

## Description
The **Motion Blur** filter simulates the effect of motion by blurring the image in a specific direction.

## Properties

### motion_blur_length
- **Description**: The length of the motion blur.
- **Value Type**: `Integer`
- **Usage**: Increase to make the motion blur longer.

### motion_blur_angle
- **Description**: The angle of the motion blur.
- **Value Type**: `Float`
- **Usage**: Adjust to change the direction of the blur.

### motion_blur_strength
- **Description**: The strength of the motion blur.
- **Value Type**: `Float`
- **Usage**: Increase to make the blur effect stronger.

### motion_blur_blend
- **Description**: The blending ratio between the blurred image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### motion_blur_directional
- **Description**: Whether to apply directional blur.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to apply blur in a specific direction.

### motion_blur_edge_handling
- **Description**: How the edges are handled during the blur.
- **Value Type**: `String` (options: `"Reflect"`, `"Constant"`)
- **Usage**: Choose the edge handling method.

---

[Back to Top](#)

---

# Motion Detection Filter

## Description
The **Motion Detection** filter detects motion in an image by highlighting areas of change.

## Properties

### motion_edge_threshold1
- **Description**: The first threshold for the edge detector.
- **Value Type**: `Integer`
- **Usage**: Increase to detect stronger edges.

### motion_edge_threshold2
- **Description**: The second threshold for the edge detector.
- **Value Type**: `Integer`
- **Usage**: Increase to detect weaker edges.

### motion_smoothing
- **Description**: The amount of smoothing applied to the detected edges.
- **Value Type**: `Float`
- **Usage**: Increase to smooth the edges more.

### motion_invert_mask
- **Description**: Whether to invert the mask of the detected edges.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to invert the edge mask.

### motion_blend_original
- **Description**: The blending ratio between the motion-detected image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### motion_highlight_color
- **Description**: The color used to highlight the detected motion.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color for highlighting motion.

### motion_mask_blur
- **Description**: The amount of blur applied to the motion mask.
- **Value Type**: `Float`
- **Usage**: Increase to soften the motion detection edges.

---

[Back to Top](#)

---

# Negative Filter

## Description
The **Negative** filter inverts the colors of the image, creating a photographic negative effect.

## Properties

### negative_intensity
- **Description**: The intensity of the negative effect.
- **Value Type**: `Float`
- **Usage**: Increase to make the negative effect stronger.

### negative_channel_selection
- **Description**: The color channels affected by the negative effect.
- **Value Type**: `String` (options: `"Red Channel"`, `"Green Channel"`, `"Blue Channel"`, `"All Channels"`)
- **Usage**: Choose which channels to apply the negative effect to.

### negative_blend_with_original
- **Description**: The blending ratio between the negative image and the original.
- **Value Type**: `Float`
- **Usage**: Increase to blend more of the original image into the result.

### negative_invert_grayscale
- **Description**: Whether to convert the image to grayscale before inverting.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to create a grayscale negative.

### negative_brightness_adjustment
- **Description**: The brightness adjustment after inverting the colors.
- **Value Type**: `Float`
- **Usage**: Increase to brighten the image after inversion.

### negative_contrast_adjustment
- **Description**: The contrast adjustment after inverting the colors.
- **Value Type**: `Float`
- **Usage**: Increase to enhance contrast in the negative image.

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

# Object Isolation Filter

## Description
The **Object Isolation** filter isolates detected objects in an image, removing or altering the background.

## Properties

### isolation_confidence_threshold
- **Description**: The confidence threshold for object detection.
- **Value Type**: `Float`
- **Usage**: Increase to isolate only highly confident objects.

### isolation_background_color
- **Description**: The color applied to the background after isolation.
- **Value Type**: `Tuple (R, G, B)`
- **Usage**: Set the color of the background after isolation.

### isolation_include_partial_objects
- **Description**: Whether to include partial objects in the isolation.
- **Value Type**: `Boolean`
- **Usage**: Set to `True` to include objects that are partially within the frame.

### isolation_mask_blur
- **Description**: The amount of blur applied to the isolation mask.
- **Value Type**: `Float`
- **Usage**: Increase to soften the edges of the isolated objects.

### isolation_box_expansion
- **Description**: The amount to expand the bounding boxes of detected objects.
- **Value Type**: `Float`
- **Usage**: Increase to include more of the surrounding area in the isolation.

---

[Back to Top](#)


