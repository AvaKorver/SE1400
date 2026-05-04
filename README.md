https://drive.google.com/file/d/1m1n0JhHaydaqH7ZmZxVN0HgstHcEHsiu/view?usp=drive_link
WEBSITE LAYOUT DICTIONARY (SE 1400 FINAL)

WRAPPER
Definition:
The container that controls the entire page layout.

#wrapper {
 display: grid;
 grid-template-columns:
   minmax(0px, 1fr)
   repeat(6, minmax(0, 175px))
   minmax(0px, 1fr);
}
HEADER
Definition:
Top section with title/logo.

header {
 display: flex;
 justify-content: space-between;
 align-items: center;
}
NAVIGATION
Definition:
Menu used to move around the site.

Home / About / Contact links
Horizontal bar
Buttons

nav ul {
 display: flex;
}
MAIN
Definition:
Primary content area.

Paragraphs
Headings
Lists
Images/videos

main {
 padding: 2rem;
 background-color: white;
}
FOOTER
Definition:
Bottom section with extra info.

Copyright
Contact info
Small text

footer {
 text-align: center;
 padding: 1rem;
}
BODY
Definition:
Background + global styles.

Page background
Overall font
Full screen height

body {
 margin: 0;
 font-family: Verdana;
}
TEXT (HEADINGS + PARAGRAPHS)
Definition:
Controls readability + hierarchy.

Big title → small text
Sections
highlighted words

h1 { font-size: 2rem; }
h2 { margin-top: 2rem; }
p { line-height: 1.6; }
IMAGES (IMG)
Definition:
Inline pictures inside content.

Photo next to text
Profile images

img {
 max-width: 100%;
 height: auto;
}
BACKGROUND IMAGES 
Definition:
Large banner images.

Full-width image section
No <img> tag


#hero {
 background-image: url("image.jpg");
 background-size: cover;
 background-position: center;
}
VIDEO
Definition:
Embedded playable media.

Play button
Controls

video {
 max-width: 100%;
}
FLEXBOX 
Definition:
Controls layout direction and spacing.

Items in a row
Even spacing
Centered items

display: flex;
justify-content: space-between;
align-items: center;
FLEXBOX DECODER
Row → flex-direction: row
Column → flex-direction: column
Center → justify-content: center
Spread → space-between
Even → space-around
Left → flex-start
Right → flex-end
GRID (PAGE LAYOUT)
Definition:
Controls full page structure.

Sections aligned in columns
Clean spacing left/right

grid-column: 2 / -2;
GRID DECODER
Full width → 1 / -1
Center content → 2 / -2
Specific area → grid-row / column
FLOAT
Definition:
Wraps text around images/video.

Text wrapping around media

float: right;
POSITION
Definition:
Controls fixed/sticky elements.

Nav stays at the top
Footer sticks

position: sticky;
top: 0;
POSITION DECODER
Always visible → fixed
Scroll then stick → sticky
Normal → static
SPACING SYSTEM
Padding (inside):
padding: 20px;
Margin (outside):
margin: auto;
BACKGROUND SYSTEM
Solid → background-color
Gradient → linear-gradient
Image → background-image
RESPONSIVE DESIGN
Layout changes on a small screen

@media (max-width: 600px) {
 flex-direction: column;
}
PSEUDO ELEMENTS
Overlay
Extra design without HTML

