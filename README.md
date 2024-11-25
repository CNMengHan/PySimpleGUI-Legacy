# PySimpleGUI-Legacy

This repository provides a functional, pre-license version of the **PySimpleGUI** library for developers who need a free and unrestricted solution. The official PySimpleGUI library has recently transitioned to a paid license model, leaving many developers unable to access or use the library. This backup allows you to continue using the legacy version without any license requirements.

---

## What is PySimpleGUI?

**PySimpleGUI** is a Python library that simplifies the process of creating graphical user interfaces (GUIs). It abstracts away the complexity of underlying frameworks like Tkinter, Qt, WxPython, and Remi, offering a beginner-friendly, high-level API. With PySimpleGUI, you can build interactive desktop applications, file explorers, progress trackers, and more with minimal code.

### Key Features of PySimpleGUI:
- **Beginner-Friendly**: Intuitive syntax, ideal for developers new to GUIs.
- **Rich Component Library**: Buttons, text inputs, sliders, progress bars, tables, and more.
- **Cross-Platform**: Runs seamlessly on Windows, macOS, and Linux.
- **Dynamic Updates**: Allows real-time updates to GUI elements during execution.
- **Integration Ready**: Supports Matplotlib, OpenCV, and other libraries for advanced functionality.

---

## What is PySimpleGUI Used For?

PySimpleGUI is widely used in:
- **Educational Projects**: Helping beginners learn GUI development.
- **Data Visualization**: Embedding interactive charts and graphs.
- **Automation Tools**: Creating simple automation utilities with user interfaces.
- **Prototyping**: Quickly designing and testing application interfaces.
- **Lightweight Desktop Apps**: Developing small-scale tools with a minimal footprint.

---

## Why Use an Older Version of PySimpleGUI?

On **[specific date of license change]**, the creator of PySimpleGUI announced a transition to a paid license model. As part of this change:
1. **A license key is now required** to use any version installed via `pip`.
2. **Older, free versions of PySimpleGUI have been removed** from the PyPI repository, preventing developers from simply downgrading to a previous version.
3. Developers who rely on PySimpleGUI for personal projects, open-source software, or educational purposes are now locked out unless they pay for a license.

This repository offers a solution by providing a backup of the last free and functional version of PySimpleGUI.

---

## Why Can't You Use `pip` to Downgrade PySimpleGUI?

Normally, developers can install a specific version of a library using `pip install PySimpleGUI==<version>`. However, with the recent changes:
1. **The author has removed older versions** from the PyPI repository, making downgrading impossible.
2. This forces developers to use the latest version, which now requires a paid license.

As a result, the only way to access a fully functional version is through a saved copy, such as the one provided in this repository.

---

## How to Use This Repository

### **1. Download the Legacy Version**

- **Download the `PySimpleGUI.7z` file** from the [Releases](https://github.com/CNMengHan/PySimpleGUI-Legacy/releases/tag/v4.60.4) section.

### **2. Extract the Files**

- Extract the `PySimpleGUI.7z` archive using any file extraction tool that supports the `.7z` format.

### **3. Locate Your Python `site-packages` Directory**

- **Windows Example:**
  ```
  C:\Users\Administrator\AppData\Local\Programs\Python\Python310\Lib\site-packages
  ```
- **macOS/Linux Example:**
  ```
  /usr/local/lib/python3.10/site-packages
  ```
  *(The exact path may vary depending on your Python installation.)*

### **4. Remove Existing PySimpleGUI Installations**

Before installing the legacy version, you need to remove any existing PySimpleGUI installations to prevent conflicts.

1. Navigate to your `site-packages` directory.
2. **Delete the following folders if they exist:**
   - `PySimpleGUI`
   - `PySimpleGUI-<version>.dist-info`
   
   *Example on Windows:*
   ```
   C:\Users\Administrator\AppData\Local\Programs\Python\Python310\Lib\site-packages\PySimpleGUI
   C:\Users\Administrator\AppData\Local\Programs\Python\Python310\Lib\site-packages\PySimpleGUI-4.60.1.dist-info
   ```

### **5. Install the Legacy PySimpleGUI**

1. **Copy the extracted `PySimpleGUI` folder and `PySimpleGUI-<version>.dist-info` folder** from the `.7z` archive.
2. **Paste these folders into your Python `site-packages` directory**.

   *Example on Windows:*
   ```
   C:\Users\Administrator\AppData\Local\Programs\Python\Python310\Lib\site-packages\PySimpleGUI
   C:\Users\Administrator\AppData\Local\Programs\Python\Python310\Lib\site-packages\PySimpleGUI-4.60.1.dist-info
   ```

### **6. Verify the Installation**

You can verify that the legacy version is installed correctly by running a simple PySimpleGUI script:

```python
import PySimpleGUI as sg

# Define the layout
layout = [
    [sg.Text("Enter your name:")],
    [sg.Input(key='-INPUT-')],
    [sg.Button("Submit"), sg.Button("Exit")]
]

# Create the window
window = sg.Window("PySimpleGUI Legacy Example", layout)

# Event loop
while True:
    event, values = window.read()
    if event == sg.WINDOW_CLOSED or event == "Exit":
        break
    if event == "Submit":
        sg.popup(f"Hello, {values['-INPUT-']}!")

# Close the window
window.close()
```

Run the script to ensure that the GUI appears and functions as expected.
