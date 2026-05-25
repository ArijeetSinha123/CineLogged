# CineLogged 🎬 - A Social Media Site For Cinephiles

A social tracking platform featuring an intuitive, modern UI and a deep media database.

## Our Goal
Combining the social, diary-like feel of Letterboxd with a broader database that covers both movies and TV shows (like IMDb), all wrapped in a cleaner, more intuitive user interface. Many users frequently express frustration that Letterboxd lacks TV shows (or handles them poorly) and that IMDb lacks a modern, community-driven social aspect. **CineLogged is the solution.**


## Tech Stack & Languages

- **Backend:** JavaScript (Node.js & Express.js)
- **Frontend :** HTML5 / EJS (Embedded JavaScript Templates)
- **Styling:** CSS3 (Custom Minimalist Layouts)
- **Database:** SQL (PostgreSQL or MySQL)
- **External Data:** TMDb API (The Movie Database) for seamless Movie & TV show data fetching <br>


## Project Structure

```text
CineLogged/
│
├── server.js                        ← Express app entry point (routes, middleware, session setup)
│
├── views/                           ← Server-rendered HTML templates (EJS)
│   ├── index.ejs                    ← Landing page (hero + search bar)
│   ├── home.ejs                     ← Personal dashboard (recent logs, trending from TMDB)
│   ├── login.ejs                    ← Login page
│   ├── register.ejs                 ← Registration page
│   ├── movie-details.ejs            ← Movie/show page (TMDB data + log/rate button)
│   ├── profile.ejs                  ← User profile (stats, log history, watchlist)
│   ├── search-results.ejs           ← Search results page (movies & shows)
│   ├── watchlist.ejs                ← Personal watchlist page
│   ├── log-history.ejs              ← Full paginated log history
│   │
│   └── partials/
│       ├── navbar.ejs               ← Navigation bar
│       ├── footer.ejs               ← Footer
│       └── movie-card.ejs           ← Reusable poster card component
│
├── public/                          ← Statically served files (Express static middleware)
│   ├── css/
│   │   └── style.css                ← Global stylesheet
│   ├── js/
│   │   └── client.js                ← Vanilla JS (rating modal, watchlist toggle, async fetch)
│   └── images/
│       └── logo.png                 ← App logo / placeholder assets
│
├── src/
│   ├── routes/                      ← Express route definitions (thin layer, calls controllers)
│   │   ├── authRoutes.js            ← /login  /register  /logout
│   │   ├── movieRoutes.js           ← /search  /movie/:id  /tv/:id
│   │   └── logRoutes.js             ← /log/add  /log/delete  /watchlist/toggle
│   │
│   ├── controllers/                 ← Route handler logic
│   │   ├── authController.js        ← Signup, login, logout, bcrypt, session
│   │   ├── movieController.js       ← TMDB fetch + render movie/search pages
│   │   └── logController.js         ← Add/edit/delete logs, watchlist CRUD
│   │
│   ├── models/                      ← Raw SQL query functions (no ORM)
│   │   ├── userModel.js             ← SELECT/INSERT/UPDATE on users table
│   │   └── logModel.js              ← SELECT/INSERT/DELETE on logs & watchlist tables
│   │
│   ├── services/
│   │   └── tmdbService.js           ← TMDB API wrapper (search, details, trending)
│   │
│   ├── middleware/
│   │   └── auth.js                  ← Session guard (redirects to /login if not authenticated)
│   │
│   └── utils/
│       └── db.js                    ← SQL connection pool (mysql2 or pg client)
│
├── database/
│   └── schema.sql                   ← CREATE TABLE statements for users, logs, watchlist
│
├── .env                             ← PORT, DB_HOST, DB_USER, DB_PASS, DB_NAME, TMDB_API_KEY, SESSION_SECRET
├── .gitignore                       ← node_modules/, .env
├── package.json                     ← express, ejs, mysql2/pg, bcrypt, express-session, dotenv
└── README.md                        ← Setup guide, env vars list, schema notes
```
<br>

## 👥 Authors & Contributors
### Arijeet Sinha, Anurag Chakraborty & Rahul Sen <br><br>


**NOTE - For a seamless coding experience, please ensure your local .vscode/ workspace configurations and structural .gitignore boundaries match the official project workflow instructions before submitting Pull Requests.**
