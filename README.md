CSS — Explained One by One* (Universal selector)Applies to every element on the page.
box-sizing: border-box — Makes width/height include padding and borders so layout math is simpler.
margin: 0 and padding: 0 — Removes the default spacing browsers add, so you control spacing yourself.
bodyThe main page container.
font-family — Sets the default font for the whole site.
background — Soft cream color for the page background.
color — Dark brown text color.
line-height: 1.6 — Makes text more readable by adding space between lines.
navThe top navigation bar.
padding: 18px 8% — Space inside the bar (18px top/bottom, 8% of the screen width left/right).
display: flex — Turns the nav into a flexible row so items can be positioned easily.
justify-content: space-between — Pushes the logo to the left and the links to the right.
align-items: center — Vertically centers everything in the bar.
background + color — Dark background with white/light text.
position: sticky + top: 0 — Keeps the nav stuck at the top when you scroll.
z-index: 100 — Makes sure the nav stays above other content.
nav h1The “MAISONÉ” logo text.
Uses a serif font (Georgia) so it looks more elegant.
letter-spacing: 4px — Spreads the letters out a bit.
font-size and font-weight: normal — Controls size and keeps it from being bold.
nav aThe navigation links (Home, Houses, About).
color — Light color so they show on the dark bar.
text-decoration: none — Removes the default underline.
margin-left: 28px — Spaces the links apart.
transition: color 0.2s — Makes the color change smoothly when you hover.
nav a:hoverWhat happens when the mouse is over a link.
Changes the text color to gold.
.heroThe big top section with the background image.
height: 520px — Makes the section tall.
background — Puts a dark gradient over the Unsplash image so white text is readable.
background-size: cover — Makes the image fill the whole area without empty space.
background-position: center — Centers the image.
display: flex + centering properties — Places the text and button in the middle of the section.
color: #fff — White text.
padding — Small space around the content.
.hero h2The main headline (“Find Your Escape.”).
Serif font, large size that scales with the screen (clamp), normal weight, slight letter spacing.
.hero pThe short line under the headline.
Slightly larger text, a bit transparent (opacity: 0.9), and space below it.
.hero buttonThe “EXPLORE HOMES” button.
Gold background, dark text, padding, letter spacing.
transition — Smoothly changes color and position on hover.
On hover it lightens and moves up slightly (translateY(-2px)).
.housesThe whole “Discover Our Homes” section.
padding: 70px 8% — Large space around the content.
.houses h2The section title.
Centered, serif font, clear size, normal weight.
.houses .subtitleThe smaller line under the title.
Centered, muted color, space below it.
.house-listThe container that holds all the house cards.
display: flex — Lays cards out in a row.
flex-wrap: wrap — Lets cards drop to the next line on smaller screens.
gap: 28px — Space between cards.
justify-content: center — Centers the group of cards.
.houseOne individual house card.
White background, fixed width, soft shadow.
transition — Smoothly animates the lift and shadow.
On hover it rises a little and the shadow gets stronger.
.house imgThe photo on each card.
Full width of the card, fixed height, object-fit: cover so the image crops nicely instead of stretching.
display: block — Removes a tiny gap that can appear under images.
.house-infoThe text area under the photo.
Adds padding so the text isn’t stuck to the edges.
.house h3House name.
Serif font, comfortable size, normal weight.
.house .locationCity and country line.
Smaller gold text.
.house .detailsFeature line (pool, bedrooms, etc.).
Muted gray color.
.house .descShort description paragraph.
Slightly muted color and comfortable line height.
.house .priceThe price.
Gold, bold, with space before the button.
.house button“View House” button.
Full width of the card, dark background, white text.
Changes to a softer brown on hover.
.aboutThe “A Different Kind of Stay” section.
Soft beige background, centered text, large padding.
.about h2Section title — serif, normal weight..about pParagraphs of text.
Limited max width so lines don’t get too long, centered, muted color.
footerBottom of the page.
Dark background, light text, centered, padding.
footer h2Logo text in the footer — serif with letter spacing.footer pTagline and copyright — smaller and slightly faded.@media (max-width: 640px)Only applies on small screens (phones).
Nav stacks vertically and tightens spacing.
Links get closer and a bit smaller.
Hero becomes shorter.
House cards stretch to full width (with a max).
Section padding is reduced so content fits better.
JavaScript — More DetailedThere are only two functions. Both are simple and written for a student demo.1. showHouses()JavaScriptfunction showHouses() {
    document.getElementById("houses").scrollIntoView({
        behavior: "smooth"
    });
}What it does:
document.getElementById("houses") finds the section that has id="houses" (the house cards area).
.scrollIntoView(...) tells the browser to scroll that section into view.
{ behavior: "smooth" } makes the scroll animated instead of jumping instantly.
When it runs:

When someone clicks the “EXPLORE HOMES” button in the hero (because of onclick="showHouses()").2. viewHouse(name, location, price)JavaScriptfunction viewHouse(name, location, price) {
    alert(
        "Welcome to " + name + "!\n\n" +
        "Location: " + location + "\n" +
        "Price: $" + price + " per night\n\n" +
        "This is a demo website. Booking is not available yet."
    );
}What it does:
It receives three pieces of information when called:
name → house name (e.g. "The Azure Villa")
location → city/country (e.g. "Santorini, Greece")
price → number (e.g. 450)

It builds a message by joining strings together with +.
\n means “new line” so the text appears on separate lines in the alert.
alert(...) shows a simple browser popup with that message.
When it runs:

When someone clicks a “View House” button.

Example from the HTML:HTMLonclick="viewHouse('The Azure Villa', 'Santorini, Greece', 450)"That passes the three values into the function.That’s the whole JavaScript. No loops, no arrays, no complex logic — just two small functions that respond to button clicks.
