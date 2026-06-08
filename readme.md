# Style Guide

Megan Lavengood, June 2026 - [megan@meganlavengood.com](mailto:megan@meganlavengood.com?subject=Stingers%20website%20help)

Now that the website has been updated, please take care when editing pages to keep the style unified. I have also written some help guidelines for how to perform other common updates.

Jump to:

- [Adding new content](#adding-new-content)
  - [Formatting text in the text editor](#formatting-text-in-the-text-editor)
  - [Pasting content written somewhere else](#pasting-content-written-somewhere-else)
  - [More formatting rules](#more-formatting-rules)
  - [Creating a new page](#creating-a-new-page)
- [Color palette](#color-palette)
- [Slideshows](#slideshows)
- [Editing the navigation menu](#editing-the-navigation-menu)
- [Command buttons](#command-buttons)
- [Partners and Sponsors](#partners-and-sponsors)
- [Team logo](#team-logo)
- [Contact Us (pool addresses)](#contact-us-pool-addresses)
- [Text section width](#text-section-width)
- [Adding images to pages](#adding-images-to-pages)
  - [In the text editor](#in-the-text-editor)
  - [Generic Photo](#generic-photo)
- [Alert text (yellow background)](#alert-text-yellow-background)
- [News and newsletters](#news-and-newsletters)

## Adding new content

To maintain accessibility and cohesive style, follow these rules when adding content to the website.

### Formatting text in the text editor

The styles for the website have been built into the stylesheet for each page. This ensures that each page has a coherent look. While many options are available in the text editor for changing font, etc., **you should only use the following formatting options in the text editor:**

- Heading dropdown menu (select Paragraph or a Heading level)
- Bold or italic (no underline)
- Lists (ordered or unordered)
- Text align center or left

**Do _not_ use the font or size dropdowns. Changing the color of the text is also not recommended.**

### Pasting content written somewhere else

A lot of formatting issues ("I added content and it looks bad and doesn't match the rest of the website!"-type issues) come from copy-pasting text from other sources (an email, a word document, another website, etc.), because the formatting of that website/whatever gets pasted along with the text.

**To keep the website coherent, it's crucial to only paste unformatted (plain) text.**

    - One good way to remove formatting is to open up a plain-text document in Text Editor (or whatever PC equivalent) and paste it there first.
    - Again, do not paste directly from another source (an email, a word document, another website, etc.) into the webiste, as this will paste formatting as well.
    - If you *do* paste from another source, there is a specific button you can press in the text editor to paste plain text only. The icon looks like a clipboard with a capital T. Click this instead of pressing ctrl+V.

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

Some of these items are for accessibility reasons; others are simply for coherent style. More information about accessibility and and why this matters can be found on the page [Writing for Web Accessibility from W3C](https://www.w3.org/WAI/tips/writing/). Designing for accessibility is crucial for disabled readers and also improves the content for everyone.

### Creating a new page

If you need to make a new page, not just edit an existing page, you'll have to do a couple additional things to ensure it matches the other pages on the website.

First, when editing the page, click the **<&nbsp;>&nbsp;Source…** button, which opens the **HTML** tab. Copy-paste the following to create a basic template:

```
<div class="max-w-600">
    <h1>Page Title</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipiscing elit.</p>
</div>
```

Don't hit update yet! Instead, click over to the Stylesheet tab and paste the stylesheet text. [You can get the stylesheet text here](https://github.com/meganlavengood/Stingers/blob/main/stylesheet.css). If that link doesn't work, email Megan <megan@meganlavengood.com>, or copy it from another page on this website.

## Color palette

When choosing a custom color, using one of these will help the page look unified.

- <span style="color:#01519b;">■</span> `#01519b` (this is the "cold blue" color variant selected with the theme)
- <span style="color:#e08e45;">■</span> `#e08e45`
- <span style="color:#12664f;">■</span> `#12664f`
- <span style="color:#39a2ae;">■</span> `#39a2ae`
- <span style="color:#333;">■</span> `#333` (a softer black looks nicer on white than true black)
- □ `#fff`

## Slideshows

- A slideshow is implemented on the front page. The slideshow does not currently switch between slides automatically, since its purpose is just aesthetic.
- To edit each slide to add a tint or text, edit the individual slide (not the entire slideshow).
    - Photos can have a tint, which can give a different look and improve the legibility of a text overlay. Black and white are common choices for a tint. Make sure to turn down the transparency of the color overlay—50% or lower is usually best.
    - Slideshows can have text overlays! This is nice for the front page.
    - The text can also have its own background color to improve legibility, but this looks a little clunkier than having a tint for the whole photo.

## Editing the navigation menu

- Try not to add new first-level menu items, as the menu is already quite long. Ideally the menu will not extend to a second line.
- If you add a new second-level menu item, make sure to also add the new link to the parent page, as these are not automatically synced.
- You can hide certain links from public view (i.e., require a login to see the menu item) by clicking the pencil icon and selecting "authenticated" from the dropdown menu.

## Command buttons

This component is featured on several pages.

- **Button groups:** I've defined many button groups. This is a nice way to make sure information is accesssible from lots of places on the website. Feel free to reuse button groups if the related pages are the same in multiple places.
- **Button color**: it's fine to just use all the default color. For more visual interest, use the colors listed [above](#color-palette) if you want a different color for a button.
- **Icons**: You can select an icon that helps communicate the destination of the button visually. Only use icons if you can find an appropriate icon for each button—it looks confusing to only have an icon on some of the buttons. Only use the default icons—don't upload your own.

## Partners and Sponsors

To add sponsors, add their logo as well as a link to their website ("on click link to:"). Make sure to select "Open link in new window."

## Team logo

- Use logos with a transparent background (.png format).
- The main logo doesn't resize well, so upload the logo with the actual dimensions you want to use. I used 300x206.
- The mobile logo should be white instead of blue, because it gets printed on a blue background with the mobile header.
- Make sure to select "on click link to:" and link to the home page. Being able to click the logo to go to the home page is a common expectation for users. Open link in same window.

## Contact Us (pool addresses)

The "Contact Us" component is used to display pool information.

- Toggle off any fields that have no content (currently "hours" is toggled off, because the pool hours are too variable for us to keep up with).
- Unlike some of the other components, there's no way to display different Contact Us info on different pages, so any changes you make on this component will occur anywhere the Contact Us component is used.
- I know the black text on blue background is too low-contrast and hard to read. Unfortunately this isn't changeable on our end. Hopefully GoMotion will update this someday (but I kinda doubt it!). I think the component is still useful despite this.

## Text section width

The GoMotion app's default is to have all text sections be full-width. But it's easier to read text that has narrower margins. I've made it so each page's text has a maximum width of 600 pixels. This involves directly editing the HTML but it's relatively simple to do:

1. When editing a custom page (or generic text), click the **<&nbsp;>&nbsp;Source…** button.
2. Before your text, e.g., on line 1, add `<div class="max-w-600">`.
3. After all your text (e.g., on the very last line of the page), add `</div>`.

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
3. Give appropriate sizes for each **display size**. I suggest a width of 750px for desktop and tablet, and 300px for mobile, `with` whatever height is automatically calculated from there.
4. Add a descriptive alt text that explains what's in the photo. The description should be brief. Do not begin with generic words like "photo of" or "image of"—just describe the content.
5. Select **center** under **Horizontal alignment** (unless of course you want it aligned left or right for some reason!).

## Alert text (yellow background)

Alert text can be used to highlight deadlines—for example, on the Team Store pages or on the Registration page.

Creating the alert text requires some HTML editing. To add an alert text box, edit the page, click the **<&nbsp;>&nbsp;Source…** button, and paste the following wherever you want the alert to appear (substituting your text for `ALERT TEXT HERE`)—

```
<div class="alert">
<p>ALERT TEXT HERE</p>
</div>
```

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
