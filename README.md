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

# Layout and Spacing

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

5. Don't make things grow/shrink proportionate to each-other (ex: Padding or margin in percentage or em), this won't make sense when things go from desktop size to mobile size.

6. Whenever you’re relying on spacing to connect a group of elements, always make sure there’s more space around the group than there is within it — interfaces that are hard to understand always look worse.

# Designing Text

This text size scheme is recommended by the Refactoring UI.

- 12px
- 14px
- 16px
- 18px
- 20px
- 24px
- 30px
- 36px
- 48px
- 60px
- 72px

* Avoid using em units, as we learned earlier relative size don't grow/shrink as expected.

* Use popular fonts and stic to neutral sans-serif font, ex; Helvetica. (Steal from websites you adore :D)

* Your line-length should be 45-75 chars/line.

* Vertically align-items to bottom when they're text, rather than aligning them in center.

* Line-height and the width of the text-content are directly proportional. Narrower content can use line-height of 1.5 while wider text-content should use 2 line height. For large headlines you can stick to line-height value as 1. (Line-height and font size are inversely proportional)

* If something is longer than 2 or 3 lines, always left align it, rather than center-aligning it.

* If you've a table with numbers, right-align them.

* You can use a tighter letter-spacing for headlines OR increase the letter-spacing for ALL-CAPS headlines or titles or sub-titles. (Tweak around and see if it looks better than before)

# Working with Color

