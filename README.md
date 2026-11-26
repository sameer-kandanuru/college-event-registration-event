# College Event Registration System

A college event system with a mobile-style app and a website. Students create an account, search events, and register. Staff sign in with a staff account to add events and see who has registered.

## Features

- Sign up and sign in with email or phone number and password
- Passwords are stored as PBKDF2 hashes, not plain text
- Forgot password: a one-time code is sent to the registered phone number
- Student dashboard: browse and search events, register, view and cancel your own registrations
- Staff dashboard: add events and view all registrations grouped by event
- Event categories, seat counts, and a duplicate roll-number check
- The app and website share the same accounts, events, and registrations

## Files

- `campus-events-app-login.html`: mobile-style app (one file: HTML, CSS, JavaScript)
- `campus-events-website-v2.html`: website (one file: HTML, CSS, JavaScript)

## Running it

The code uses the Claude artifact database (`window.claude.use('db')`). Accounts and registrations only load inside a Claude artifact page. Opening the files directly in a browser shows the sign-in screen with a "cannot reach accounts" message.

## Known limitations

This is a student project, not a production system.

- The one-time code is shown on screen (`SHOW_DEMO_OTP`) because no SMS service is connected.
- The staff access code (`STAFF_CODE`) is visible in the page source.
- Access rules are enforced in the browser, not on a server, so anyone with access to the database can read the data.

## Moving to a real deployment

- Build a Node.js and Express backend with MongoDB
- Check passwords and staff access on the server
- Send one-time codes through an SMS provider
- Replace the on-screen code with real delivery# college-event-registration-event
https://v.gd/1IjOAO