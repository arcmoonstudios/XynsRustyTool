# 🦀🚀 XynsTool: ArcMoon Studios' Trusty All-in-One Rusty Debugger+ Tool by Lord Xyn 🛠️

![LordXyn](https://tinypic.host/images/2024/09/30/LordXyn.jpeg)

Welcome to **XynsTool**, your ultimate companion for Rust development! Whether you're a seasoned Rustacean or just starting out, XynsTool offers a suite of powerful features to streamline your debugging, refactoring, and project management tasks. 🌟

## 📖 Table of Contents

- [🔍 Features](#-features)
- [💾 Installation](#-installation)
- [🛠️ Usage](#️-usage)
  - [Running All Tasks](#running-all-tasks)
  - [Saving Project State](#saving-project-state)
  - [Restoring Project State](#restoring-project-state)
  - [Toggle Overwrite Protection](#toggle-overwrite-protection)
  - [Manual Debugging](#manual-debugging)
- [⚙️ Configuration](#️-configuration)
- [🔄 Updating XynsTool](#-updating-xynstool)
- [🛡️ Security Considerations](#️-security-considerations)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [📞 Contact](#-contact)

## 🔍 Features

✨ **XynsTool** is packed with features to enhance your Rust development experience:

- **All-in-One Debugging** 🐞: Automate the process of analyzing and refactoring your Rust code.
- **Manual Debugging Option** 📝: Generate comprehensive error logs (`noXai.txt`) for manual or AI-assisted debugging.
- **State Management** 💽: Save and restore project states effortlessly.
- **Overwrite Protection** 🛡️: Safeguard your files with toggleable overwrite protection.
- **Automated Updates** 🔄: Keep XynsTool up-to-date with the latest features and security patches.
- **Detailed Logging** 📜: Maintain logs of all actions and errors for easy troubleshooting.
- **Secure Update Mechanism** 🔒: Verify updates using GPG signatures to ensure authenticity.

## 💾 Installation

Follow these steps to install **XynsTool** on your system:

1. **Clone the Repository** 🐙:
    
        git clone https://github.com/arcmoonstudios/XynsRustyTool.git
        cd XynsRustyTool

2. **Make the Script Executable** 🔧:
    
        chmod +x xynstool.sh

3. **Run the Installation Script** 🚀:
    
        ./xynstool.sh

4. **Verify Installation** ✅:
    Ensure that the `lx` command is available:
    
        lx help

## 🛠️ Usage

**XynsTool** utilizes the `lx` command to perform various tasks. Below are the primary commands and their functionalities:

### Running All Tasks

Execute all available tasks with automatic or manual approvals.

- **Automatic Approval** 🤖:
    
        lx all y

    *Runs all tasks without prompting for confirmations.*

- **Manual Approval** 🧑‍💻:
    
        lx all

    *Runs all tasks, asking for approval before each step.*

### Saving Project State

Save the current state of your project to enable easy restoration later.

    lx sv <save_name>

**Example**:
    
    lx sv initial_setup

*Creates a save point named `initial_setup`.*

### Restoring Project State

Restore your project to a previously saved state.

    lx rstrXX

**Example**:
    
    lx rstr01

*Restores the project to the state saved as `restore01`.*

### Toggle Overwrite Protection

Enable or disable overwrite protection to prevent accidental file overwrites.

- **Enable Overwrite Protection** 🛡️:
    
        lx ow on

- **Disable Overwrite Protection** 🔓:
    
        lx ow off

*When enabled, XynsTool will prompt before overwriting existing files.*

### Manual Debugging

Generate a comprehensive `noXai.txt` file for manual debugging or to use with external AI tools like ChatGPT, AskCodi, or Claude.

    lx manual

**What It Does**:
- Captures the project layout excluding the `target` directory.
- Builds the project and logs build outputs.
- Parses error and warning messages, injecting them into `noXai.txt` with context.
- Appends detailed refactoring instructions to assist in manual debugging or AI-assisted debugging.

**Output**:
- The `noXai.txt` file is located in the `mr_fixit` directory, ready for use.

## ⚙️ Configuration

Customize **XynsTool** to fit your development needs:

1. **Environment Variables** 🛠️:
    - The `.env` file is created automatically. Update it with your actual API keys for full functionality.
    - **Example**:
        
        HUGGING_FACE_API_KEY=your_hugging_face_api_key_here
        CLAUDE_API_KEY=your_claude_api_key_here
        OPENAI_API_KEY=your_openai_api_key_here
        GITHUB_API_TOKEN=your_github_api_token_here
        AWS_ACCESS_KEY_ID=your_aws_access_key_id_here
        AWS_SECRET_ACCESS_KEY=your_aws_secret_access_key_here

2. **Overwrite Protection** 🛡️:
    - Managed via `./mr_fixit/config.cfg`.
    - Toggle using `lx ow on/off`.

## 🔄 Updating XynsTool

Keep **XynsTool** up-to-date with the latest features and security patches:

1. **Automatic Update Check** 🔍:
    - Upon running, XynsTool checks for the latest release on GitHub.
    - If a new version is available, it prompts you to update.

2. **Secure Update Process** 🔒:
    - Downloads the update script and its signature.
    - Verifies the signature using GPG to ensure authenticity.
    - Installs the update upon successful verification.

**Note**: Ensure your GPG key is correctly set up and replace the placeholder fingerprint with your actual GPG key fingerprint.

## 🛡️ Security Considerations

**XynsTool** prioritizes security to protect your projects:

- **GPG Signature Verification** 🔒:
    - Ensures that updates are authentic and have not been tampered with.
    - **Setup**:
        - Replace `A2204479CEDA92DA4058027780DDD12DCD9F7D6B` with your actual GPG key fingerprint in the script.

- **Secure Update URLs** 🔗:
    - All update downloads are performed over HTTPS to prevent man-in-the-middle attacks.

- **Permissions Management** 🔑:
    - The script requires appropriate permissions to modify `/usr/local/bin/`.
    - **Recommendation**: Run the script with a user that has `sudo` privileges.

## 🤝 Contributing

We welcome contributions from the community! Follow these steps to contribute to **XynsTool**:

1. **Fork the Repository** 🍴:
    - Click the "Fork" button at the top right of the [GitHub repository](https://github.com/arcmoonstudios/XynsRustyTool).

2. **Clone Your Fork** 📥:
    
        git clone https://github.com/your_username/XynsRustyTool.git
        cd XynsRustyTool

3. **Create a New Branch** 🌱:
    
        git checkout -b feature/your-feature-name

4. **Make Your Changes** ✏️:
    - Implement your feature or fix a bug.

5. **Commit Your Changes** 📝:
    
        git commit -m "Add feature: your feature description"

6. **Push to Your Fork** 🚀:
    
        git push origin feature/your-feature-name

7. **Create a Pull Request** 📨:
    - Navigate to your fork on GitHub and click "Compare & pull request".

**Please ensure your contributions adhere to our [Code of Conduct](https://github.com/arcmoonstudios/XynsRustyTool/blob/main/CODE_OF_CONDUCT.md).**

## 📄 License

Distributed under the [MIT License](https://opensource.org/licenses/MIT). See `LICENSE` for more information.

## 📞 Contact

Have questions or need support? Reach out to us:

- **Email** 📧: support@arcmoonstudios.com
- **GitHub Issues** 🐛: [Open an Issue](https://github.com/arcmoonstudios/XynsRustyTool/issues)

---

✨ **Thank you for using XynsTool!** We're excited to see what you build with it. Happy coding! 🦀🚀

---
