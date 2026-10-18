# Starlight Cinemas

**Dynamic Websites and Applications — Assignment 1**  
**Project:** Movie Night / Starlight Cinemas  
**Student:** Nikoi Cole  


## Project overview
Starlight Cinemas is a fictional Jamaican cinema website built as a **front-end classroom demonstration**. Visitors can browse movies and showtimes, explore sample cinema locations and prices, register/sign in to demo accounts, reserve sample seats, print digital tickets, and interact with an admin catalog. The black-and-gold interface adapts to different screen sizes.

## Technologies
- **HTML5:** separate pages and forms.
- **CSS3:** custom black-and-gold visual theme, responsive styling and animations.
- **Bootstrap 5.3.3:** responsive navigation/collapse, grid-based movie layouts, and movie-details modal.
- **JavaScript (ES6+):** catalog rendering, form handling, booking and seat selection, storage, Admin tools, and ticket views.
- **jQuery 3.7.1:** delegated movie search input listener and dynamic results updates.
- **Browser localStorage/sessionStorage:** demonstration data; **not secure production accounts or payments**.

## Running the project
1. Download/extract the complete project folder.
2. Open that folder in Visual Studio Code.
3. Launch **index.html** with the **Live Server** extension.
4. Keep an internet connection for Bootstrap, jQuery, QR renderer, fonts, and hosted images.

## Website pages
| File | Purpose |
|---|---|
| `index.html` | Landing page and highlights |
| `movies.html` | Search, browse, and see details/trailers |
| `schedule.html` | View sample showtimes |
| `booking.html` | Select ticket types and seats |
| `confirmation.html` | View/print ticket and receipt |
| `register.html`, `login.html` | Demo account registration and login |
| `profile.html` | Demo account details and transaction history |
| `gifts.html` | E-gift preview and experimental wallet |
| `retrieve.html` | Retrieve demo booking by reference |
| `admin.html` | Edit movies, showtimes, prices and view bookings |
| `cinemas.html`, `prices.html`, `events.html` | Other cinema information |

## Project structure
```
Starlight-Cinemas/
├── index.html, movies.html, schedule.html, booking.html, ...
├── css/styles.css
├── js/app.js
├── js/auth.js
├── js/gift-wallet.js
├── images/
├── README.md
└── docs/
```

## Demonstrated interactions
- Bootstrap **Collapse** controls the responsive navigation; Bootstrap **Modal** displays movie details.
- jQuery listens for typing in the movie search and updates the result list/count.
- JavaScript updates movie views, ticket quantities, available seats and booking history.
- Admin movie changes are saved **only in the current browser**. To display newly edited code defaults, use **Admin → Movies → Reset to Code Defaults**; this clears browser Admin movie overrides.

## Test status (user-reported, October 14, 2026)
**Reported working:** multiple viewport sizes, movie details, booking administration, movie search, registration, login, movie booking, booking display in profile, digital ticket generation and printing, sending/saving an e-gift in the sender profile.

**Known issue:** gifts **do not reliably appear in the recipient profile**. Treat receiving, claiming, and checkout redemption as experimental and **do not demonstrate them as proven**. Other error cases and accessibility behavior still require testing.

## Limitations / safety
- The website is a school demonstration, not a live business. Venues, schedules and prices are illustrative.
- Accounts, reservations, gift codes and balances are stored locally; there is no protected server database or cross-device synchronization.
- The Admin page is not access-controlled; no real payment or e-gift value is processed.
- Posters and other images may be sourced from third parties and must be reviewed for copyright and attribution before public use.

## Source code and documentation
See `docs/PROJECT_DOCUMENTATION.md` for implementation notes, the requirements map, testing evidence and planned improvements. See `docs/GITHUB_SUBMISSION_CHECKLIST.md` for hand-in steps.

## Academic integrity / AI disclosure
AI tools (ChatGPT) were used to help plan, draft, troubleshoot, and refactor parts of the website, including Bootstrap/jQuery integration and demo features. The student is responsible for reviewing, testing and understanding the final code and for following the lecturer's rules for acknowledgement. Describe any further assistance accurately before submission.

## GitHub repository
**Repository URL:** [PASTE YOUR REPOSITORY URL HERE AFTER UPLOADING]
