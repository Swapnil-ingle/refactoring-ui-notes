## refactoring-ui-notes

Started reading refactoring-ui, making notes of important points and solving exercises.

# Starting with Scratch

## Design the feature and not the layout

Your designs should be based on feature-first approach and not on layout.

The author says, build the functional part first and then worry about Navs, and headers, and footers.

## Design in GrayScale

Delegate the color induction part for later time. When you design in gray-scale, you're forced to rely on the highlights, and contrasts and spacing to do all the hard-lifting.

This will make the design sound and you can throw in a bunch of colors later.

## Choose a personality

Choose fonts and colors according to your website's personality.

- For a bank application (or a classic app) a straight edged **serif font** would feel great.
- For a new startup a playful more _rounded_ font (any rounded sans serif) would look nice.
- Or you can use a neutral sans serif font if you want your other element to deliver the personality.

Same goes for color, there are many color psycology on the internet but the author tells that the design boils down to how you _feel_ about the color.

- Blue is safe and familiar
- Gold might say expensive and familiar
- Pink is fun and not so serious

> it can be helpful to think about when you’re trying to understand why you think a color is the right fit.

## Border Radius

- Small: No personality and can blend in anywhere
- Large: Feels more playful
- No Border-Radius: This sounds more serious

> Whatever you choose, it’s important to stay consistent. Mixing square corners with rounded corners in the same interface almost always looks worse than sticking with one or the other.

## Limit your choices

The idea that there are 1000s of fonts and colors to choose from might sound like you have the freedom to choose from whatever you want.

However, this is often a paralysing cause.

When you're designing without constraints the decision-making is torture because there can always be more than one right choice.

### Define systems in advanced

Rather than picking a color at a time when needed, define the color-palette and shades of each color ahead of time.

Similarly, don't tweak the font-size one pixel at a time. Define the type-face and font-colors ahead of time, and stick to it.

Ensure you have a system designed for:

- Font size
- Font weight
- Line height
- Color
- Margin
- Padding
- Width
- Height
- Box shadows
- Border radius
- Border width
- Opacity

…and anything else you run into where it feels like you’re laboring over a lowlevel design decision.

# Hierarchy is everything

## Not all elements are equal

Know how to create hierarchies in components (notes below) and this will improve the design of your site.

When there are countless items screaming for attention it is more chaotic and confusing and less appealing.

### Size isn't everything

Rather than depending upon the text-size to steer the hierarchy (Using bigger font for main-heading and smaller for less and less important stuff) use the following factors to create a much better hierarchy.

1. Make the primary element bolder, rather than making them of bigger font.
2. Rather than making seconday elements smaller in font, use a softer font-color to create the hierarchy. You can use more lighter font-color to tertiary text.

#### Try to stick to two or three colors

##### Color palette setup

1. A dark color for primary content (like headline)
2. A grey color for secondary content (like for the date published)
3. A lighter grey color for tertiary content (Like for footer)

##### Text Font Setup

1. For primary use 600-700
2. For secondary use 400-500

This should be it, for anything tertiary use lighter color rather than smaller font size.

Don't use grey text on colored background, this will look dull and give it an "inactive" sense. Use a color of same hue and change the saturation until satisfied (No science behind this).

- Instead of presenting the data from DB in name: value format represent it as plain data. This will open the doors to define hierarchy between the items in constrast to _name: value_ format which entails every field has the same importance.

#### Button styling

If there are multiple buttons on one page, don't style all the buttons same.

Only the primary action button of that page should be bold or have high-contrast background, the secondary and tertiary should be different.

- Primary Button: Bold or high-contrast background
- Secondary Button: Soft-contrast or outlined styled
- Tertiary Button: Just a colored text with the link to tertiary action page or pop-up modal.

### Layout and Spacing

1. Start with too much white space. Rather than adding white-space until it feels enough, add too much of it and _remove_ until it feels enough.
2. Establish spacing and sizing system. Limit yourself to a constrainted set of spacing/sizing values defined in advance.

Spacing System as suggested by the book, use the following template of pre-defined values for defining any space in your UI. (These are multiple of 16 and that is why they are consistent, if one value is too small pick next one and so on)

- 4px
- 8px
- 12px
- 16px
- 24px
- 32px
- 48px
- 64px
- 96px
- 128px
- 192px
- 256px
- 384px
- 512px
- 640px
- 768px

3. Design the mobile layout first (On ~400px canvas), as the contraints are real. Once the mobile version is ready, bring it to desktop width and resize whatever was a compromise due to mobile screen limit.

4. Think in terms of columns. If you bring something from mobile-view to desktop-view and that element is taking too much size think how you can refactor it into multiple columns.