body::before {
 content: "";

HEAD TEMPLATE

<!doctype html>
<html lang="en">

<head>
  <title>Page Name</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="robots" content="noindex">

  <link href="font-link" rel="stylesheet">
  <link href="style.css" rel="stylesheet">
  <link rel="icon" href="favicon.png">
</head>

UTAH TECH’S HEAD

HTML
CSS
<head>
<title>Utah Tech University</title>
  <meta charset="utf-8">
  <meta name="robots" content="noindex, nofollow">
  <link rel="stylesheet" href="style.css">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>






PRACTICE SITE’S HEAD

HTML
CSS
<head>
    <title>The History of Gnomes</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="robots" content="noindex">
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300..700&display=swap" rel="stylesheet">    
    <link href="style.css" rel="stylesheet" type="text/css" media="all">
    <link rel="icon" type="image/x-icon" href="images/fav.png">
</head>

All You Need to Know: Body HTML

Body: The container for EVERYTHING visible on the page (layout, structure, and content).

Basic Body Structure
<body>
  <div id="wrapper">
    <header></header>
    <nav></nav>
    <div id="hero"></div>
    <main></main>
    <footer></footer>
  </div>
</body>
Body with Layout Containers
<body>
  <div id="bluebar"></div>
  <div id="greybar"></div>

  <header></header>
  <nav></nav>

  <main></main>
</body>

All You Need to Know: Body CSS

BASIC BODY TEMPLATE
body {
 margin: 0;
 font-family: Verdana, Arial, sans-serif;
 color: #666666;
 background-color: #ffffff;
}
DEFAULT RESET
Remove browser spacing
body {
 margin: 0;
 padding: 0;
}
Prevent weird overflow
body {
 overflow-x: hidden;
}
FULL PAGE BACKGROUND SYSTEM
Solid Color Background
body {
 background-color: #ffffff;
}
Gradient background
body {
 background-image: linear-gradient(to bottom, #eeeeee, #ffffff);
 background-attachment: fixed;
}
Image background
body {
 background-image: url("bg.jpg");
 background-size: cover;
 background-position: center;
 background-repeat: no-repeat;
}
BODY LAYOUT CONTROL
Center page content system
body {
 max-width: 1100px;
 margin: auto;
}
Full page stretch
body {
 width: 100%;
 min-height: 100vh;
}
FLEXBOX BODY (global, applies to all)
body {
 display: flex;
 flex-direction: column;
}
Center EVERYTHING
body {
 display: flex;
 justify-content: center;
 align-items: center;
 height: 100vh;
}
GRID BODY 
Full page grid system
body {
 display: grid;
 grid-template-columns:
   minmax(0px, 1fr)
   repeat(6, minmax(0, 175px))
   minmax(0px, 1fr);
}
BODY + WRAPPER RULE
Wrapper inside body controls layout
#wrapper {
 display: grid;
}
SCROLL BEHAVIOR
Smooth page control
body {
 scroll-behavior: smooth;
}
Prevent horizontal scroll issues
body {
 overflow-x: hidden;
}
GLOBAL TEXT CONTROL
body {
 font-family: Verdana, Arial, sans-serif;
 line-height: 1.6;
 color: #666666;
}
BODY PATTERNS
Pattern 1: Standard Website Body
body {
 margin: 0;
 font-family: Verdana, Arial, sans-serif;
}
Pattern 2: Gradient Site 
body {
 background-image: linear-gradient(to bottom, #eeeeee, #ffffff);
 background-attachment: fixed;
}
Pattern 3: Grid Layout Website
body {
 display: grid;
}
Pattern 4: Full Page Flex Layout
body {
 display: flex;
 flex-direction: column;
 min-height: 100vh;
}
If it affects:
whole page layout → BODY
background → BODY
global font/color → BODY
page structure system → BODY
Viewport Height (vh)
Full screen height
body {
 min-height: 100vh;
}
(100vh = 100% of the screen height)
Overlays basic structure
body::before {
 content: "";
}
Dark or light layer over the background
body::before {
 content: "";
 position: fixed;
 top: 0;
 left: 0;
 width: 100%;
 height: 100%;
 background: rgba(0, 0, 0, 0.4);
 z-index: -1;
}
Adds content at the bottom of the page
body::after {
 content: "";
 display: block;
}
If using pseudo-elements:
position: fixed;
inset: 0;
Behind everything
z-index: -1;

All You Need to Know: Wrapper HTML

Wrapper: A container that holds the entire page layout and controls positioning.


Basic Wrapper
<div id="wrapper">
  <header></header>
  <nav></nav>
  <main></main>
  <footer></footer>
</div>
Wrapper with Full Layout
<div id="wrapper">

  <div id="bluebar"></div>
  <div id="greybar"></div>

  <header></header>
  <nav></nav>
  <div id="hero"></div>

  <main></main>
  <footer></footer>

</div>

All You Need to Know: Wrapper CSS



Wrapper = controls page layout system (grid or centered layout)

WRAPPER TEMPLATE 
#wrapper {
 display: grid;
}
GRID WRAPPER
#wrapper {
 display: grid;
 grid-template-columns:
   minmax(0px, 1fr)
   repeat(6, minmax(0, 175px))
   minmax(0px, 1fr);
}

