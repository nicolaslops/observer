# OBSERVER

## About the Project

This project is an intelligent and reactive automation script focused on monitoring and dynamically managing files within the operating system. Developed in Python, the `watchdogs.py` script runs in the background, monitoring a specific input folder, typically the Downloads folder, and automatically organizing any new files added to it.

Unlike manually executed scripts, this application implements a continuous **Observer pattern**. As soon as a new download is completed and the file is detected in the monitored directory, the program identifies its extension and immediately transfers it asynchronously to a properly structured destination folder organized by category.

---

## Features

* Continuous real-time monitoring of a target directory, such as the Downloads folder.
* Instant detection of file creation or modification events.
* Automated file classification based on file extensions.
* Immediate transfer and relocation of files into dedicated subfolders, keeping the environment organized without manual intervention.

---

## Technologies Used

* **Python 3**
* Main external library: `watchdog` (used by the `watchdogs.py` monitoring script)
* Native auxiliary libraries: `os`, `shutil`, `time`

---

## Objective

The main objective of this project is to create a **"Zero-Click"** workflow for automatically organizing frequently changing directories. The technical focus is on event-driven programming within the operating system, using active monitoring loops and event handlers to react to real-time file system I/O changes.

---

## Learning Outcomes

During the development of this project, the following concepts were applied:

* Using the `watchdog` library to instantiate an `Observer` and associate it with a file system event handler (`FileSystemEventHandler`).
* Capturing and handling the specific `on_created` event to trigger automated actions when a new file is detected.
* Implementing temporary delays or exception handling to prevent files from being manipulated while they are still being written to disk by the browser.
* Integrating advanced functionality from the native `os` and `shutil` modules to rename, move, and validate destination paths.

---

## How to Run

1. Make sure Python is installed on your machine.
2. Install the required library using the terminal:

```bash
pip install watchdog
```

3. Navigate to the project folder:

```bash
cd OBSERVER
```

4. Run the script to start background monitoring:

```bash
python watchdogs.py
```

---

## Project Structure

```text
OBSERVER/
│
├── watchdogs.py
└── README.md
```

---

## License

This project was developed exclusively for educational and learning purposes.

Developed as an advanced hands-on exercise in local infrastructure automation and system event handling with Python, creating an intelligent automated file-sorting workflow for download directories.
