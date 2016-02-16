**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

## Importing Fonts

### What is a Font?

Fonts in modern operating systems are created as scalable vector graphics. They are stored as a collection of curves (usually one for each character), which are independent of the screen resolution, and stored in standardized file formats, such as TTF (TrueType) or OTF (OpenType).

Rendering such fonts to bitmaps is a complex process, which employs different methods to convert curves to pixels depending on context and target size. Due to this, this rendering process must be done by using the CPU. 
Game engines use the GPU to render, and 3D APIs don't really support the means to do this efficiently, so fonts have to be converted to a format that is friendly to the GPU when imported to a project.

### Converting Fonts

This conversion process consists of rendering a vector font to a given point size and storing all the resulting characters in a bitmap texture. The bitmap texture is then used by the GPU to draw a small quad for each character and form readable strings.

<p align="center"><img src="images/bitmapfont.png"></p>

The drawback of this process is that fonts must be pre-imported in the specific sizes that they will use in the project. However, given that that bitmap fonts compress really well, this is not as bad as it sounds.

### Importing a Font

Fonts are imported via the Font import dialog. The dialog will ask for a font, a size, some options and a target resource fie to save.

<p align="center"><img src="images/fontimport.png"></p>

The dialog is fully dynamic, which means that any change will be reflected in the font preview window. The user ccan tweak almost every parameter and get instant feedback on how the font will look.

Since the resulting font is a bitmap, a few more options were added to make the imported font look even nicer. These options were added to please graphic designers, who love putting gradients, outlines and shadows in fonts, as well as changing all the inter-spaces available :). The options which will be explained as follows.

#### Extra Spacing

It is possible to add more space for:
*  Characters, the space between them can be varied.
*  "space" character, so the distance between words is bigger.
*  Top and Bottom margins, this changes the spacing between lines as well as the space between the top and bottom lines and the borders.

<p align="center"><img src="images/fontspacing.png"></p>

#### Shadows & Outline

Fonts can be added a shadow. For this, the font is drawn again below on a different color and the blurred with a gaussian kernel of different sizes. The resulting shadow can be adjusted with an exponential function to make it softer or more like an outline. A second shadow is also provided to create some added effects, like a bump or outline+shadow.

<p align="center"><img src="images/shadowoutline.png"></p>

#### Gradients

Gradients are also another of the visual effects that graphic designers often use. To show how much we love them, we added those too. Gradients can be provided as a simple curve between two colors, or a special png file with a hand drawn gradient.

<p align="center"><img src="images/fontgradients.png"></p>
 
#### Internationalization

Colors, shadows and gradients are beautiful, but it's time we get to serious business. Developing games for Asian markets is a common practice in today's globalized world and app stores. 

Here's when things get tricky with using bitmap fonts. Asian alphabets (Chinese, Japanese and Korean) contains dozens of thousands of characters. Generating bitmap fonts with every single of them is pretty expensive, as the resulting textures are huge. If the font size is small enough, it can be done without much trouble, but when the fonts become bigger, we run out of video ram pretty quickly!

To solve this, Godot allows the user to specify a text file (in UTF-8 format) where it expects to find all the characters that will be used in the project. This seems difficult to provide at first, and more to keep up to date, but it becomes rather easy when one realizes that the .csv with the translations can be used as such source file (see the [Importing Translations](import_translations) section). As Godot re-imports assets when their dependencies change, both the translation and font files will be updated and re-imported automatically if the translation csv changes. 

Another cool trick for using a text file as limit of which characters can be imported is when using really large fonts. For example, the user might want to use a super large font, but only to show numbers. For this, he or she writes a numbers.txt file that contains "1234567890", and Godot will only limit itself to import data, thus saving a lot of video memory.


 --- //[Juan Linietsky](reduzio@gmail.com) 2013/11/10 18:12//


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