WRAPPER IDENTIFICATION RULES
Page uses grid layout → wrapper has display: grid
Centered content with margins → 1fr columns on sides
Full-width sections → grid-column: 1 / -1
Main content centered → grid-column: 2 / -2

CENTERED WRAPPER 
#wrapper {
 max-width: 1100px;
 margin: auto;
}
FULL WIDTH WRAPPER
#wrapper {
 width: 100%;
}
GRID ROW CONTROL
#wrapper {
 grid-auto-rows: minmax(0px, auto);
}

Padding inside layout
#wrapper {
 padding: 20px;
}
GAP BETWEEN SECTIONS
#wrapper {
 gap: 20px;
}
Vertical page layout
#wrapper {
 display: flex;
 flex-direction: column;
 min-height: 100vh;
}
STICKY FOOTER LAYOUT
#wrapper {
 display: flex;
 flex-direction: column;
 min-height: 100vh;
}

main {
 flex: 1;
}
WRAPPER + GRID PLACEMENT SYSTEM
Example placement
header {
 grid-column: 2 / -2;
}

nav {
 grid-column: 2 / -2;
}

#hero {
 grid-column: 1 / -1;
}

main {
 grid-column: 2 / -2;
}
RESPONSIVE WRAPPER
Smaller screens
@media (max-width: 900px) {
 #wrapper {
   grid-template-columns: 1fr;
 }
}
WRAPPER IDENTIFICATION RULES
controlling layout → wrapper
centering page → wrapper
using grid → wrapper
organizing sections → wrapper
COMMON WRAPPER PATTERNS
Pattern 1: Grid Layout Site
#wrapper {
 display: grid;
 grid-template-columns:
   minmax(0px, 1fr)
   repeat(6, minmax(0, 175px))
   minmax(0px, 1fr);
}
Pattern 2: Centered Website
#wrapper {
 max-width: 1100px;
 margin: auto;
}
Pattern 3: Full Page Flex Layout
#wrapper {
 display: flex;
 flex-direction: column;
 min-height: 100vh;
}
Pattern 4: Simple Container
#wrapper {
 width: 100%;
 padding: 20px;
}
All You Need to Know: Header HTML

Header: Above the navigation, containing titles and logos. 

Basic Header
<header>
  <h1>Header Text</h1>
</header>
Page-specific Header (including logo)
<header>
  <h1> <a href="index.html">Header Text</a> </h1>
  <img src="logo.png" alt=" Logo">
</header>
All You Need to Know: Header CSS
(The head of your page must reference this CSS)
Grid = page layout (where header goes)
Flexbox = layout inside header

Header template:
header {
 display: flex;
 justify-content: space-between;
 align-items: center;
 padding: 15px 30px;
 background-color: #1f4b75;
 color: white;
}
Flexbox:
header {
 display: flex;
}
Flexbox Tips:
flex-direction: row;
[ Item 1 → Item 2 → Item 3 ]
Options:
flex-direction: row;
flex-direction: column;
flex-direction: row-reverse;
flex-direction: column-reverse;
Options:
justify-content: center;
justify-content: space-around;
justify-content: space-between;
justify-content: flex-start;
justify-content: flex-end;
HEADER IDENTIFICATION RULES

Horizontal layout → display: flex
Space between items → justify-content: space-between
Center everything → justify-content: center
Vertical stacking → flex-direction: column
Center vertically → align-items: center

