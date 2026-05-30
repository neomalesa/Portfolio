


## The Header & Hero Section


The Navbar: I utilized Bootstrap's .navbar and .sticky-top classes to create a fixed header. Because JavaScript was strictly forbidden, I bypassed standard toggle menus and used Bootstrap's Flexbox utilities (.d-flex, .justify-content-between, .d-sm-flex) to manage the layout.





Interactive Links: The active link underlines were built entirely from scratch using CSS ::after pseudo-elements. 



The Hero Background: I set the section to 100vh to guarantee it fills the viewport. 



Accessibility: I implemented a .skip-link class that is hidden off-screen (top: -50px) but gracefully slides into view when navigating via keyboard (:focus), ensuring WCAG compliance.





## The About Me Card 



Grid Layout: I structured this using Bootstrap's grid system  This handles the responsive stacking  on desktops and stacking neatly on mobile devices.



Imagery & Badges: The profile image utilizes a CSS filter: grayscale to sliglty match the theme. The tech stack badges use custom CSS variables to maintain strict color hierarchy.


## The Projects Grid 


Responsive Grid: Instead of using a JavaScript masonry library, I leveraged Bootstrap's highly efficient row-cols utility classes  This tells the browser to automatically render 1 column on mobile, 2 on tablets, and 3 on large desktop screens. I 

I applied a default grayscale filter to the images, which transitions to full color (grayscale(0%)) alongside a -10px Y-axis translate when the user hovers over the card.



## The Contact Section 



Form Validation: The form utilizes pure HTML5 validation and no backend.



Minimalist UI: I overrode Bootstrap's default .form-control styles, stripping away the borders and the glowing focus ring. Instead, I applied a stark border-bottom that highlights sharply when focused, fitting the avant-garde design language.



## The Footer



I used a dark background color and specific HTML <span> targeting to highlight my name against the muted grey text.


## Bonus Feature: Print-Ready Resume View

I successfully implemented the Print-Ready Résumé bonus requirement.

By writing a custom @media print CSS block, I created a magic filter for the browser's print engine. When a user presses Ctrl + P (or Cmd + P), the CSS strictly enforces the following:

display: none !important is applied to the Hero, Navbar, Projects, and Contact sections to hide non-essential elements.

Backgrounds are forced to white and text to black to save printer ink.

Shadows and thick borders are stripped from the "About Me" card.

The result is a flawlessly formatted, minimalist, black-and-white 1-page paper résumé generated directly from the live website. It prints best in landscape.


## Image credits 
All images used in the projects grids for this portfolio are royalty-free and sourced from Unsplash.


