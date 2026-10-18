# Starlight Cinemas — Project Documentation

**Student:** Nikoi Cole  
**Assignment:** Dynamic Websites and Applications — Assignment 1  
**Date:** 14 October 2026  
**Project choice:** Movie Night

## 1. Introduction
Starlight Cinemas is a responsive demonstration website for a fictional Jamaican cinema. It provides movie browsing, sample showtimes, seat reservation, digital tickets, basic account screens and administrative movie management. The project was designed to resemble a professional customer experience while remaining a front-end coursework demonstration.

## 2. Goals and intended users
The main user is a cinema customer looking for movies and an easy booking experience. A secondary user is a cinema administrator who maintains demo movies and showtimes. Goals include clear navigation, responsive layouts, visible feedback after actions, and readable booking information.

## 3. Technologies and why they were chosen
- HTML5: semantic webpage structure across independent pages.
- CSS3: custom dark/black-and-gold theme, hover animations and layout styling.
- Bootstrap 5.3.3: responsive navbar with Collapse; grid utility classes on movie cards; movie-details Modal.
- JavaScript: data objects, arrays, DOM updates, event handlers, booking state, forms and browser persistence.
- jQuery 3.7.1: delegated input handler for dynamically rendered movie search.
- localStorage/sessionStorage: lightweight browser-local persistence for demonstrating workflows. They are not substitutes for a real secure backend.

## 4. Structure and page navigation
The home page links to movie listings and showtimes; customers can move to booking, confirmation and profile. Additional pages display cinemas, prices, events, gifts, retrieval and administration. All pages import shared styles and scripts for a consistent presentation. Consult `README.md` for the full page list.

## 5. Key implementation details
### 5.1 Movies and data
In `js/app.js`, `let movies = [...]` holds movie objects with IDs, names, genres, images and descriptions. The catalog is rendered into cards. Admin-edited movies are saved to browser storage and override code defaults until **Reset to Code Defaults** is selected.

### 5.2 Bootstrap
The responsive navigation uses Bootstrap Collapse. Movie cards use grid classes such as `row`, `col-6`, `col-md-4`, and `col-xl-3`. Movie details are displayed in a Bootstrap Modal. These are genuine Bootstrap features, not just library imports.

### 5.3 jQuery
The movie discovery interaction includes a delegated `jQuery(document).on('input', '#discoverQuery', ...)` handler in `js/app.js`. Typing narrows the list and updates the matching results display.

### 5.4 Booking and ticket logic
The booking screen uses JavaScript to track selected screenings, ticket categories, seats and a calculated total. Demo bookings are stored in localStorage; confirmation and profile views can render the booking reference. Printing relies on the browser print dialog. This is not a real paid ticketing or seat-locking service.

### 5.5 Registration and profiles
Registration and login are demonstration forms; browser storage tracks accounts and session state. Booking history appears in the signed-in profile on the same browser. This should never be represented as production-grade authentication.

### 5.6 Admin dashboard
Admin supports editing demonstration movies, showtimes and prices, and viewing/cancelling local booking records. Movie edits are local to the browser and do not change `app.js` on disk. The Admin view has no secure role-based access control.

### 5.7 E-gift prototype
Sending/saving an e-gift in the sender profile has been reported to work. Receiving gifts in a recipient's profile has been reported not to work reliably. The experimental wallet and redemption code exist but are **not accepted as passed testing**. There is no real payment or email delivery.

## 6. Requirements review
| Area | Evidence | Status |
|---|---|---|
| Multiple HTML pages | 14 separate HTML files | Implemented |
| Responsive design | Bootstrap grid/nav + custom responsive CSS | User-reported pass |
| Bootstrap JavaScript components | Collapse and Modal | User-reported working |
| jQuery interaction | Search input handler | User-reported working |
| JavaScript interactivity | Movie catalog, booking, tickets, Admin | User-reported main flow working |
| Forms and validation | Login, registration and booking forms | Basic flow passed; edge cases need checking |
| GitHub with meaningful commits | Git history not supplied | **Pending** |
| Documentation and disclosure | README + project documentation | Drafted; student review required |
| E-gift receiving | Experimental feature | **Known failure** |

## 7. Testing record
These checks were **reported by the student** on 14 October 2026, not independently browser-automated:

| Test | Expected outcome | Outcome |
|---|---|---|
| Resize desktop/mobile viewport | Layout adapts | Reported pass |
| Movie Details | Opens information dialog | Reported pass |
| Movie search | Filters movie listing | Reported pass |
| Booking administration | Booking visible/manageable | Reported pass |
| Register and log in | Demo account flow completes | Reported pass |
| Book movie | Demo reservation created | Reported pass |
| View profile | Booking visible | Reported pass |
| Open digital ticket | Ticket view renders | Reported pass |
| Print ticket | Browser print dialog works | Reported pass |
| Send e-gift | Sender's gift appears in profile | Reported pass |
| Recipient opens e-gift | Gift appears in recipient profile | **Reported fail** |

**Additional tests before hand-in:** form invalid inputs, empty searches, mobile menu toggling, seat conflicts, cancelled bookings, keyboard navigation, image failures, refresh persistence, browser console errors and external CDN loading.

## 8. Constraints and future improvements
For a real client deployment, use a secure backend database, authorization for Admin, protected login sessions, a real payment provider, transaction-safe seat reservations and gift redemptions, automated tests, transactional email, privacy safeguards and licensed media assets. This coursework prototype does not provide those capabilities.

## 9. AI use disclosure
ChatGPT was used as a coding assistant to refine HTML, CSS and JavaScript, troubleshoot browser storage issues, and integrate Bootstrap/jQuery. 

## 10. Screenshots to add before submission
1. Home page, desktop
2. Movie search with filtered results
3. Bootstrap Movie Details Modal
4. Narrow viewport showing mobile navbar Collapse
5. Booking seat map and ticket total
6. Digital ticket/print preview
7. Admin booking/movie view
8. VS Code showing Bootstrap classes and jQuery handler

## 11. Conclusion
Starlight Cinemas demonstrates a multi-page interactive front-end using HTML5, CSS3, Bootstrap, JavaScript and jQuery. The main customer journey has been tested successfully by the student, while limitations (especially receiver-side e-gifts and lack of backend services) are documented openly.
