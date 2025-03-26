# PyQt5 Application with Splash Screen

## Overview
This project is a PyQt5-based GUI application that displays a splash screen before navigating to either a setup window or a login window. The decision is based on the existence of a `config.json` file.

## Features
- Displays a splash screen (`slash_img.jpg`) on startup.
- If `config.json` exists, the application opens the login window.
- If `config.json` does not exist, the application opens the setup window.

## Requirements
- Python 3.x
- PyQt5
- MySQL (if used within `InstallWindow` or `LoginScreen`)

## Installation
1. Clone or download the repository.
2. Install dependencies using pip:
   ```sh
   pip install PyQt5 mysql-connector-python
   ```
3. Ensure `slash_img.jpg` is present in the same directory.

## Usage
Run the main script using:
```sh
python main.py
```

## File Structure
```
.
├── main.py  # Main entry point of the application
├── InstallWindow.py  # Contains InstallWindow class
├── LoginWindow.py  # Contains LoginScreen class
├── config.json  # (Optional) Determines whether to show login or setup window
├── slash_img.jpg  # Image used for the splash screen
```

## How It Works
1. The application starts with a splash screen.
2. After 3 seconds, it checks for the existence of `config.json`:
   - If `config.json` exists, it shows the login window.
   - Otherwise, it shows the setup window.
3. The app runs using `QApplication.exec_()` until manually closed.

## Notes
- Ensure `config.json` is correctly formatted if used.
- Modify `slash_img.jpg` to change the splash screen appearance.

## License
This project is open-source under the MIT License.

