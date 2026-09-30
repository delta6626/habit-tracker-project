# Habit Tracker

A command line habit tracking application built with Python. The application allows users to create, manage, and analyse personal habits with daily or weekly periodicity.

### Features

* Create, complete, and delete habits
* Daily and weekly habit tracking
* View habit details and group habits by periodicity
* Track completion streaks
* Analyse the longest streaks across all or specific habits
* Persistent storage using SQLite
* Predefined demo data with four weeks of example tracking data
* Unit tests for core habit behaviour and analytics

## Requirements

* Python 3.13 is preferred. Python 3.10 or later should work fine.
* No external dependencies are required.

## Setup

Clone the repository and open the project folder:

```bash
git clone https://github.com/delta6626/habit-tracker-project
cd habit-tracker-project
```

No additional packages or setup are required because the application uses only Python's standard library.

## Running the Application

Run the application from the project root:

```bash
python main.py
```

The application opens the command line menu, where users can create, complete, delete, and analyse habits.

## Demo Data

On the first run, the application automatically loads the predefined demo habits with four weeks of example tracking data.

This data is used for testing purposes and also gives new users something to interact with. It can be deleted or modified through the CLI like any other habit.

If the demo data has been deleted or modified and you want to restore it to its original state, open `config.json` and set the `demo_data_loaded` flag to `false`:

```json
{"demo_data_loaded": false}
```

The original demo data will then be loaded the next time the application is started.

## Running the Tests

**Important:** Run the unit tests from the project root to ensure there are no import errors.

```bash
python -m unittest ./tests/test_habit.py ./tests/test_analytics.py
```

The tests cover core habit behaviour, period calculations, completion tracking, and the analytical functions.
