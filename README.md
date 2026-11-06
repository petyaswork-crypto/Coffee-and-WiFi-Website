# ☕ Cafe Finder - Coffee-and-WiFi 

Hello to all the coffee lovers! This platform that I am about to walk you through is for all of you that are always wondering
which café would be most comfortable for working since staying at home all day can be a little depressing.


## 🎯 About 

This app solves the problem above by letting users browse a curated list of cafes and contribute their own finds — 
each entry rated on Wi-Fi reliability, power outlet access, and coffee quality. 
It's a small project with a clear purpose: help people find places where they can actually get work done.


## ✨ Features

- Browse cafés — view a list of cafés with ratings for WiFi, power sockets, and coffee

- Add new entries — contribute a café via a validated form

- Server-side validation — form data is checked with Flask-WTF and WTForms before it's accepted

- Persistent storage — cafe data is stored in a CSV file

- Aestetically pleasing design — Bootstrap frontend built


## ⚙️ How It Works

1. The app loads cafe data from a CSV file on startup

2. Users browse the list, rendered dynamically with Jinja templating

3. The "Add a Cafe" form is validated server-side with WTForms — required fields, correct formats, sensible values

4. Valid submissions are appended to the CSV file and appear in the list immediately

Design note: I intentionally chose CSV over database. The app is read-heavy with occasional writes, 
and the dataset is small — a full database would have added complexity without benefit. 
Validation lives at the form boundary so bad data never reaches storage.


## 🚀 Getting Started

To run this project locally, you'll need Python 3.8 or higher and pip installed on your machine.

First, clone the repository from GitHub and navigate into the project folder. 
Then create a virtual environment to keep the project's dependencies isolated from your system Python — 
this avoids version conflicts with other projects. Activate the virtual environment: on macOS or Linux, 
you run the activation script from the bin folder; on Windows, you run the one from the Scripts folder.

Next, install the dependencies by running pip against the requirements.txt file included in the repository. 
This installs Flask, Flask-WTF, and WTForms.

Once everything is installed, start the app. If your project uses Flask's built-in command, 
run flask run from the terminal. If it has a main.py entry point, run python main.py instead. 
Either way, the app will start a local development server.

Finally, open your browser and go to http://127.0.0.1:5000 to view the app. 
To stop the server, press Ctrl+C in the terminal.

Hope this helps! 


## 📜 License

This project is free to use and modify for personal or
educational purposes. No warranty is provided.


## 🎓 Credits

Inspired by Day 62 of the course
"100 Days of Code: The Complete Python Pro Bootcamp".

The project idea, structure, and learning path came from the course.
The code in this repository was written by me as I followed along,
and I have added my own comments and tweaks along the way.


P.S. May your WiFi be strong, your coffee be bold, and every socket be free!