Padding
header {
 padding: 15px 30px;
}
Margin
header {
 margin: 0;
}
Spacing between items
header item {
 margin-left: 20px;
}
Full-Screen Bar
header {
 width: 100%;
} 
Centered content inside the header
header {
 max-width: 1100px;
 margin: auto;
}
Solid Color:
background-color: #1f4b75;
Gradient:
background: linear-gradient(to right, #1f4b75, #163a5c);
Image:
background-image: url("header.jpg");
background-size: cover;
background-position: center;
Header Text Styling:
header h1 {
 font-size: 2rem;
 margin: 0;
}
Clickables
header a {
 text-decoration: none;
 color: white;
}
Logo/ Image Styling:
header img {
 height: 40px;
}
Prevent distortion:
header img {
 height: 40px;
 width: auto;
}
“Sticky and Fixed” Headers
Sticky:
header {
 position: sticky;
 top: 0;
 z-index: 1000;
}
Fixed:
header {
 position: fixed;
 top: 0;
 width: 100%;
}
body {
 margin-top: 80px;
}
Layering: The higher the number, the further to the top
header {
 z-index: 1000;
}
Stack on small screens:
@media (max-width: 600px) {
 header {
   flex-direction: column;
   text-align: center;
 }
}
Pattern 1: Split 
header {
 display: flex;
 justify-content: space-between;
 align-items: center;
}
Pattern 2: Centered
header {
 text-align: center;
}
Pattern 3: Logo left, nav right
header {
 display: flex;
 justify-content: space-between;
}
Pattern 4: Stacked (title above nav)
header {
 display: flex;
 flex-direction: column;
}
UTAH TECH SITE’S HEADER
HTML
CSS
 <header>
   <h1><a href="index.html">Utah Tech University</a></h1>
  </header>


header { 
background-color: #0D3B66 ;
background-attachment: fixed; font-family: Georgia ;
color:#FFFFFF ; 
padding: 0.5rem 1rem ;
grid-row: 1/ 2;
grid-column: 2 / -2;
 }
header h1 {
margin: 0;
font-size: 2em;
line-height: 140%;
padding-left: 1em;
background-image: url('utahtechlogo.svg');
background-position: right;
background-repeat: no-repeat;
background-origin: content-box;
margin-bottom: 0;
text-decoration: none;
color: #FFFFFF;
}
header a:visited {
text-decoration: none;
color: #FFFFFF;
}

MY SITE’S HEADER
HTML
CSS
 <header></header>
header {
    grid-column: 1 / 9;
    background-color: rgba(185, 154, 200, 0);
    height: 120px;}

All You Need to Know: Navigation HTML

Navigation: Used for menus/links that help users move around your site.

Basic Navigation
<nav>
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
  <a href="contact.html">Contact</a>
</nav>
Navigation with List 
<nav>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Contact</a></li>
  </ul>
</nav>
Navigation inside Header
<header>
  <h1>Site Name</h1>
  <nav>
    <ul>
      <li><a href="">Home</a></li>
      <li><a href="">Gallery</a></li>
    </ul>
  </nav>
</header>
Dropdown Navigation (basic structure)
<nav>
  <ul>
    <li><a href="">Home</a></li>
    <li>
      <a href="">Menu</a>
      <ul>
        <li><a href="">Option 1</a></li>
        <li><a href="">Option 2</a></li>
      </ul>
    </li>
  </ul>
</nav>

All You Need to Know: Navigation CSS
Grid = where nav sits on the page, Flexbox = layout inside the nav

Navigation Template
nav {
 display: flex;
 justify-content: center;
 align-items: center;
 background-color: #1f4b75;
 padding: 10px 20px;
}
Remove Default List Styling
nav ul {
 list-style: none;
 margin: 0;
 padding: 0;
}
Horizontal Navigation
nav ul {
 display: flex;
}
Navigation Links
nav a {
 text-decoration: none;
 color: white;
 padding: 10px 15px;
 display: block;
}
Hover Effects
nav a:hover {
 background-color: #163a5c;
}
Active Link (current page)
nav a.active {
 font-weight: bold;
 border-bottom: 2px solid white;
}
Flexbox for Navigation
Default Row Layout
Home → About → Contact
nav ul {
 display: flex;
 flex-direction: row;
}
Spacing Options
justify-content: center;
justify-content: space-around;
justify-content: space-between; 
justify-content: flex-start;
justify-content: flex-end;
NAVIGATION IDENTIFICATION RULES
Horizontal menu → display: flex
Even spacing → justify-content: space-around
Push links apart → space-between
Center menu → justify-content: center
Vertical menu → flex-direction: column
Items aligned left → justify-content: flex-start
Items aligned right → justify-content: flex-end

Spacing
Padding (inside buttons)
nav a {
 padding: 10px 15px;
}
Space between items
nav li {
 margin-right: 20px;
}
Full Width Navigation Bar
nav {
 width: 100%;
}
Centered Content Inside Nav
nav ul {
 max-width: 1100px;
 margin: auto;
}
Background Styles
Solid
background-color: #1f4b75;
Gradient
background: linear-gradient(to right, #1f4b75, #163a5c);
Dropdown Navigation CSS
nav ul ul {
 display: none;
 position: absolute;
 background-color: #1f4b75;
}
nav li:hover ul {
 display: block;
}
Sticky / Fixed Navigation
Sticky
nav {
 position: sticky;
 top: 0;
 z-index: 1000;
}
Fixed
nav {
 position: fixed;
 top: 0;
 width: 100%;
}
body {
 margin-top: 60px;
}
Mobile Navigation (Responsive)
Stack on Small Screens
@media (max-width: 600px) {
 nav ul {
   flex-direction: column;
   text-align: center;
 }
}
Common Navigation Patterns
Pattern 1: Centered Menu
nav {
 display: flex;
 justify-content: center;
}
Pattern 2: Spread Across
nav {
 display: flex;
 justify-content: space-between;
}
Pattern 3: Right-Aligned Menu
nav {
 display: flex;
 justify-content: flex-end;
}
Pattern 4: Vertical Sidebar
nav ul {
 display: flex;
 flex-direction: column;
}
UTAH TECH SITE’S NAV
HTML
CSS
 <nav>
   <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="students.html">Students</a></li>
      <li><a href="faculty.html">Faculty</a></li>
      <li><a href="alumni.html">Alumni</a></li>
      <li><a href="shop.html">Shop</a></li>
   </ul>
</nav>



nav { 
font-weight: bold; 
background-color: #F3F3F3;
padding: 0.5rem 0.5rem 0.5rem 2rem; 
grid-row: 2 / 3;
grid-column: 2 / -2;
background-color: #424242;
margin: 0;
padding: 0;
position: sticky;
top: 0;
 }
nav ul {
   margin: 0;
   padding: 0;
   display: flex;
   flex-flow: row nowrap;
   list-style-type: none;}
nav ul li {
   width: 100%;}
nav a { text-decoration: none ;
    color: #FFFFFF;
   padding: 1rem 0rem;
   display: block;
   text-align: center;
   text-decoration: none; 
  transition: background-color 0.5s ease-out;}
nav a:hover {
   background-color: #BA1C21;}



MY SITE’S NAV
HTML
CSS
<nav>
<ul class="nav-tabs">
<li><ahref="index.html">HOME</a></li>
<li><ahref="aboutme.html">ABOUTME</a></li>
<li><ahref="gallery.html">GALLERY</a></li>
<li><ahref="journey.html">JOURNEY</a></li> <li><ahref="goals.html">GOALS</a></li>            
</ul>
</nav>


nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 20;
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  background: #ffffff;
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
  padding: 10px 0;
  border-top: 2px solid black;
  border-bottom: 2px solid black;
}
.nav-tabs {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 20px;
    font-family: monospace;
    font-size: 30px;
    margin: 0;
    padding: 0;
}
.nav-tabs li {
    display: inline;
}
.nav-tabs a {
    text-decoration: none;
    color: #53412f;
    padding: 10px 20px;
    transition: background 0.3s;
}
.nav-tabs a:hover {
    text-decoration: none;
    color: #53412f;
    background: lightgrey;
}


All You Need to Know: Main HTML

Main: The primary content area of the page.

Basic Main
<main>
  <h1>Page Title</h1>
  <p>Main content goes here</p>
</main>
Main with Sections
<main>
  <h2>Section Title</h2>
  <p>Content</p>

  <h2>Another Section</h2>
  <ul>
    <li>Item</li>
  </ul>
</main>
Main with Media
<main>
  <h2>About</h2>

  <video controls>
    <source src="video.mp4" type="video/mp4">
  </video>

  <p>Text content</p>
</main>

All You Need to Know: Main CSS

Main = content layout + readable spacing

MAIN TEMPLATE
main {
 padding: 20px;
 background-color: #ffffff;
}
MAIN IDENTIFICATION RULES
Main content area → main
Readable spacing → padding
White content box → background-color
Centered layout → grid column rules

GRID PLACEMENT 
main {
 grid-row: 4 / 5;
 grid-column: 2 / -2;
}
SPACING 
Padding inside main
main {
 padding-left: 2rem;
 padding-right: 2rem;
}
Full padding
main {
 padding: 2rem;
}
BACKGROUND STYLES
White content box
main {
 background-color: #ffffff;
}
Light background section
main {
 background-color: #f3f3f3;
}
TEXT STYLING INSIDE MAIN
main {
 line-height: 1.6;
}
FLOATING CONTENT 
Image or video to the right
main img, main video {
 float: right;
 padding-left: 2rem;
}
FLOAT RULES
Wrap text around media → float: right
Remove on mobile → float: none
MEDIA INSIDE MAIN
Responsive video/image
main img, main video {
 max-width: 100%;
 height: auto;
}
LIST STYLING
main ul {
 padding-left: 20px;
}
MULTI-COLUMN LAYOUT
main {
 display: grid;
 grid-template-columns: 1fr 1fr;
 gap: 20px;
}
FLEXBOX MAIN
main {
 display: flex;
 flex-direction: column;
}
WIDTH CONTROL
Keep content centered
main {
 max-width: 1100px;
 margin: auto;
}
RESPONSIVE MAIN
Mobile adjustments
@media (max-width: 600px) {
 main {
   padding: 1rem;
 }
}
Remove float on small screens
@media (max-width: 900px) {
 main img, main video {
   float: none;
   width: 100%;
 }
}
COMMON MAIN PATTERNS
Pattern 1: Basic Content Area
main {
 padding: 20px;
 background-color: white;
}
Pattern 2: Centered Content Box
main {
 max-width: 1100px;
 margin: auto;
}
Pattern 3: Grid Content Layout
main {
 display: grid;
 grid-template-columns: 1fr 1fr;
}
Pattern 4: Media + Text Layout
main img {
 float: right;
}
All You Need to Know: Footer HTML

Footer: Bottom section of the page containing copyright, links, contact info, etc.

Basic Footer
<footer>
  <p>Copyright © 2026 My Website</p>
</footer>
Footer with Links
<footer>
  <p>Copyright © 2026</p>
  <a href="mailto:email@example.com">Email Us</a>
</footer>
Footer with Structured Content
<footer>
  <div>
    <h3>Contact</h3>
    <p>Address, phone, email</p>
  </div>
</footer>

All You Need to Know: Footer CSS

FOOTER TEMPLATE
footer {
 background-color: #1f4b75;
 color: white;
 text-align: center;
 padding: 20px;
}
FOOTER IDENTIFICATION RULES
Bottom of page → footer
Centered text → text-align: center
Horizontal layout → display: flex
Stacked content → flex-direction: column
Full-width bar → width: 100%

FOOTER LAYOUT 
Horizontal footer sections
footer {
 display: flex;
 justify-content: space-between;
 align-items: center;
}
Stacked footer
footer {
 display: flex;
 flex-direction: column;
 text-align: center;
}
SPACING
Padding inside the footer
footer {
 padding: 20px;
}
Space between items
footer div {
 margin: 10px;
}
BACKGROUND STYLES
Solid color footer
footer {
 background-color: #424242;
}
Gradient footer
footer {
 background: linear-gradient(to right, #1f4b75, #163a5c);
}
TEXT STYLING
Footer text
footer {
 font-size: 0.8rem;
 color: #ffffff;
}
Links in footer
footer a {
 color: white;
 text-decoration: none;
}
HOVER EFFECTS
footer a:hover {
 text-decoration: underline;
}
FULL WIDTH FOOTER
footer {
 width: 100%;
}
CENTERED FOOTER CONTENT
footer {
 max-width: 1100px;
 margin: auto;
 text-align: center;
}
FOOTER GRID PLACEMENT
footer {
 grid-row: 5 / 6;
 grid-column: 2 / -2;
}
STICKY FOOTER 
footer {
 position: sticky;
 bottom: 0;
}
FIXED FOOTER
footer {
 position: fixed;
 bottom: 0;
 width: 100%;
}
COMMON FOOTER PATTERNS
Pattern 1: Simple Footer
footer {
 text-align: center;
 padding: 20px;
}
Pattern 2: Split Footer
footer {
 display: flex;
 justify-content: space-between;
}
Pattern 3: Centered Footer
footer {
 text-align: center;
}
Pattern 4: Multi-column Footer
footer {
 display: flex;
 justify-content: space-around;
}
All You Need to Know: Text HTML

Text: Used to display content, organize information, and create hierarchy.

Basic Paragraph
<p>This is a paragraph of text.</p>
Headings (Hierarchy)
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Subsection</h3>
Paragraph with Inline Styling
<p>This is <span class="highlight">important</span> text.</p>
Line Breaks + Address Style
<p>
Line 1<br>
Line 2<br>
Line 3
</p>
Lists
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>

All You Need to Know: Text CSS
Text CSS = controls readability + spacing + hierarchy

BASIC TEXT TEMPLATE
body {
 font-family: Verdana, Arial, sans-serif;
 color: #666666;
 line-height: 1.6;
}
HEADINGS
Main heading
h1 {
 font-size: 2rem;
 margin: 0;
}
Section heading
h2 {
 color: #424242;
 font-family: Georgia;
}
Subheading
h3 {
 color: #003058;
}
PARAGRAPHS
p {
 margin-bottom: 1rem;
}
TEXT SPACING
Line spacing
body {
 line-height: 1.6;
}
Space between sections
h2 {
 margin-top: 2rem;
}
TEXT ALIGNMENT
text-align: left;
text-align: center;
text-align: right;
TEXT COLOR
color: #333333;
HIGHLIGHTED TEXT
.highlight {
 color: #BA1C21;
 font-weight: bold;
}
FONT STYLING
font-weight: bold;
font-style: italic;
text-transform: uppercase;
LINKS
a {
 text-decoration: none;
 color: #003058;
}
Hover effect
a:hover {
 text-decoration: underline;
}
LIST STYLING
ul {
 padding-left: 20px;
}
Remove bullets
ul {
 list-style: none;
}
TEXT IDENTIFICATION RULES
Main title → h1
Section titles → h2
Subsections → h3
Body text → p
Important word → span + class
Lists → ul + li
TEXT HIERARCHY
Biggest → h1
Medium → h2
Smaller → h3
Content → p
COMMON TEXT PATTERNS
Pattern 1: Standard Content
body {
 font-family: Verdana;
 line-height: 1.6;
}
Pattern 2: Sectioned Layout
h2 {
 margin-top: 2rem;
}
Pattern 3: Highlight Important Text
.highlight {
 color: red;
 font-weight: bold;
}
Pattern 4: Clean Links
a {
 text-decoration: none;
}

All You Need to Know: Images & Videos HTML

Media: Used to display visuals (images, videos) inside your page.

IMAGES
Basic Image
<img src="image.jpg" alt="Description of image">
Image inside content
<main>
  <img src="photo.jpg" alt="Photo">
  <p>Text wraps around image</p>
</main>
Decorative (background instead)
<div id="hero"></div>
VIDEOS
Basic Video
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
Video with size + poster
<video controls width="480" height="270" poster="poster.jpg">
  <source src="video.mp4" type="video/mp4">
</video>
Fallback text
<video controls>
  <source src="video.mp4" type="video/mp4">
  Your browser does not support video.
</video>


All You Need to Know: Images & Videos CSS


Media CSS = controls size, layout, and responsiveness

BASIC IMAGE TEMPLATE
img {
 max-width: 100%;
 height: auto;
}
FIXED SIZE IMAGE
img {
 width: 300px;
 height: auto;
}
IMAGE POSITIONING
Float right 
img {
 float: right;
 padding-left: 2rem;
}
Float left
img {
 float: left;
 padding-right: 2rem;
}
CENTER IMAGE
img {
 display: block;
 margin: auto;
}
IMAGE AS BACKGROUND
#hero {
 height: 300px;
 background-image: url("image.jpg");
 background-size: cover;
 background-position: center;
 background-repeat: no-repeat;
}
BACKGROUND IMAGE RULES
Cover entire area → background-size: cover
Center image → background-position: center
No repeat → background-repeat: no-repeat

VIDEO STYLING
Responsive video
video {
 max-width: 100%;
 height: auto;
}
Float video 
video {
 float: right;
 padding-left: 2rem;
}
REMOVE FLOAT (MOBILE)
@media (max-width: 900px) {
 img, video {
   float: none;
   width: 100%;
 }
}
GRID IMAGE LAYOUT
#gallery {
 display: grid;
 grid-template-columns: repeat(3, 1fr);
 gap: 20px;
}
Images inside the grid
#gallery img {
 width: 100%;
 height: auto;
}
IMAGE CARD STYLE
.card {
 background-color: rgba(255,255,255,0.9);
 padding: 15px;
 border-radius: 10px;
 text-align: center;
}
MEDIA IDENTIFICATION RULES
Image inline → <img>
Hero/banner → background-image
Video → <video>
Responsive → max-width: 100%
Text wrapping → float

