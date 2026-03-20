# Responsive Portfolio — Lesson 8.11 Responsive Design Project

## Overview

This project is a **responsive personal portfolio homepage** built as the submission for **Lesson 8.11 — Graded Assignment: Responsive Design Project**.

The site is designed to demonstrate the responsive design concepts covered in Lessons 8.1–8.11, including:

* mobile-first CSS
* responsive breakpoints
* viewport setup
* relative units and fluid typography
* layout reflow across screen sizes
* responsive navigation
* touch-friendly spacing and controls

The page presents a portfolio-style layout with a fixed header, collapsible mobile navigation, hero section, featured projects section, skills section, and footer.

## Submission Notes

This README is included as part of the official submission for **Lesson 8.11 — Graded Assignment: Responsive Design Project** and is intended to document how the project meets the assignment requirements.

### Live Site

The project can be viewed live here:

[https://tristanedu.github.io/AlgoLearnCSS_Responsive-Design-Project/](https://tristanedu.github.io/AlgoLearnCSS_Responsive-Design-Project/)

### Important Testing Note

For accurate evaluation, the site is best viewed on a **real mobile device**.

During development, the browser in Spectre Tools introduced rendering inconsistencies that did not match real device behavior. The layout and interactions have been optimized for real-world usage on an actual phone.

Because of this:

* Mobile responsiveness is most accurate on a physical device
* Browser dev tools still work for general testing, but may not perfectly reflect real behavior

## Project Files

```text
index.html
style.css
```

### `index.html`

The HTML file provides the page structure and includes:

* semantic sections such as `header`, `nav`, `main`, `section`, `article`, and `footer`
* a hero section introducing Tristan Thomas
* a featured projects area with project cards
* a skills overview section
* a footer with navigation and social links
* a responsive navigation pattern built with a checkbox toggle and label
* the viewport meta tag required for responsive behavior

### `style.css`

The CSS file contains the responsive styling and includes:

* mobile-first base styles
* `min-width` media queries for larger layouts
* relative sizing with `rem`
* `clamp()` for fluid heading sizes
* flexbox layout patterns
* CSS Grid for the desktop hero layout
* sticky section behavior for layered visual transitions
* touch-friendly button and link spacing

## Responsive Features Implemented

### 1. Mobile-First CSS

The stylesheet begins with base styles intended for smaller screens first. Enhancements for larger devices are added later using `min-width` media queries.

This matches the assignment requirement to build from mobile upward rather than writing desktop styles first and shrinking them down.

### 2. Breakpoints Used

The project currently includes these responsive breakpoints:

| Breakpoint  | Purpose                                                   |
| ----------- | --------------------------------------------------------- |
| Base styles | Small mobile devices, starting around 320px               |
| `520px`     | Large phones and small tablets                            |
| `1024px`    | Small laptops and desktop layout changes                  |
| `1280px`    | Desktop expansion point reserved for large screens        |
| `1536px`    | Large desktop / very wide screen expansion point reserved |

### 3. Layout Changes by Screen Size

#### Small mobile (base styles)

* Navigation is collapsed into a hamburger-style toggle
* Navigation links stack vertically
* Main content is arranged in a single-column layout
* Buttons are large and easy to tap
* Sections fill the viewport vertically for strong mobile presentation

#### Large mobile / small tablet (`min-width: 520px`)

* Project cards are constrained with a maximum width for better readability
* Layout remains mostly vertical, but spacing becomes more comfortable on wider screens

#### Desktop (`min-width: 1024px`)

* Navigation switches from collapsed mobile menu to always-visible horizontal layout
* The menu label is hidden
* The hero section changes to a grid layout
* The portrait and text content are distributed into separate columns for a more desktop-oriented composition

#### Large desktop (`1280px` and `1536px`)

* These breakpoints are currently in place as extension points for future refinement
* Their presence shows planning for wider screens, even though the major desktop layout change happens at `1024px`

## Typography

The project uses responsive typography techniques including:

* `rem`-based font sizing
* readable line-height and spacing
* `clamp()` on major headings such as the skills section header and footer brand text

This helps the text remain readable across mobile and desktop screens without relying entirely on fixed pixel sizes.

## Responsive Navigation

The navigation is implemented using a mobile-friendly checkbox toggle pattern.

### On smaller screens:

* the menu is hidden by default
* the user opens it using the menu label button
* links are shown in a stacked vertical list

### On desktop screens:

* the menu is always visible
* the toggle label is hidden
* the layout becomes more traditional and desktop-friendly

This satisfies the requirement for a navigation system that adapts across screen sizes.

## Responsive Layout Techniques

The site demonstrates multiple responsive layout strategies:

* **Flexbox** for alignment, spacing, and wrapping
* **CSS Grid** in the hero section at desktop width
* **viewport-relative units** such as `dvh` and `dvw`
* **sticky positioning** for layered sections
* **custom properties** such as `--card-height` and `--peek` to control the featured project card stack

These choices make the page more dynamic and visually interesting while still demonstrating responsive behavior.

## Touch-Friendly Design

The project includes several touch-friendly choices for small screens:

* padded buttons and links
* large tap areas in the navigation and call-to-action buttons
* generous spacing between interactive elements
* readable default text size

These support the assignment requirement for mobile usability and touch accessibility.

## Viewport and Testing

The HTML file includes the required viewport meta tag:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

The site should be tested in browser developer tools across a range from **320px to 1200px and wider**.

### Suggested testing widths

* 320px
* 375px
* 480px
* 520px
* 768px
* 1024px
* 1200px+

### Testing notes

When reviewed across screen sizes, the layout should demonstrate:

* no intentional horizontal scrolling
* readable text and usable spacing
* navigation adapting appropriately to screen width
* content reflow from single-column mobile layout to more advanced desktop composition

## Assignment Requirement Checklist

| Requirement                               | Evidence in Project                                                                             |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Mobile-first CSS                          | Base styles are written first, with larger-screen enhancement through `min-width` media queries |
| Several breakpoints from 320px to 1200px+ | Base mobile styling plus `520px`, `1024px`, `1280px`, and `1536px` breakpoints                  |
| Responsive typography                     | Relative units and `clamp()` are used                                                           |
| Responsive layout                         | Mobile single-column layout shifts to more complex desktop structure                            |
| Responsive navigation                     | Checkbox-driven mobile nav becomes visible desktop nav                                          |
| Touch-friendly and readable               | Buttons, labels, and links use generous spacing and readable sizing                             |
| Viewport and testing                      | Viewport meta tag is included and layout is intended for testing from 320px to 1200px+          |

## Technologies Used

* HTML5
* CSS3
* Flexbox
* CSS Grid
* Media Queries
* Custom Properties (CSS Variables)
* Fluid Typography with `clamp()`

## Author

**Tristan Thomas**

Responsive portfolio project created for Lesson 8.11.
