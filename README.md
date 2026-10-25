# 🏆 SportsHub

### Multi-Sport Management and Facility Booking Platform

SportsHub is a **multi-sport management platform** designed to bring players, teams, sports facilities, tournaments, matches, and live scoring into one centralized system.

The platform supports multiple sports and provides features such as **team management, opponent discovery, tournament management, facility booking, match management, live scoring, player statistics, notifications, and reviews**.

---

## 🎯 Project Objective

The main objective of SportsHub is to provide a single platform where users can:

- Create and manage sports teams
- Find nearby teams and potential opponents
- Organize and participate in matches
- Discover nearby sports facilities
- Book grounds, turfs, and courts
- Create and manage tournaments
- Record live match events and scores
- Maintain player statistics and leaderboards
- Receive match and booking notifications
- Review sports facilities

The system is designed to support both **local sports communities** and organized tournaments.

---

## 🏅 Supported Sports

SportsHub is designed to support:

- 🏏 Cricket
- ⚽ Football
- 🏀 Basketball
- 🏸 Badminton
- 🎾 Tennis
- 🏐 Volleyball

The database is designed so that additional sports can be added in the future without redesigning the entire system.

---

## 👥 User Roles

SportsHub supports different types of users.

### 👤 Viewer

A viewer can:

- View live scores
- View matches
- View teams and players
- View tournaments
- View player statistics
- Find nearby facilities

### 🏃 Player / Team User

A player can:

- Create teams
- Join teams
- Manage team members
- Search for nearby opponent teams
- Send and receive match requests
- Participate in matches
- Manage authorized live scoring
- View player statistics and leaderboards
- Book sports facilities

A player can create teams for different supported sports.

### 🏟️ Facility / Tournament Owner

An owner can:

- Register sports facilities
- Add facility details and pricing
- Manage facility availability
- Manage bookings
- Create tournaments
- Manage tournament information
- View facility-related activities

### 🔐 Admin

The administrator manages and monitors the platform, including:

- Users
- Teams
- Facilities
- Tournaments
- Matches
- Notifications
- Reviews
- Data validation and moderation

---

# 🗺️ Find Opponent

One of the key features of SportsHub is **Find Opponent**.

For example, if a cricket team wants to play a match on the weekend but does not have an opponent, they can search for nearby teams.

### Flow

```text
Select Team
     ↓
Select Sport
     ↓
Choose Preferred Date / Time
     ↓
Use Current Location
     ↓
Find Nearby Teams
     ↓
Send Match Request
     ↓
Opponent Accepts / Rejects
     ↓
Match Created
```

This feature helps local teams discover and connect with other teams.

---

# 🏟️ Facility Booking

SportsHub allows users to discover and book nearby sports facilities.

Examples:

| Sport | Facility |
|---|---|
| Cricket | Ground / Box Cricket |
| Football | Turf |
| Basketball | Basketball Court |
| Badminton | Badminton Court |
| Tennis | Tennis Court |
| Volleyball | Volleyball Court |

Users can view facility details, pricing, availability, and booking information.

---

# 🏆 Tournament Management

Tournament owners can create tournaments by providing information such as:

- Tournament name
- Sport
- Location
- Tournament date
- Registration fee
- Maximum teams
- Tournament status

Teams can then participate in available tournaments.

---

# 📊 Live Match Management

SportsHub supports match event recording for different sports.

### Cricket

The system can represent events such as:

- Runs
- Wides
- No-balls
- Byes
- Leg-byes
- Wickets

### Football

Examples include:

- Goals
- Own goals
- Yellow cards
- Red cards
- Substitutions

### Basketball

Examples include:

- 1-point score
- 2-point score
- 3-point score
- Fouls
- Timeouts

Other supported sports can use sport-specific match events as the project evolves.

---

# 📍 Location-Based Features

SportsHub uses location information to support nearby searches.

Users can discover:

- Nearby teams
- Nearby matches
- Nearby sports facilities
- Nearby tournaments

The database can store:

- City
- Latitude
- Longitude

Location-based calculations and map integration can be handled by the application layer.

---

# 🗄️ Database Design

The current project focuses on the **MySQL database layer**.

The database contains **13 core tables**:

