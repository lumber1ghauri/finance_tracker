Personal Finance Tracker

A Ruby on Rails-based web application to help users manage their personal finances by tracking incomes, expenses, and budgets. The system includes user authentication, transaction categorization, and a responsive UI using Rails views and Tailwind CSS.

Project Overview

The goal of this application is to help users:

Track income and expenses.

Categorize their financial transactions.

Set budgets and monitor financial goals.

Visualize data through a dashboard (planned).


The project is built using:

Ruby on Rails (v7+)

PostgreSQL

Tailwind CSS (via Rails)

Devise for user authentication


Completed Features

✅ User Authentication

Devise is configured and integrated.

User registration, login, logout, and password management fully functional.


✅ Models and Migrations

Models created: User, Category, Transaction, Expense, Income, Budget

All migrations for these models are completed and functioning.

Associations such as belongs_to and has_many are set correctly.


✅ Controllers & Basic CRUD

TransactionsController fully set up:

index, show, new, edit, create, update, destroy actions.

Validations added in model for amount, date, and category presence.


CategoriesController, IncomesController, and ExpensesController also structured similarly.

Category and transaction forms are functional.


✅ Basic Views

Transactions views (index, form, show) are created and render properly.

Navigation structure is partially in place.

Flash messages implemented for create/update/destroy.


✅ Routing

All standard RESTful routes implemented.

Root path configured to welcome#index or dashboard#index (depending on state).


Pending / Upcoming Features

🟡 Budget Tracking Module

BudgetController actions are scaffolded but require logic implementation.

Need ability to set monthly/weekly budgets per category.


🟡 Dashboard View

Needs a proper dashboard view showing:

Monthly income vs expenses

Top categories

Budget usage

Planned graphs (maybe using Chartkick or similar)



🟡 Error Messages & Form Validation UI

Form error messages should be displayed cleanly in the views.

Currently backend validations exist, but no frontend UX polish yet.


🟡 User-based Data Filtering

Currently all transactions/incomes/expenses are global.

Need to scope models and controllers so users only see their own data.


🟡 Visual Improvements

Integrate proper layout using Tailwind CSS.

Add icons, better spacing, mobile responsiveness, etc.


🟡 Testing (RSpec or Minitest)

No automated tests added yet.


Getting Started

1. Clone the repo: git clone https://github.com/yourusername/finance_tracker.git


2. Install dependencies: bundle install


3. Set up the database: bin/rails db:drop db:create db:migrate


4. Start the server: bin/rails server


5. Access it at: http://localhost:3000



Notes

If you run into permission errors with bin/rails, try: chmod +x bin/rails

If db:migrate throws duplicate table errors, use db:drop before re-running.
