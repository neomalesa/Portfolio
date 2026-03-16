
Live Demo: https://neo-malesa-bstrap-portfolio.netlify.app/

This repository contains the source code for my personal portfolio website, submitted for the Website Designer role assignment.

My design philosophy for this project was "Avant-Garde Minimalist" / "Industrial Tech." I wanted to prove that you do not need heavy JavaScript libraries or complex backend frameworks to build a premium, high-impact digital experience. This entire project was engineered using strictly native HTML5, CSS3, and Bootstrap 5.

Here is a technical breakdown of how I built this project from the header to the footer.



## The Header & Hero Section


The Navbar: I utilized Bootstrap's .navbar and .sticky-top classes to create a fixed header. Because JavaScript was strictly forbidden, I bypassed standard toggle menus and used Bootstrap's Flexbox utilities (.d-flex, .justify-content-between, .d-sm-flex) to manage the layout.

Interactive Links: The active link underlines were built entirely from scratch using CSS ::after pseudo-elements. By applying transform: translateX(-50%) and animating the width property on :hover and :focus, I created a smooth, dynamic underline effect without JS.

The Hero Background: I set the section to 100vh to guarantee it fills the viewport. I used background-attachment: fixed to create a native CSS parallax effect, and overlaid an absolutely positioned rgba(0, 0, 0, 0.7) div to ensure the massive Syne typography remains highly legible against the background image.

Accessibility: I implemented a .skip-link class that is hidden off-screen (top: -50px) but gracefully slides into view when navigating via keyboard (:focus), ensuring WCAG compliance.

## The About Me Card 



Grid Layout: I structured this using Bootstrap's grid system (.row, .col-lg-8, .col-md-5). This handles the responsive stacking natively—sitting side-by-side on desktops and stacking neatly on mobile devices.

Styling: I applied (solid) borders and completely removed standard soft shadows and rounded corners.

Imagery & Badges: The profile image utilizes a CSS filter: grayscale to sliglty match the theme. The tech stack badges use custom CSS variables to maintain strict color hierarchy.


## The Projects Grid 


Responsive Grid: Instead of using a JavaScript masonry library, I leveraged Bootstrap's highly efficient row-cols utility classes (.row-cols-1 .row-cols-md-2 .row-cols-lg-3). This tells the browser to automatically render 1 column on mobile, 2 on tablets, and 3 on large desktop screens. I used .g-4 and .g-5 gutter classes to keep the spacing airy and consistent.

Card Interactions: Each card uses object-fit: cover to ensure images never warp. I applied a default grayscale filter to the images, which transitions to full color (grayscale(0%)) alongside a -10px Y-axis translate when the user hovers over the card.



## The Contact Section 

Goal: Provide a clean, functional communication channel.

Form Validation: The form utilizes pure HTML5 validation and no backend.

Minimalist UI: I overrode Bootstrap's default .form-control styles, stripping away the borders and the glowing focus ring. Instead, I applied a stark border-bottom that highlights sharply when focused, fitting the avant-garde design language.

## The Footer

High-contrast footer.

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


##

#HTML5: Semantic tags utilized (<header>, <nav>, <main>, <section>, <footer>).

CSS3: Custom CSS variables (:root), Flexbox, Grid, CSS Transitions, and Media Queries.

Bootstrap 5: CDN integration for the responsive grid skeleton, spacing utilities, and layout classes. 

Bootstrap Icons: SVGs used for scalable, high-resolution social links.

Fonts: Syne (Headings) and Inter (Body copy) via Google Fonts.