| # | Table | Purpose |
|---|---|---|
| 1 | `users` | Stores user accounts and roles |
| 2 | `sports` | Stores supported sports |
| 3 | `player_profiles` | Stores player information |
| 4 | `teams` | Stores sports teams |
| 5 | `team_members` | Manages team membership |
| 6 | `facilities` | Stores grounds, turfs and courts |
| 7 | `tournaments` | Stores tournament information |
| 8 | `matches` | Stores match information |
| 9 | `bookings` | Manages facility bookings and payment information |
| 10 | `match_events` | Stores live match events |
| 11 | `player_statistics` | Stores player performance statistics |
| 12 | `notifications` | Stores user notifications |
| 13 | `reviews` | Stores facility reviews and ratings |

---

# 🔗 Database Features

The MySQL database includes:

### Tables
Stores the core SportsHub data and relationships.

### Primary Keys & Foreign Keys
Maintain entity identity and relationships between tables.

### Constraints
Help maintain valid and consistent data.

### Indexes
Improve query performance for commonly searched fields such as:

- Users by role and city
- Teams by sport and city
- Facilities by sport and city
- Matches by sport and date
- Bookings by facility and date
- Match events by match

### Views

The project includes reusable database views for commonly required information, including:

- Active teams
- Approved facilities
- Match listings
- Player leaderboards

### Stored Procedures

Stored procedures are used for reusable database operations such as:

- Finding nearby facilities
- Finding nearby opponent teams
- Retrieving match scores

### Triggers

Triggers provide automatic validation for important database operations, including:

- Review rating validation
- Match validation
- Booking time validation
- Match event validation

---

# 🧩 Entity Relationship Diagram

The ER diagram represents the major entities and relationships in the SportsHub database.

### Main relationships include:

```text
SPORTS
   ↓
TEAMS
   ↓
TEAM_MEMBERS
   ↓
USERS

SPORTS
   ↓
TOURNAMENTS
   ↓
MATCHES
   ↓
MATCH_EVENTS

USERS
   ↓
FACILITIES
   ↓
BOOKINGS
   ↓
REVIEWS

PLAYER_PROFILES
   ↓
PLAYER_STATISTICS

USERS
   ↓
NOTIFICATIONS
```

The complete ER diagram is available in the repository as:

**`SportsHub Multi-Sport ER Diagram.png`**

---

# 🛠️ Current Technology

### Database

- **MySQL**
- MySQL Workbench

### Planned Application Stack

```text
React
   ↓
REST API
   ↓
Flask
   ↓
Python
   ↓
MySQL
```

### Frontend

- React
- HTML
- CSS
- Bootstrap
- JavaScript

### Backend

- Python
- Flask
- REST API

---

# 📁 Project Files

```text
SportsHub/
│
├── sportsHub.txt
│
├── SportsHub Multi-Sport ER Diagram.png
│
└── README.md
```

### `sportsHub.txt`

Contains the complete MySQL database implementation, including:

- Database creation
- Table creation
- Sample data
- Indexes
- Views
- Stored procedures
- Triggers

### `SportsHub Multi-Sport ER Diagram.png`

Contains the Entity Relationship Diagram representing the database structure.

---

# 🚀 Future Development

The project will be developed progressively.

### Phase 1 — Database ✅

- Database design
- ER diagram
- Tables
- Relationships
- Sample data
- Indexes
- Views
- Stored procedures
- Triggers

### Phase 2 — Python Backend

- MySQL connectivity
- Business logic
- Data access layer

### Phase 3 — Flask REST API

- Authentication
- User APIs
- Team APIs
- Match APIs
- Tournament APIs
- Facility APIs
- Booking APIs
- Scoring APIs

### Phase 4 — Frontend

- React application
- User dashboard
- Team management
- Match management
- Facility search
- Booking interface
- Tournament interface
- Live scoring interface

### Phase 5 — Full-Stack Integration

```text
React Frontend
       ↓
Flask REST API
       ↓
Python Business Logic
       ↓
MySQL Database
```

---

# 🔒 Data & Security

The application will implement appropriate security practices such as:

- Password hashing
- Authentication
- Role-based authorization
- Input validation
- Secure API access

Sensitive payment information such as **card numbers, CVV, or UPI PINs will not be stored in the database**.

---

# 📌 Project Status

**Current Stage: MySQL Database Development**

The database schema, ER diagram, sample data, indexes, views, stored procedures, and triggers have been designed as the foundation of the SportsHub application.

Further development will extend the database into a complete **Python + Flask REST API + React full-stack application**.

---

## 👨‍💻 Developer

**B. NIKHIL**

**Batch:** PFS-VSP-007

**Project:** SportsHub — Multi-Sport Management and Facility Booking Platform

---

## ⭐ Project Vision

> **SportsHub aims to connect players, teams, facilities, tournaments, and matches through one unified multi-sport platform.**
