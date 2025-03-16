

The error `bash: gh: command not found` indicates that the GitHub CLI (`gh`) is not installed in your environment. To use `gh` commands, you need to install the GitHub CLI first. Here's how you can install and set it up in your Termux or `proot-distro` environment:

---

### Steps to Install GitHub CLI (`gh`)

1. **Update and Install Dependencies**:
   Ensure your environment is up to date and install necessary dependencies:
   ```bash
   pkg update
   pkg install curl git
   ```

2. **Download and Install GitHub CLI**:
   - For Termux (Android), you can install the precompiled `gh` binary for Linux ARM64:
     ```bash
     curl -LO https://github.com/cli/cli/releases/download/v2.40.1/gh_2.40.1_linux_arm64.tar.gz
     tar -xzf gh_2.40.1_linux_arm64.tar.gz
     mv gh_2.40.1_linux_arm64/bin/gh /data/data/com.termux/files/usr/bin/
     ```
   - For `proot-distro` (Ubuntu), you can use the official installation script:
     ```bash
     curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg
     echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
     sudo apt update
     sudo apt install gh
     ```

3. **Verify Installation**:
   Check if `gh` is installed correctly:
   ```bash
   gh --version
   ```

---

### Authenticate with GitHub

1. **Log in to GitHub**:
   Run the following command to authenticate with GitHub:
   ```bash
   gh auth login
   ```
   Follow the prompts to authenticate using a web browser or a personal access token.

2. **Create a Repository**:
   Once authenticated, you can create a new repository:
   ```bash
   gh repo create Termux --public
   ```

---

### Troubleshooting

- **Command Not Found After Installation**:
  If `gh` is still not found after installation, ensure the binary is in your `PATH`. You can add it manually:
  ```bash
  export PATH=$PATH:/data/data/com.termux/files/usr/bin
  ```

- **Permission Issues**:
  If you encounter permission issues, ensure you have the necessary permissions to write to the `/data/data/com.termux/files/usr/bin` directory or use `sudo` in `proot-distro`.

---

