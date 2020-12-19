## Testing

### Browser Compatability

- I tested the appearance and responsiveness of the website across many different devices using Chrome Dev Tools.
- Generally, the appearance and responsiveness is quite good on different devices.

### Code Validation

Testing HTML with [The W3C Markup Validation Service ](https://validator.w3.org/)
- Home page errors discovered when run through validation:

![Home Page Errors](readme-images/home-page-errors.png)

- There were no errors on the About page.

- For the Media page the following two errors were discovered for each of the six Spotify music clips:

![Media Page Errors](readme-images/media-page-errors.PNG)

- There were no errors on the Shop page.

- For the Contact page the following errors were discovered:

![Contact Page Errors](readme-images/contact-page-errors.PNG)

- Resolution of errors:
    - Home page errors were resolved by adding the button classes to the anchor tag.
    - Media page errors were resolved by removed those obsolete attributes.
    - Contact page errors were resolved by changing the input type from "name" to "text".

Testing CSS with the [Jigsaw CSS Validation Service ](https://jigsaw.w3.org/css-validator/)
- While there were no errors with my own custom style.css file, the following two errors were discovered in Bootstrap's style sheet:
![CSS Error](readme-images/css-error.PNG)
- The above two errors are minor, and relate to CSS selectors that are not used in my website.
- Warnings were also discovered, but these relate mainly to "unknown vendor extensions", which can be safely ignored.

### Performance Testing

Testing page with Lighthouse in Chrome Dev Tools to optimise performance, accessibility, best practices and SEO
- Lighthouse desktop report:
![Lighthouse Desktop Report](readme-images/home-desktop-performance.PNG)

- Lighthouse mobile report:
![Lighthouse Mobile Report](readme-images/home-mobile-performance.PNG)

- Accessibility, Best Practices and SEO were roughly the same on desktop and mobile, the only difference was in performance. Performance was roughly 92 on desktop and 73 on mobile. This was largely as a result of loading the hero image.

---
## Bugs
**Bug:** Burger menu wasn't showing dropdown of navigation links when clicked.

**Fix:** The solution was to revisit the "Progressive Enhancement With JavaScript Components - Part 1" lesson from the User Centric Frontend Development module, where I saw that jQuery, Popper, and Bootstrap scripts had to be included at the bottom of the body element to make the dropdown menu work properly.

**Bug:** Problem with horizontal scrolling on the contact page.

**Fix:** Solution was to set the margin to 0 for the Bootstrap row where the problem was.

**Bug:** Problem with my CSS styles not updating in my browser preview.

**Fix:** After asking for help on Slack, I was told that this was as a result of browser caching of my old CSS stylesheet. The solution therefore was to use a hard refresh of the page, done by holding Shift + refreshing the page.