# Linux Malware Development Project

This repository contains scripts and tools for developing a basic backdoor for educational purposes. The project demonstrates how to create a simple backdoor in Python and convert it into an executable file using PyInstaller.

## Features

- **Backdoor Script**: The main backdoor functionality implemented in `backdoor.py`.
- **Listener Script**: A listener script (`listener.py`) that waits for incoming connections from the backdoor.
- **Executable Conversion**: Instructions to convert the `backdoor.py` script into an executable file.

## Prerequisites

- Python 3.x
- `pip` (Python package installer)
- PyInstaller

## Setup Instructions

### 1. Convert `backdoor.py` to an Executable File

Follow these steps to convert the `backdoor.py` script into an executable file using PyInstaller:

1. Install PyInstaller:
   ```sh
   pip install pyinstaller
   ```

2. Convert the script to an executable:
   ```sh
   pyinstaller --onefile backdoor.py
   ```

3. Navigate to the `dist` directory to find the executable file:
   ```sh
   cd dist
   ```

### 2. Transfer Executable to Victim Machine

Copy the executable file (`backdoor`) to the target Linux machine. You can use various methods like SCP, USB, or any other file transfer method suitable for your environment.

### 3. Run the Listener on Attacker Machine

On your attacking machine, run the `listener.py` script to start listening for incoming connections:
```sh
python listener.py
```

### 4. Run the Backdoor on Victim Machine

On the victim machine, execute the backdoor:
```sh
./backdoor
```

### 5. Establish Connection

Once the backdoor is running on the victim machine, return to your attacking machine where the `listener.py` script is running. You should see a notification indicating that a connection has been established.

## Repository Structure

- `backdoor.py`: The Python script implementing the backdoor.
- `listener.py`: The Python script acting as a listener on the attacker machine.
- `README.md`: This README file.

## Disclaimer

This project is intended for educational purposes only. Unauthorized use of these scripts is illegal and unethical. Always ensure you have explicit permission before deploying any form of backdoor or malware.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or bug fixes.

---

**Note**: Always use such tools responsibly and within legal boundaries. This repository is meant to provide educational insights into malware development for security professionals and researchers. Misuse of these scripts can lead to serious legal consequences.
