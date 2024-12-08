* * * * *

Vite React Setup Automation
===========================

This script automates the process of creating a Vite React app with a single command. It performs the following tasks:

-   Creates a new Vite React app.
-   Installs the necessary dependencies.
-   Starts the development server.
-   Opens the project in VS Code.

This guide includes setup instructions for **macOS** and **Linux**.

* * * * *

Prerequisites
-------------

-   **Node.js**: Make sure Node.js is installed. You can verify by running:

    bash

    Copy code

    `node -v
    npm -v`

    If not installed, you can download it from [Node.js official website](https://nodejs.org/) or use a package manager like `brew` (macOS) or `apt` (Linux).

-   **npm**: The script uses npm to install dependencies, so make sure it is installed as part of Node.js.

-   **VS Code**: The script opens the project in VS Code, so you need to have VS Code installed and the `code` command available in your terminal.

* * * * *

Setup Instructions
------------------

### **macOS**

1.  **Create the Script**

    -   Open your terminal and create the script:

        bash

        Copy code

        `nano ~/vite-react.sh`

2.  **Add the Script Content** Copy and paste the following script:

    bash

    Copy code

    `#!/bin/bash

    # Check if the project name is provided
    if [ -z "$1" ]; then
      echo "Usage: vite-react <project-name>"
      exit 1
    fi

    # Create the Vite React project (with the react template directly specified)
    npm create vite@latest $1 --template react --no-interactive

    # Navigate into the project directory
    cd $1

    # Install dependencies
    npm install

    # Start the development server in the background
    npm run dev &

    # Open the project in VS Code
    code .`

3.  **Make the Script Executable**

    bash

    Copy code

    `chmod +x ~/vite-react.sh`

4.  **Move the Script to a Directory in PATH**

    bash

    Copy code

    `sudo mv ~/vite-react.sh /usr/local/bin/vite-react`

5.  **Ensure VS Code is Installed**

    -   To install VS Code, you can use `brew`:

        bash

        Copy code

        `brew install --cask visual-studio-code`

### **Linux**

1.  **Create the Script**

    -   Open your terminal and create the script:

        bash

        Copy code

        `nano ~/vite-react.sh`

2.  **Add the Script Content** Copy and paste the same script:

    bash

    Copy code

    `#!/bin/bash

    # Check if the project name is provided
    if [ -z "$1" ]; then
      echo "Usage: vite-react <project-name>"
      exit 1
    fi

    # Create the Vite React project (with the react template directly specified)
    npm create vite@latest $1 --template react --no-interactive

    # Navigate into the project directory
    cd $1

    # Install dependencies
    npm install

    # Start the development server in the background
    npm run dev &

    # Open the project in VS Code
    code .`

3.  **Make the Script Executable**

    bash

    Copy code

    `chmod +x ~/vite-react.sh`

4.  **Move the Script to a Directory in PATH**

    bash

    Copy code

    `sudo mv ~/vite-react.sh /usr/local/bin/vite-react`

5.  **Ensure VS Code is Installed**

    -   For Ubuntu/Debian:

        bash

        Copy code

        `sudo apt install code`

    -   For Fedora:

        bash

        Copy code

        `sudo dnf install code`

* * * * *

Usage
-----

After following the setup steps, you can use the script to create a new Vite React app by running the following command:

bash

Copy code

`vite-react <project-name>`

Replace `<project-name>` with the name of your new project. For example:

bash

Copy code

`vite-react my-awesome-app`

This command will:

1.  Create the Vite React project using the React template.
2.  Install the necessary dependencies.
3.  Start the development server.
4.  Open the project in VS Code.

* * * * *

Troubleshooting
---------------

-   If you encounter any issues with VS Code not opening, make sure the `code` command is available in your terminal. You can verify this by running:

    bash

    Copy code

    `code --version`

    If it's not available, follow the [installation instructions](https://code.visualstudio.com/docs/setup/setup-overview).

-   If the script fails, make sure you have `npm` and `Node.js` properly installed, and check if there are any permission issues with the script.

* * * * *

Conclusion
----------

This script simplifies the process of setting up a new Vite React project. It automates multiple steps, saving you time and making the process more streamlined.

Happy coding! 🎉

* * * * *

Now, you can share this README for others to follow the steps to automate Vite React setup on **macOS** and **Linux**!
