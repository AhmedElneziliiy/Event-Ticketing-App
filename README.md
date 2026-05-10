# Event Ticketing App

An **ASP.NET Core MVC web application** for browsing and booking cinema event tickets — with a shopping cart, checkout, and user authentication.

## What it does

Users can browse movies, actors, cinemas, and producers. Authenticated users can add event tickets to a shopping cart and place orders. Admin users manage all catalog data through the same interface.

## Tech Stack

- **ASP.NET Core MVC** (.NET) — server-rendered Razor views
- **Entity Framework Core** — Code-First with SQL Server
- **ASP.NET Identity** — authentication and role-based access
- **Repository Pattern + Service Layer**

## Key Features

- Movie catalog with actors, cinemas, producers, and categories
- Many-to-many relationships (movies ↔ actors, movies ↔ producers)
- Shopping cart backed by session storage
- Order creation and order history per user
- Role-based authorization (Admin vs. User)
- Database seeder for initial catalog data

## Controllers

| Controller | Responsibility |
|---|---|
| `MoviesController` | Browse, create, and manage movies |
| `ActorsController` | Manage actor profiles |
| `CinemasController` | Manage cinema venues |
| `ProducersController` | Manage producers |
| `OrdersController` | Shopping cart and order placement |
| `AccountController` | Registration, login, logout |

## Getting Started

1. Set your connection string in `appsettings.json`.
2. Apply migrations:
   ```bash
   dotnet ef database update
   ```
3. Run the app:
   ```bash
   dotnet run --project E-ticket
   ```
