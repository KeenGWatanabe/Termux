To switch back to Termux from a `proot-distro` Ubuntu session, you can simply **exit the proot environment**. Here's how:

### Steps to Switch Back to Termux
1. **Exit the Proot Environment**:
   While inside the `proot-distro` Ubuntu session, type the following command:
   ```bash
   exit
   ```
   This will terminate the proot session and return you to the Termux shell.

2. **Verify You're Back in Termux**:
   After running `exit`, you should see the Termux prompt (usually something like `~ $`). You can confirm you're back in Termux by running:
   ```bash
   uname -a
   ```
   This should show `Android` or `aarch64` instead of `Linux` or `Ubuntu`.

### Additional Notes
- If you want to return to the `proot-distro` Ubuntu session later, simply run:
  ```bash
  proot-distro login ubuntu
  ```
- You can have multiple `proot-distro` environments installed (e.g., Ubuntu, Alpine, Debian). Use the `proot-distro list` command to see all installed distributions.

