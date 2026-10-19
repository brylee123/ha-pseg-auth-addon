# PSE&G Home Assistant Add-ons

Official Home Assistant Add-on repository for the [PSE&G Integration](https://github.com/sidprax/ha-pseg).

## Add-ons in this Repository

### [PSE&G Auth Companion](pseg_auth/)
Headless browser companion service that automates sign-in and handles OTP/reCAPTCHA challenges for the PSE&G integration.

## Installation

### Method 1: 1-Click via My Home Assistant

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fsidprax%2Fha-pseg-auth-addon)

### Method 2: Manual Setup

1. In Home Assistant, navigate to **Settings** > **Add-ons** > **Add-on Store**.
2. Click the three dots in the top right corner and select **Repositories**.
3. Add this repository URL:
   ```text
   https://github.com/sidprax/ha-pseg-auth-addon
   ```
4. Click **Add**, then close the dialog.
5. In the Add-on Store, find **PSE&G Auth Companion**, click **Install**, and **Start**.
6. Turn on **Start on boot** and **Watchdog**.

## License

MIT
