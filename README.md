# Habit Tracker

A command line habit tracking application built with Python. The application allows users to create, manage, and analyze personal habits with daily or weekly periodicity.

## Features

* Create, complete, and delete habits
* Daily and weekly habit tracking
* View habit details and group habits by periodicity
* Track completion streaks
* Analyze the longest streaks across all or specific habits
* Persistent storage using SQLite
* Predefined demo data with four weeks of example tracking data
* Unit tests for core habit behaviour and analytics

## Requirements

* Python 3.13 is preferred. Python 3.10 or later should work fine
* No external dependencies are required

## Setup

Clone the repository and open the project folder:

```
git clone https://github.com/delta6626/habit-tracker-project
cd habit-tracker-project
```

No additional packages or setup are required because the application uses only Python's standard library.

## Running the Application

Run the application from the project root:

```
python main.py
```

The application opens the command line menu, where users can create, complete, delete, and analyze habits.

## Usage

Enter the number of an action from the main menu:

| Option | Action |
| ------ | ------ |
| 1 | Add a new habit |
| 2 | Complete (check off) a habit |
| 3 | Delete a habit |
| 4 | View analytics |
| 5 | Show the menu again |
| 6 | Exit |

**Creating a habit:** choose `1`, then enter a name, an optional description, and a periodicity (`daily` or `weekly`).

**Completing a habit:** choose `2`, then enter the number of the habit from the displayed list. The current date and time is recorded as a completion. A habit can be completed at any point in time.

**Deleting a habit:** choose `3`, then enter the number of the habit. Its completion history is deleted along with it.

**Analytics:** choose `4`, then pick one of the following:

1. View all habits
2. View a habit in detail
3. View habits grouped by periodicity
4. View the longest streak overall
5. View the longest streak for a specific habit

A streak is the number of consecutive periods (days or weeks) in which a habit was completed at least once.

## Demo Data

On the first run, the application automatically loads five predefined habits with four weeks of example tracking data:

| Habit | Periodicity |
| ----- | ----------- |
| Drink water | Daily |
| Daily run | Daily |
| Daily meditation | Daily |
| Read a book | Weekly |
| Learn CS | Weekly |

This data is used for testing purposes and also gives new users something to interact with. It can be deleted or modified through the CLI like any other habit.

If the demo data has been deleted or modified and you want to restore it to its original state, open `config.json` and set the `demo_data_loaded` flag to `false`:

```
{"demo_data_loaded": false}
```

The original demo data will then be loaded the next time the application is started.

## Running the Tests

**Important:** Run the unit tests from the project root to ensure there are no import errors.

```
python -m unittest ./tests/test_habit.py ./tests/test_analytics.py
```

The tests cover core habit behaviour, period calculations, completion tracking, and the analytical functions.
