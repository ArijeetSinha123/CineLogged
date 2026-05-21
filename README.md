# CineLogged 🎬

A social tracking platform featuring an intuitive, modern UI and a deep media database.

## Our Goal
Combining the social, diary-like feel of Letterboxd with a broader database that covers both movies and TV shows (like IMDb), all wrapped in a cleaner, more intuitive user interface. Many users frequently express frustration that Letterboxd lacks TV shows (or handles them poorly) and that IMDb lacks a modern, community-driven social aspect. **CineLogged is the solution.**


## 🛠️ Tech Stack & Languages

- **Backend:** JavaScript (Node.js & Express.js)
- **Frontend :** HTML5 / EJS (Embedded JavaScript Templates)
- **Styling:** CSS3 (Custom Minimalist Layouts)
- **Database:** SQL (PostgreSQL or MySQL)
- **External Data:** TMDb API (The Movie Database) for seamless Movie & TV show data fetching <br>


## 📁 Project Structure

```text
CineLogged/
│
├── server.js                        ← Entry point / Starts the Node.js server 
│
├── view/                           ← View layer - Dynamic HTML templates (EJS)
│   ├── index.ejs                    ← Landing page / Public landing layout
│   ├── home.ejs                     ← Main dashboard (Social feed of friend activity)
│   ├── login.ejs                    ← User login page
│   ├── register.ejs                 ← User registration page
│   ├── movie-details.ejs            ← Individual movie/show page with logs & ratings
│   ├── profile.ejs                  ← User profile page (Shows user's logs, lists, followers)
│   ├── search-results.ejs           ← Dynamic movie, show, or user search results page
│   │
│   └── partials/                    ← Reusable UI elements (Keeps interface clean)
│       ├── navbar.ejs               ← Streamlined navigation header
│       ├── footer.ejs               ← Standard page footer
│       └── movie-card.ejs           ← Reusable movie poster card UI component
│
├── assets/                          ← Static asset files
│   ├── css/
│   │   └── style.css                ← Main stylesheet for your easier, minimalist UI
│   ├── js/
│   │   └── client.js                ← Frontend JavaScript (Handles ratings modals, async clicks)
│   └── images/
│
├── src/                             ← Backend JavaScript source code
│   ├── controllers/                 # Express route handlers
│   │   ├── authController.js        ← Handles user signup, login, and sessions
│   │   ├── movieController.js       ← Handles search queries and media page construction
│   │   ├── socialController.js      ← Handles follow/unfollow logic and activity feeds
│   │   └── logController.js         ← Handles one-click rating, logging, and reviews
│   │
│   ├── models/                      # Database interface logic
│   │   ├── userModel.js             ← User database CRUD (Profiles, authentication data)
│   │   ├── logModel.js              ← Log database CRUD (Ratings, written reviews, watch dates)
│   │   └── socialModel.js           ← Social mapping (Followers, followings, network activity)
│   │
│   ├── services/                    # Third-party integrations
│   │   └── tmdbService.js           ← Core logic to query the TMDb API for movie & show metadata
│   │
│   └── utils/
│       └── db.js                    ← Database connection instance (PostgreSQL or MySQL client)
│
├── database/
│   └── schema.sql                   ← Tables configuration (Users, Logs, Follows relationships)
│
├── .env                             ← Sensitive environment keys (PORT, DATABASE_URL, TMDB_API_KEY)
├── .gitignore                       ← Instructs Git to ignore node_modules/ and the .env file
├── package.json                     ← Project dependencies configuration (Express, EJS, DB drivers)
└── README.md                        ← Project roadmap, UI guidelines, and local setup steps
```
<br>

# 👥 Authors & Contributors
### Arijeet Sinha, Anurag Chakraborty & Rahul Sen <br><br>


**NOTE - For a seamless coding experience, please ensure your local .vscode/ workspace configurations and structural .gitignore boundaries match the official project workflow instructions before submitting Pull Requests.**
