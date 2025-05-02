# QZX-Windows

**QZX-Windows** is a GitHub Actions workflow that enables Remote Desktop Protocol (RDP) access to a Windows GitHub runner by automatically setting up a secure TCP tunnel using `ngrok`.

## Features

- Enables RDP on the GitHub-hosted Windows runner.
- Sets up a secure `ngrok` tunnel for external access.
- Automatically configures firewall and terminal server settings.
- Sets a predefined password for the `runneradmin` user.

## Usage

1. Fork or clone this repository.
2. Go to your GitHub repository page.
3. Click on the **Settings** tab.
4. In the left sidebar, click **Secrets and variables** > **Actions**.
5. Click the **New repository secret** button.
6. In the **Name** field, enter `NGROK_AUTH_TOKEN`.
7. In the **Secret** field, paste your auth token from the [ngrok dashboard](https://dashboard.ngrok.com/get-started/your-authtoken).
8. Click **Add secret** to save.
9. Run the `QZX☆` workflow manually via the **Actions** tab or push to trigger it automatically.

## Default RDP Credentials

- **Username:** `runneradmin`
- **Password:** `P@ssw0rd!`

## How to Connect via RDP

1. Once the workflow completes, open the logs in the GitHub Actions page.
2. Look for the output in the `Start ngrok tunnel` step – it will show an address like `tcp://x.tcp.ngrok.io:xxxxx`.
3. Open the Remote Desktop Connection tool on your computer.
4. Enter the ngrok address in the "Computer" field.
5. Use the provided credentials to log in.

## Notes

- This setup only works temporarily while the GitHub runner is active.
- The `runneradmin` password can be changed for security purposes.
- The `ngrok` tunnel address will be different each time the workflow runs.

## License

MIT License

---

**Developed by İsmet Emir**

---
## Github Fix plz

![ngrok setup](https://i.postimg.cc/FszW1vBz/Screenshot-20250502-184406-Windows-App.jpg)
