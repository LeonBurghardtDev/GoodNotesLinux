# GoodNotes on Linux

This project provides a simple Electron wrapper for the GoodNotes web application, allowing you to use it as a standalone desktop application on Linux, particularly on Arch-based systems.

## Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/LeonBurghardtDev/GoodNotesLinux.git
    cd GoodNotesWeb
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Package the application:**

    ```bash
    npm run package
    ```

## Running the Application

After packaging, you can run the application from the `dist/GoodNotesWeb-linux-x64` directory:

```bash
./dist/GoodNotesWeb-linux-x64/GoodNotesWeb
```

## Desktop Integration

To add GoodNotes to your application launcher, you can create a `.desktop` file.

1.  **Create the file:**

    Create a file named `GoodNotes.desktop` with the following content:

    ```ini
    [Desktop Entry]
    Name=GoodNotes
    Exec=/path/to/your/project/GoodNotesWeb/dist/GoodNotesWeb-linux-x64/GoodNotesWeb
    Icon=/path/to/your/project/GoodNotesWeb/icon.png
    Type=Application
    Categories=Office;
    ```

    **Important:** Replace `/path/to/your/project` with the actual absolute path to the `GoodNotesWeb` directory.

2.  **Install the desktop file:**

    Move the `GoodNotes.desktop` file to `~/.local/share/applications/`:

    ```bash
    mv GoodNotes.desktop ~/.local/share/applications/
    ```

3.  **Install the icon:**

    Copy the icon to the icons directory:

    ```bash
    mkdir -p ~/.local/share/icons/hicolor/48x48/apps/
    cp icon.png ~/.local/share/icons/hicolor/48x48/apps/GoodNotes.png
    ```

After these steps, you should be able to find and launch GoodNotes from your application menu.