1. Rather than Hex or RGB use HSL (Hue, Saturation, Lightness) color-codes. Because, these values are actually comprehensible compared to the Hex or RGB codes. For ex; three different shades of blue in HSL are HSL(220, 95%, 35%), HSL(220, 69%, 80%), HSL(220, 65%, 61%) - which is evident by the 220 value which is the radial degreee val for the blue color on the [HSL color wheel](https://tsh.io/wp-content/uploads/2019/12/hsl-color-wheel.png).

## How to make your color-pallete

### Greys

Almost anywhere, where there is some user-interaction going on, a grey color-pallete should be used.

> "Text, backgrounds, panels, form controls — almost everything in an interface is grey"

You want 8-10 shades of grey to choose from. Start with a really dark grey and work your way to white incrementally.

### Primary Colors

Your site will need one or two primary colors (used for primary actions, active navigation elements, etc).

Just like with greys, you need a variety (5-10) of lighter and darker shades to choose from.

> Ultra-light shades can be useful as a tinted background for things like alerts, while darker shades work great for text.

### Accent Colors

On top of primary colors, every site needs a few accent colors for communicating different things to the user.

For ex; red for destructive actions, green for positive actions, yellow for warnings, teal for some special tag, etc. All in all, it is not uncommon to have ~10 accent colors on a complex UI.

You'll also need 5-10 shades of each of these colors defined, although make sure to use them very sparingly.

## Define your shades upfront

Define you primary, accent and neutral (Greys) color and shades upfront.

Steps:

1. Choose the base color first. (Prefer a color that would work well as a button background)
   1. Choose the darkest (this should make a good font-color) and the lightest color (this should make a good background color/tint).
   2. Prefer a nine-colors palette, now you have three colors and require 6. Pick a color which is midway of darkest and base and another which is midway of lightest and base. Repeat four more times with the new colors that you just added.
2. In HSL color-scale, increase the saturation as you move further away from 50% lightness.
3. To make a color lighter or darker (rather than just tweaking the lightness param in HSL color), try rotating the hue. To make lighter rotate towards lighter perceived hues (60° - Yellow, 180° - Cyan, 300° - Magenta), and to make it darker rotate towards darked perceived hues (0° - Red, 120° - Green, Blue - 240°). This will vibrantly make your color light/dark. (Refer to a HSL color wheel image to visualize this if it confuses you) Note: As a rule of thumb, don't rotate the hue more than 20-30°.

## Greys don't have to grey

By definition, grey have a saturation of 0, but you don't have to go that way.

You can make your grey color-palette "cool" by saturating it with a bit of blue or "warm" by saturating it with a bit of yellow/orange.

Try doing this, instead of using dull greys and see if it goes with your design.

## Ensuring Accessibility

- Rather than using light color font on dark background (for status of something; ex-Approved, Denied, Awaiting Approval, etc) use dark color font on lighter background. This will not scream for attention ruining the heirarchy of the design.

- For light color secondary font (where the primary font is white) on a darker background, rotate the hue of the secondary text-color to create enough contrast without having to use very close to white color (which is already our primary text and secondary also will look the same in that case).

* Make the UI color-blind friendly adding icons whereever necessary and using constrast of same color instead of diff color in a pie chart. Always be vigilant and lookout for color-blindness failing elements.

### Offset or Inset a button, element or div.

- To offset a button/element/div (make it appear as elevated from the page) add an inset box-shadow to top and a normal box-shadow on bottom.

```CSS
#submit-button {
   color: hsl(225, 80%, 60%);
}

.raise-btn {
   box-shadow: inset 0 1px 0 hsl(224, 84%, 74%);
   box-shadow: 0 1px 3px hsla(0, 0%, 0%, .2);
}

.dug-down-btn {
   box-shadow: inset 0 2px 2px hsl(0, 0, 0, 0.1);
   box-shadow: 0 -2px 0 hsla(0, 0%, 100%, .15);
}
```

Generally, make inputs (textbox, checkbox, radio-btns, etc) as inset and buttons as offset.

### Use shadows to elevate diff elements.

The more the shadow-blur area, the closer the element feels to the user and the more important that element is.

- Lower shadow -> Use for small btns which are not very prominent
- Medium shadow -> Use for the dropdown elements.
- High shadow -> Use for modals which really demand attention.

**Setup an elevation system:**

Predefining a fixed set of shadows will expedite your design workflow.

The book recommend these five (or start with your own min shadow and max shadow and fill in with linearly increasing the area):

1.  box-shadow: 0 1px 3px hsla(0, 0%, .2);
2.  box-shadow: 0 4px 6px hsla(0, 0%, .2);
3.  box-shadow: 0 5px 15px hsla(0, 0%, .2);
4.  box-shadow: 0 10px 24px hsla(0, 0%, .2);
5.  box-shadow: 0 15px 35px hsla(0, 0%, .2);

- Make your divisions span across another divs to create a multi-layered effect. You can do this by either, 1. Making margin negative so that it spills across to other div. 2. Expanding the height more than the parent container.

## Playing with images

- Use a sharp bg images that go with the website color-scheme and mood.
- If you want to add text on image either whiten the image and darken the text or the opposite or "colorize" the image and then add the text.
- Don't scale icons up or down, use specific icons created for specific dimension. Or, if you want to upscale, add a background color to the same size icon.
- For adding a gradient as bg color, use two hues that are no more than 30° apart.

### Don't overlook empty states

- Imagine you've created a contact-book and there are no contacts added by the user, rather than showing empty screen. Add an image and a CTA button that directly lets the user add a contact.
- Don't show filters and search tab and everything unless the content that it is searching is not there at all. For ex; don't show the search notes, and bookmarked notes button if there are currently no notes. Just show one primary button that lets the user create a note first.

### Use fewer borders

When you need to create separation between the two elements, try to resist immediately reaching for the border.

- Rather than using borders to create distinction between two adjacent elements, use diff background-colors to create that distinction.
- Add more than and remove the borders, this will mostly get the elements to feel more distinct.

# Think outside the box

**Dropdowns:** Don't use a simple text-list with box-shadow, maybe use icons multiple columns and little descriptions.
**Tables:** Don't use each column for each data, use some data as subtitle of other column add picture if relevant, introduce some colored-tags from the data. It'd make things more interesting.
**Bullet List (Radio buttons):** If a radio-button selection is important part of the UI you're designing, try something like selectable card instead. Or use some relevant icons as the bullets rather than plain bullets.

> Whenever you stumble across a design you really like, ask yourself:
> “Did the designer do anything here that I never would have thought to do?”
