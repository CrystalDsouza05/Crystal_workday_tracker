# Workday

### A lightweight personal work-hours tracker

Workday is a simple browser-based tool I built for my own workday tracking.

I wanted an easier way to keep track of my check-in time, lunch break, remaining working hours, and expected checkout time without repeatedly doing the calculations myself.

The current version is intentionally small and is still an early-stage prototype.

## Why I built it

My office already has a check-in/check-out system, but I wanted a personal view of my workday while I was working.

The idea was simple:

**Check in → see the workday progress → track the break → get a reminder before leaving → check out.**

What started as a small personal productivity idea turned into a useful little web app.

## Features

- Check in and start the workday timer
- Real-time workday progress bar
- Displays expected checkout time
- Shows remaining working time
- Tracks a 45-minute lunch break
- Break progress bar and remaining break time
- Configurable reminders 5 or 10 minutes before break ends
- Configurable reminders 5 or 10 minutes before checkout
- Browser notification support where available
- In-app notifications as a fallback
- Edit check-in and break timings
- View a history of previous workdays
- Data is stored locally in the browser using `localStorage`
- Light and dark mode support based on browser/system preference

## Current workday setup

The current prototype uses:

- **9 hours 15 minutes** as the workday duration
- **45 minutes** as the lunch break duration
- **5 or 10 minutes** as the reminder window

These values are currently built into the application settings/logic rather than being a fully configurable work policy.

## How it works

The app is a single-page HTML application using vanilla HTML, CSS and JavaScript.

No backend is required.

When you check in, the application records the timestamp and calculates the expected end of the workday from that time. A timer updates the progress bar and remaining time every second.

Break tracking works in a similar way. Starting a break records the break-out time, while returning from the break records the break-in time.

Daily records are stored locally in the browser, so the application can show previous entries without requiring an account or database.

## Tech stack

- HTML
- CSS
- Vanilla JavaScript
- Browser Notifications API
- `localStorage`

## Running locally

There is no build process.

1. Clone the repository.
2. Open `index.html` in a modern browser.
3. Click **Check In** to start tracking.

For the best notification experience, browser notification permissions may need to be enabled.

## Project structure

```text
workday/
├── index.html
├── README.md
└── .gitignore
```

## Screenshots

Add screenshots of the application here once the repository is published.

For example:

```text
screenshots/
├── workday-dashboard.png
├── break-tracker.png
└── history-log.png
```

## What I learned

This project was less about building a complex application and more about turning a small personal problem into something usable.

A few things I explored while building it:

- Managing timestamps in JavaScript
- Calculating elapsed and remaining time
- Updating UI elements in real time
- Working with browser notifications
- Persisting data with `localStorage`
- Building a responsive interface without a framework
- Using ChatGPT as a coding partner while iterating on an idea

## Built with ChatGPT

I used ChatGPT as a coding partner during the development of this project.

Rather than treating it as a one-shot code generator, I used it to help translate the idea into a working prototype, work through implementation details, and iterate on the functionality.

The idea, requirements, testing and decisions around the tool were still driven by the problem I wanted to solve.

## Current limitations

This is an early prototype, so there are several things it does not attempt to solve yet:

- No user accounts
- No cloud/database storage
- No synchronization across devices
- No connection to an office attendance system
- No analytics dashboard
- No export to CSV/Excel
- Workday and break durations are not fully configurable
- Local browser storage means clearing browser data can remove the records

## Possible future improvements

Some ideas I may explore:

- Configurable working hours
- Multiple break periods
- Weekly/monthly work-hour summaries
- CSV/Excel export
- Better mobile experience
- PWA support
- Optional cloud synchronization
- Attendance analytics
- More flexible notification rules
- Custom themes

## Status

**Early prototype / v0.1**

Built primarily for personal use and experimentation.

---

If you find a small personal problem that keeps bothering you, sometimes the easiest way to understand the problem is to build a tiny solution for yourself.