COMMON MEDIA PATTERNS
Pattern 1: Inline Image with Text
img {
 float: right;
}
Pattern 2: Hero Image
#hero {
 background-image: url("hero.jpg");
 background-size: cover;
}
Pattern 3: Responsive Media
img, video {
 max-width: 100%;
 height: auto;
}
Pattern 4: Grid Gallery
display: grid;
grid-template-columns: repeat(3, 1fr);


CLASS SELECTOR DICTIONARY (CSS “.” SYSTEM)

HTML
<img class="logo">
<div class="side">
<img class="responsive">
<div class="clear">
CSS
.side — SIDE CONTENT BOX
Small box on the side of the page
Often image + caption or note
Text wraps around it
Sits left or right of the main content

.side {
 float: right;
 width: 300px;
 padding: 20px;
 font-style: italic;
 font-size: .75rem;
}
 .logo — BRAND IMAGE CONTROL
Small logo in nav/header
Never huge
Always neatly sized

.logo {
 width: 90%;
 max-width: 200px;
 padding-top: 20px;
}
 .responsive — AUTO-SCALING IMAGE
Image fills the width of the page or container
Shrinks on mobile
No overflow

.responsive {
 width: 100%;
}
 .clear — RESET FLOATS
The next section starts BELOW the images
No text wrapping around floats
Layout “resets” after side elements

.clear {
 clear: both;
}

.side → floats side box
.logo → controls logo size
.responsive → makes images scale
.clear → fixes float layout issues









