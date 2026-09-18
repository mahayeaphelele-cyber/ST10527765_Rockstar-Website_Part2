# ST10527765_Rockstar-Website_Part2
ROCKSTAR GAMES - Fan Website Project
Student: Aphelele Mahaye
Location: Durban, KwaZulu-Natal, South Africa
Module: Web Development - Part 1 & Part 2
Submission Date: May 2026
Website Type: Informational Fan Website (Inspired by Rockstar Games)
📖 PROJECT OVERVIEW
This is a fully responsive, extraordinary fan website inspired by Rockstar Games.
The site showcases iconic franchises like Grand Theft Auto, Red Dead Redemption,
Max Payne, L.A. Noire, and Bully. Built to feel like a real AAA game studio website
with perfect alignment, engaging UX, and neon-enhanced design.
Live Theme: Dark cinematic (#0A0A0F) with neon mesh background - Blue
#00E5FF + Green #39FF14 + Orange #FF6A00 + Rockstar Yellow #FFB700
📂 FILE STRUCTURE
1 /project-folder/
1 ├── index.html          
1 ├── about.html          
1 ├── games.html          
1 ├── store.html          
1 ├── contact.html        
1 ├── cart.html           
1 ├── changelog.html      
# Home - Hero, About, Featured Games
# About Us - Studio history & stats
# Games Catalog - 6 featured titles (IMAGES F
# Store - 6 products with Add to Cart
# Contact - Form with special features
# Cart - Persistent cart using localStorage
# Changelog - Development log (IN NAV ON EVERY
1 └── style.css           
# External Stylesheet - Single file for all p
All pages use ONE external stylesheet:
<link rel="stylesheet"
href="style.css">
✅ PART 1 - HTML STRUCTURE & CONTENT (Rubric)
1. Website Structure & Navigation
7 fully linked pages with consistent navigation on every page
Navigation menu contains: Home | About | Games | Store | Contact | Changelog |
Cart
Sticky navbar with logo 
ROCKSTAR
 - perfectly centered
Changelog added to navigation menu as requested - appears on ALL pages
Footer with links on all pages
2. Semantic HTML
Proper use of 
<nav> 
, 
<header> 
, 
Meta viewport tag for responsive: 
<section> 
, 
<footer> 
, 
<main>
 equivalent
<meta name="viewport"
content="width=device-width, initial-scale=1.0">
Alt attributes on all images for accessibility
3. Content Organization
Home: Hero + Who We Are + Stats + Featured Games + Gallery
Games: 6 game cards with images, titles, descriptions, Learn More links
Store: 6 products with prices, badges, Add to Cart
Contact: Form + Info cards + Social links
Cart: Shows item count from localStorage
Changelog: Version history documenting all fixes
About: Studio story
4. Images & Media
Fixed Issue: Old 
images/gta.jpg
 paths were broken - replaced with reliable
Unsplash CDN
All images use 
object-fit: cover
 to prevent stretching
Games page: 6 images now show correctly (GTA V, GTA Online, RDR2, Max
Payne Remake, Bully, L.A. Noire)
Contact page: No broken images
✅ PART 2 - CSS & RESPONSIVE DESIGN (Rubric)
External Stylesheet - Created & Implemented
File:
style.css
 (17,108 chars, ~600 lines)
Single external stylesheet linked in EVERY HTML page
No internal 
<style>
 tags in final version (rubric requirement met)
Clearly commented sections for marking
A. Default Style Code (Lines 1-45)
css
1 * { margin:0; padding:0; box-sizing:border-box; }
1 html { scroll-behavior:smooth; }
1 body { font-family: Arial; background: #0A0A0F; }
1 img { max-width:100%; height:auto; display:block; }
Reset, box-model, body background, image defaults
B. Typography Styles (Lines 47-75)
Headings: 
font-weight:900; text-transform:uppercase; letter
spacing:2px;
Responsive typography using 
clamp() 
:
h1: 
clamp(32px, 5vw, 58px)
 - scales from mobile to desktop
clamp(24px, 4vw, 36px)
h2: 
p: 
clamp(14px, 2vw, 16px)
 with 
text-wrap:balance
 for perfect
alignment
Lead paragraphs, section labels, eyebrows all styled
C. Layout Structure (Lines 77-210)
Navbar: flex, justify-content:space-between, max-width:1320px, sticky
Hero: flex column, centered, 82vh min-height, padding
Grid2:
grid-template-columns:1.1fr 0.9fr
 for About section
Cards:
grid-template-columns:repeat(3, 1fr)
 - 3 columns desktop
Products: 3 columns store grid
Gallery: 4 columns
Contact Wrapper:
grid-template-columns:1fr 1.6fr
Stats: 3 columns with border separation
Timeline (Changelog): border-left with entries
D. CSS Styling for Desktop (Lines 212-250)
Desktop max-width: 1320px centered with 
margin:0 auto
Card image height fixed: 240px (games), 260px (store), 460px (about) - prevents
huge images
Buttons: 
.btn-primary
 yellow #FFB700 with shadow, 
.btn-ghost
Badges: BESTSELLER (yellow), NEW (green #39FF14), PRE-ORDER (orange
#FF6A00)
Cart badge with count
E. CSS Decoration and Color (Lines 252-280)
Neon Edition: As requested by sir for more visible background
Background mesh:
radial-gradient(600px at 15% 20%, rgba(0,229,255,0.18))
 
Blue
radial-gradient(800px at 85% 10%, rgba(255,106,0,0.16))
 
Orange
radial-gradient(700px at 50% 90%, rgba(57,255,20,0.12))
 
Green
Dark glass cards: 
background: #12121A; backdrop-filter:blur(8px);
Hero title gradient: 
linear-gradient(90deg, #00E5FF, #FFB700,
#FF6A00)
 with background-clip:text
Card hover glow: 
box-shadow:0 10px 30px rgba(0,0,0,0.4), 0 0 20px
rgba(0,229,255,0.12)
F. CSS Pseudo Classes (Lines 282-330)
css
1 .nav-links a:hover { color:#FFB700; letter-spacing:2.5px; }
1 .card:hover { transform:translateY(-8px); border-color:#FFB700; }
1 .card:hover .card-img img { transform:scale(1.08); }
1 .btn:hover { letter-spacing:2.5px; }
1 .btn:active { transform:scale(0.97); }
1 a:focus { outline:2px solid #FFB700; }
1 .card:first-child { border-top:2px solid #FFB700; }
1 .gallery img:nth-child(odd):hover { border-color:var(--neon-blue); }
1 .hero::after { content:""; width:100px; height:3px; background:#FFB70
1 p::selection { background:#FFB700; color:#000; }
Includes :hover, :active, :focus, :first-child, :last-child, :nth-child, ::after, ::selection
G. Responsive Design
1. Media Queries / Breakpoints
1024px Tablet (iPad, small laptops)
768px Tablet Portrait / Mobile Landscape
480px Mobile Portrait
320px Extra Small
2. Layout Adjustment
Desktop: Cards 3 columns 
→
 Tablet: 2 columns 
→
 Mobile: 1 column
Grid2: 1.1fr 0.9fr 
→
 1fr stacked on mobile
Stats: 3 cols 
→
 1 col on mobile
Gallery: 4 cols 
→
 2 cols 
→
 2 cols (tighter) 
→
 1 col on very small
3. Typography Adjustment
h1: 58px 
→
 48px (1024px) 
→
 36px (768px) 
→
 28px (480px) 
→
 24px (320px)
p: 16px 
→
 14px 
→
 13px
Using clamp() for fluid scaling without extra queries
4. Navigation Adjustment
Desktop: Horizontal flex with gap:32px
Tablet/Mobile (
≤
768px): Hamburger checkbox hack
.hamburger { display:block; }
.nav-links { position:fixed; right:0; height:100vh;
width:280px; transform:translateX(100%); }
.nav-links.open { transform:translateX(0); }
No JavaScript needed for toggle - pure CSS checkbox
Perfect for sir's feature tablet
5. Images Adjustment (FIXED GAMES PAGE ISSUE)
Problem: Images were too big, stretching, not appearing
Solution:
Set fixed heights: 
height:260px; } 
, 
.card-img { height:240px; } 
, 
.prod-img-wrap {
.grid2-img-wrap { height:460px; }
Added 
object-fit:cover; object-position:center;
 - keeps faces
centered, no stretch
Responsive heights: 460px 
→
 360px (1024px) 
→
 300px (768px) 
→
 220px
(480px) 
→
 180px (320px)
Fixed src: Changed 
images/gta.jpg
 to Unsplash CDN URLs
Added 
overflow:hidden
 and 
mobile)
transition
 for zoom on hover (disabled on
Result: Perfectly aligned, organized, same size on all pages
🌟 SPECIAL FEATURES - Contact Page (Extraordinary)
Kept your original clean centered design from screenshot but added:
1. Live Character Count
Name: 0 / 50, Message: 0 / 300
Warns orange at 200 chars, red at 250+ chars
Class changes: 
.warn
 and 
2. Toast Notification System
.danger
#toast
 slides from right 
transform:translateX(400px)
 
→
translateX(0)
Shows "MESSAGE SENT ✓ We'll reply within 2 hours!" or warning
Auto-hides after 3 seconds and clears form
3. Form Validation
Checks if all fields filled before sending
Prevents empty submission
4. Response Badge
Green pulsing dot with animation 
pulse 1.5s infinite
"Average response time: 2 hours • Live support"
box-shadow
 pulse effect
5. Info Cards with Hover
3 cards: Headquarters, Support Hours, Player Support
Left border animation: 
transform:scaleY(0)
 
→
 
Lift effect: 
translateY(-3px)
6. Social Buttons
4 buttons: , , 📷, f
Hover: yellow background, lift, color change
7. Input Focus States
border-color:#FFB700
 + 
scaleY(1)
 on hover
box-shadow:0 0 0 3px
rgba(255,183,0,0.15)
 on focus
Smooth transition 0.3s
8. Security Note
"🔒 Your info is encrypted" with neon colors mention
🌈 NEON COLOR REQUIREMENT (Sir's Request)
Sir said: Change background to be more visible - Neon blue mixed with orange and
green effect
Implementation:
Blue: #00E5FF (cyan glow at top-left)
Green: #39FF14 (neon green glow at bottom)
Orange: #FF6A00 (warm glow at top-right)
Applied as fixed mesh background behind dark cards
Professional: Visible but readable - not blinding
Also used as badges: NEW = green, HOT = orange, BESTSELLER = yellow
Documented in footer and contact page
🚀 HOW TO RUN
1. Download all files into one folder
2. Make sure 
style.css
 is in same folder as HTML files
3. Double-click 
index.html
 to open in browser
4. Test responsiveness:
Chrome: Press F12 
→
 Click phone/tablet icon (top-left of DevTools)
Try iPad (768px), iPhone SE (375px), Desktop (1920px)
Check sir's feature tablet at 1024px and 768px
No server needed - pure HTML/CSS/JS
🧪 TESTING CHECKLIST FOR MARKING
External stylesheet linked in ALL 7 pages
No internal <style> tags in final version
Default styles present (reset, box-sizing, body)
Typography styles with clamp() responsive
Layout structure (flex, grid, max-width)
Desktop styling (1320px, 3-col cards, buttons)
Decoration & color (neon mesh, yellow accents)
Pseudo classes (hover, active, focus, first-child, nth-child, ::after)
Media queries: 1024px, 768px, 480px, 320px
Layout adjustment: 3
→
2
→
1 columns
Typography adjustment: h1 58px
→
24px
Navigation adjustment: horizontal
→
hamburger drawer
Images adjustment: fixed height + object-fit + responsive
Games images fixed - now show and aligned
Changelog in navigation on every page
Contact page special features
📝 CHANGELOG
v3.0 - 2026-05-13 - Rubric Part 2 Final (Extraordinary Edition)
Fixed hero height bug: 40vh/50vh 
→
 height:auto + min-height
Fixed games images too big: added fixed heights + object-fit:cover
Fixed broken image paths: images/gta.jpg 
→
 Unsplash CDN
Added neon mesh background: Blue #00E5FF + Green #39FF14 + Orange
#FF6A00
Added Changelog to navigation on every page
Implemented all rubric requirements with labeled comments
Perfect alignment: text-wrap:balance, clamp(), consistent padding
Full responsiveness: 320px-1320px tested
Added contact special features: char count, toast, validation, pulse badge, info
cards
Real UX: cart localStorage, hover, focus states, smooth scroll
v2.1 - 2026-05-12 - Image Organization
Replaced broken local images with Unsplash CDN
Added gallery grid with grayscale hover
v2.0 - 2026-05-11 - Responsive Foundation
Added media queries for tablet and mobile
Fixed nav overlapping
v1.0 - 2026-05-10 - Initial Structure
Basic navbar, hero, cards, footer
👨‍💻 AUTHOR
Aphelele Mahaye
Web Development Student
Durban, KwaZulu-Natal
Project built for assignment - Part 1 (HTML) & Part 2 (CSS & Responsive)
Inspired by Rockstar Games official site
Fan project - not affiliated with Rockstar Games
📄 LICENSE
Fan project for educational purposes. All game images from Unsplash / Rockstar
Games. No commercial use.
External Resources:
Fonts: Arial, Helvetica (system fonts - no external load needed for rubric)
Images: Unsplash CDN (https://images.unsplash.com)
Icons: Unicode emoji for social buttons
🎯 RUBRIC COMPLIANCE SUMMARY
Requirement
External stylesheet created
Implemented
File/Line
✅
style.css (17k chars)
Requirement Implemented File/Line
Implemented in each page ✅ All 7 HTML files link to style.css
Default style code ✅ Lines 1-45
Typography styles ✅ Lines 47-75 + clamp()
Layout structure ✅ Lines 77-210 (flex, grid)
CSS styling for desktop ✅ Lines 212-250 (1320px, 3-col)
CSS decoration and color ✅ Lines 252-280 (neon mesh)
CSS Pseudo classes ✅ Lines 282-330
Media queries/breakpoints ✅ 1024px, 768px, 480px, 320px
Layout adjustment ✅ 3
→
2
→
1 columns
Typography adjustment ✅ h1 58px
→
24px
Navigation adjustment ✅ Hamburger drawer
Images adjustment ✅ Fixed height + object-fit + responsive
Games images fixed ✅ 240px height, CDN URLs
Changelog in nav ✅ All pages
Contact special features ✅ Char count, toast, validation, etc.
Result: Extraordinary, perfectly aligned, fully responsive, real website feel - ready
for submission!
