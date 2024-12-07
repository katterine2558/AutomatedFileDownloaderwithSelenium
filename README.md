🌐 Automated File Downloader with Selenium

This project contains Python scripts to automate file downloads from a website using Selenium. The automation can be performed in both automatic and manual modes, depending on user requirements. These scripts are specifically designed to interact with the Metro de Bogotá Data Room platform.

📂 Project Structure

    descargar_archivo.py
    Contains functions to identify download buttons, handle pagination, and manage file downloads.

    main_automatico.py
    Automates the login process and downloads files from predefined sections of the website.

    main_manual.py
    Allows the user to manually specify the download location and URL for downloading files.

🚀 Features

    Automated Downloads:
    Automatically finds and clicks download buttons on the webpage.

    Pagination Support:
    Handles pagination and downloads files across multiple pages.

    Subfolder Management:
    Creates and organizes downloaded files into subfolders based on webpage sections.

    Manual Download Option:
    Allows users to input custom download paths and URLs for more control.

📋 Prerequisites

    Python 3.x

    Dependencies:
    Install required libraries using pip:

    pip install selenium webdriver-manager beautifulsoup4

    Google Chrome
    Ensure Chrome is installed on your system.

    ChromeDriver
    webdriver_manager handles automatic installation of the appropriate ChromeDriver version.

⚙️ How to Use
1. Automatic Mode (main_automatico.py)

    Configure Login Credentials:
    Update the following lines with your login credentials:

input_usuario.send_keys("your-email@example.com")
password.send_keys("your-password")

Run the Script:

    python main_automatico.py

    The script will:
        Log in automatically.
        Navigate through predefined sections.
        Download files and organize them into folders.

2. Manual Mode (main_manual.py)

    Run the Script:

    python main_manual.py

    Provide User Inputs:
        Download Path: Specify where you want the files to be saved.
        URL: Enter the URL you want to download files from.

    The script will:
        Log in automatically.
        Open the specified URL.
        Download available files.

📄 Function Descriptions
descargar_archivo.py

    download_files(driver, carpeta_destino)
    Downloads files by detecting download buttons and handles pagination.

    crear_subcarpeta(ruta)
    Creates subfolders for organizing downloaded files.

    get_titulo_divs(divs)
    Extracts titles from webpage sections to name subfolders.

    esperar_descarga(carpeta_descargas)
    Waits until a download is complete before proceeding.

🛠️ Configuration

    Download Folder:
    Update carpeta_descargas in descargar_archivo.py with your download directory:

carpeta_descargas = "D:\\Descargas"

Chrome Options:
You can modify Chrome options in main_automatico.py and main_manual.py:

    options.add_argument("--start-maximized")

🔒 Security Note

    Credentials: Ensure login credentials are kept secure. Avoid hardcoding them in public repositories.
    File Paths: Adjust file paths to match your system configuration.

🤝 Contributing

Contributions are welcome! If you encounter any issues or have suggestions, please submit an issue or pull request.

📝 License

This project is licensed under the MIT License.
