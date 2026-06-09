# Style Guide

Megan Lavengood, June 2026 - [megan@meganlavengood.com](mailto:megan@meganlavengood.com?subject=Stingers%20website%20help)

Now that the website has been updated, please take care when editing pages to keep the style unified. I have also written some help guidelines for how to perform other common updates.

Jump to:

- [Adding new text to pages](#adding-new-text-to-pages)
    - [Formatting text in the text editor](#formatting-text-in-the-text-editor)
    - [Pasting content written somewhere else](#pasting-content-written-somewhere-else)
    - [More formatting rules](#more-formatting-rules)
    - [Alert text (yellow background)](#alert-text-yellow-background)
    - [Text section width](#text-section-width)
    - [Tables](#tables)
- [Creating a new page (not just adding text)](#creating-a-new-page-not-just-adding-text)
- [Uploading PDFs or other documents](#uploading-pdfs-or-other-documents)
- [Color palette](#color-palette)
- [Components](#components)
    - [Slideshows](#slideshows)
    - [Slide text](#slide-text)
        - [Photo tint](#photo-tint)
    - [Navigation menu](#navigation-menu)
    - [Command buttons](#command-buttons)
    - [Partners and Sponsors](#partners-and-sponsors)
    - [Team logo](#team-logo)
    - [Contact Us (pool addresses)](#contact-us-pool-addresses)
    - [Adding components](#adding-components)
- [Adding images to pages](#adding-images-to-pages)
    - [In the text editor](#in-the-text-editor)
    - [Generic Photo](#generic-photo)
- [News and newsletters](#news-and-newsletters)

## Adding new text to pages

To maintain accessibility and cohesive style, follow these rules when adding content to the website.

### Formatting text in the text editor

> [!CAUTION]
> Do _not_ use the font or size dropdowns. Changing the color of the text is also not recommended.

The styles for the website have been built into the stylesheet for each page. This ensures that each page has a coherent look. While many options are available in the text editor for changing font, etc., **you should only use the following formatting options in the text editor:**

- Heading dropdown menu (select Paragraph or a Heading level)
- Bold or italic (no underline)
- Lists (ordered or unordered)
- Text align center or left

![buttons you should use, and buttons you shouldn't](/screenshots/text-editor.png)

### Pasting content written somewhere else

> [!NOTE]
> To keep the website coherent, it's crucial to only paste unformatted (plain) text.

A lot of formatting issues ("I added content and it looks bad and doesn't match the rest of the website!"-type issues) come from copy-pasting text from other sources (an email, a word document, another website, etc.), because the formatting of that website/whatever gets pasted along with the text.

- One good way to remove formatting is to open up a plain-text document in Text Editor (or whatever PC equivalent) and paste it there first.
- Again, do not paste directly from another source (an email, a word document, another website, etc.) into the webiste, as this will paste formatting as well.
- If you _do_ paste from another source, there is a specific button you can press in the text editor to paste plain text only. The icon looks like a clipboard with a capital T. Click this instead of pressing ctrl+V.

![the Paste as Plain Text button](/screenshots/paste.png)

### More formatting rules

- **Use headings, and use them thoughtfully.** 
    - Every page should begin with a **Header 1** that says the title of the page. Surprisingly, the app does not create this for you! You have to add it yourself.
    - Break the page up by using headings to show important sections of the page. The headings in your document should group related paragraphs into sections (**Header 2** level) and subsections (**Header 3** level). The structure of the headings should create a coherent outline of the document/webpage.
    - **Do not use bold, italics, extra line breaks, etc. to show document headings.** This formatting happens automatically when you select a Heading.
    - Do not end headings with a colon.
- **All links should have helpful and descriptive link text.** Your link text should explain where the link is going to take the user. For example: "View our team store"---the link text ("team store") tells the user that the link will take them to the team store. 
    - Do not use generic language like "click here". Each link text should be unique and descriptive.
    - Do not put raw URLs into the text.
- **Use list formatting as appropriate.** Use ordered list when presenting information that is also ordered (e.g., a sequence of steps to take) and an unordered list when the order is not relevant (e.g., a list of helpful resources). Lists are easier for readers to scan and parse quickly when compared to paragraphs.
    - Do not manually type numbers to create an ordered list—use an ordered list format.
    - Do not use tabs or tables to create a list.

![use of HTML elements: heading, unordered list, div](/screenshots/html1.png)

Some of these items are for accessibility reasons; others are simply for coherent style. More information about accessibility and and why this matters can be found on the page [Writing for Web Accessibility from W3C](https://www.w3.org/WAI/tips/writing/). Designing for accessibility is crucial for disabled readers and also improves the content for everyone.

### Alert text (yellow background)

![an Alert text box, and the Div button](/screenshots/div1.png)

Alert text can be used to highlight deadlines—for example, on the Team Store pages or on the Registration page.

To create an alert text box:

1. On the text editor, click the Div button.
2. In the popup box, under **General**, in **stylesheet classes**, type `alert`.
3. Click OK and you will see the alert text box in the text editor with all styles applied.

![the options when creating a Div](/screenshots/div2.png)

### Text section width

The GoMotion app's default is to have all text sections be full-width. But it's easier to read text that has narrower margins. I've made it so each page's text has a maximum width of 600 pixels. This involves directly editing the HTML but it's relatively simple to do:

1. When editing a custom page (or generic text), click the **<&nbsp;>&nbsp;Source…** button.
2. Before your text, e.g., on line 1, add `<div class="max-w-600">`.
3. After all your text (e.g., on the very last line of the page), add `</div>`.

If this is too complicated, you can also do it similarly to how the Alert text box is created. Highlight all text to keep in the div, and follow the [instructions for the alert text box](#alert-text-yellow-background), but instead of `alert`, type `max-w-600`.

### Tables

If you create a new table:

- Clear the values for
    - Border size
    - Width
    - Height
    - Cell spacing
    - Cell padding
- From the dropdown, select the header row/column that suits your needs. Don't create a table without any header.

![settings on a table](/screenshots/table1.png)

- To prevent weird text wrapping on small devices:
    - Go to the **Advanced** tab
    - Under **Stylesheet classes**, enter `nowrap`.
    - click OK.

![adding a class to a table](/screenshots/table2.png)

## Creating a new page (not just adding text)

If you need to make a new page, not just edit an existing page, you'll have to do a couple additional things to ensure it matches the other pages on the website.

First, when editing the page, click the **<&nbsp;>&nbsp;Source…** button, which opens the **HTML** tab. Copy-paste the following to create a basic template:

```
<div class="max-w-600">
    <h1>Page Title</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipiscing elit.</p>
</div>
```

**Don't hit update yet!** Click over to the Stylesheet tab and paste the stylesheet text. [You can copy the stylesheet text here](https://github.com/meganlavengood/Stingers/blob/main/stylesheet.css). If that link doesn't work, email Megan <megan@meganlavengood.com>.

## Uploading PDFs or other documents

Navigate to the [Documents page](https://www.gomotionapp.com/team/reccobcs/page/documents) to upload documents. Follow the instructions there.

## Color palette

When choosing a custom color, using one of these will help the page look unified.

- ![#01519b](https://img.shields.io/badge/____-01519b?style=flat-square) `#01519b` (this is the "cold blue" color variant selected with the theme)
- ![#e08e45](https://img.shields.io/badge/____-e08e45?style=flat-square) `#e08e45`
- ![#12664f](https://img.shields.io/badge/____-12664f?style=flat-square) `#12664f`
- ![#39a2ae](https://img.shields.io/badge/____-39a2ae?style=flat-square) `#39a2ae`
- ![#333](https://img.shields.io/badge/____-333?style=flat-square) `#333` (a softer black looks nicer on white than true black)
- ![#fff](https://img.shields.io/badge/____-fff?style=flat-square) `#fff`

## Components

### Slideshows

On the front page:

- A slideshow is implemented on the front page. The slideshow does not currently switch between slides automatically, since its purpose is just aesthetic.
- To edit each slide to add a tint or text, edit the individual slide (not the entire slideshow). Edit a slide by clicking "edit slideshow" and then clicking on the slide you'd like to edit. (there's no obvious menu or icon for this—just click the slide.)

Elsewhere:

- If you are uploading a new batch of photos, make a new Slider Group for those photos.
- For each photo, the default settings are mainly okay, but if you can, add alt text for each photo.

### Slide text

![The interface for adding text and text background](/screenshots/slide-textbg.png)

Slideshows can have text overlays! This is nice for the front page.

The text can also have its own background color to improve legibility, but this looks a little clunkier than having a tint for the whole photo.

#### Photo tint

![The interface for adding a photo tint](/screenshots/slide-tint.png)

Photos can have a tint, which can give a different look and improve the legibility of a text overlay. Black and white are common choices for a tint. Make sure to turn down the transparency of the color overlay—50% or lower is usually best.

### Navigation menu

The app calls nav menu items "tabs".

- Try not to add new first-level menu items, as the menu is already quite long. Ideally the menu will not extend to a second line.
- If you add a new second-level menu item, make sure to also add the new link to the parent page, as these are not automatically synced.
- You can hide certain links from public view (i.e., require a login to see the menu item) by clicking the pencil icon and selecting "authenticated" from the dropdown menu.

![Authentication option in the nav menu](/screenshots/auth2.png)

### Command buttons

This component is featured on several pages.

- **Button groups:** These are super useful for repeating links across pages. I'm using them as sort of sub-menus that list groups of related pages. I've defined many button groups and reused them in several places (e.g., the "summer season" button group is on all the pages under "summer season" on the nav menu). This is a nice way to make sure information is accesssible from lots of places on the website, **and if you update a link there, it will update everywhere that button group appears**. Use this feature!
- **Button color**: it's fine to just use all the default color. For more visual interest, use the colors listed [above](#color-palette) if you want a different color for a button.
- **Icons**: You can select an icon that helps communicate the destination of the button visually. Only use icons if you can find an appropriate icon for each button—it looks confusing to only have an icon on some of the buttons. Only use the default icons—don't upload your own.

### Partners and Sponsors

- To add sponsors, add their logo. Square images work best.
- Link to their website ("on click link to:"). Make sure to select "Open link in new window."

### Team logo

- Use logos with a transparent background (.png format).
- The main logo doesn't resize well, so upload the logo with the actual dimensions you want to use. I used 300x206.
- The mobile logo should be white instead of blue, because it gets printed on a blue background with the mobile header.
- Make sure to select "on click link to:" and link to the home page. Being able to click the logo to go to the home page is a common expectation for users. Open link in same window.

### Contact Us (pool addresses)

The "Contact Us" component is used to display pool information.

- Toggle off any fields that have no content (currently "hours" is toggled off, because the pool hours are too variable for us to keep up with).
- Unlike some of the other components, there's no way to display different Contact Us info on different pages, so any changes you make on this component will occur anywhere the Contact Us component is used.
- I know the black text on blue background is too low-contrast and hard to read. Unfortunately this isn't changeable on our end. Hopefully GoMotion will update this someday (but I kinda doubt it!). I think the component is still useful despite this.

### Adding components

To add a component to a page:

- Hover over the left corner of the top of the page, under the navigation menu, and you should see a blue button appear that says **Layout Section.** Click the settings wheel next to the button.
- A map of the current components will appear. Underneath that, click **+ Select component(s) to add.**

![adding a component step 1](/screenshots/component-add1.png)
![adding a component step 2](/screenshots/component-add2.png)

## Adding images to pages

There are two ways of adding images to a page: with the text editor and with the Generic Photo component.

### In the text editor

1. Click the button with the photo icon.
2. Go to the **Upload** tab.
3. Click **Choose file** and browse to and select your photo.
4. When you return to the previous screen, click **Send it to the server.**
5. This should take you back to the **Image info** tab.
6. Add a descriptive alt text that explains what's in the photo. The description should be brief. Do not begin with generic words like "photo of" or "image of"—just describe the content.
7. Give the photo a width. I suggest 700px. The height should be auto-calculated and automatically filled in based on the width. Leave everything else blank.
8. Click OK.
9. In the text editor, put the cursor on the same line as the image, and then click the center align icon to center the photo (unless of course you want it oriented left or right for some reason!).

### Generic Photo

1. Upload the photo.
2. Under **Display mode**, toggle **Absolute.**
3. Give appropriate sizes for each **display size**. I suggest a width of 750px for desktop and tablet, and 300px for mobile, with whatever height is automatically calculated from there.
4. Add a descriptive alt text that explains what's in the photo. The description should be brief. Do not begin with generic words like "photo of" or "image of"—just describe the content.
5. Select **center** under **Horizontal alignment** (unless of course you want it aligned left or right for some reason!).

## News and newsletters

The News section of the website is not edited directly; its content is populated from the News tool, under Org Tools. Use it for posting the Newsletters to the website and any other coummunication you'd like featured there.

1. On the Admin interface (back office), hover over **Org tools** and select **News** (under Communication, right before Message Center).
2. Click **Add news**.
3. Add a title (e.g., **Week 3 Newsletter**).
4. Add the current date for the news date.
5. Add a news expiration date for when you'd like the news to no longer be available on the front page (I've been selecting Sept 1 for summer newsletters).
6. Make sure **show on homepage** is toggled on.
7. Add the newsletter content under **News Content**, being sure to follow the same [formatting rules as given above](#adding-new-content).
8. Click **Send News Emails** so that the newsletter is also emailed to everyone.
9. Click **Create**.

---

**Questions?** Email <megan@meganlavengood.com> if you need more help or have suggestions on how to update this page.
