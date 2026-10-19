# PSE&G Auth Companion Add-on

Automated sign-in companion service for the [PSE&G Home Assistant Integration](https://github.com/sidprax/ha-pseg).

## How it works

The companion add-on runs an isolated, headless Chromium browser to automate Okta portal authentication, handle reCAPTCHA audio challenges, and forward the one-time passcode (SMS/Email OTP) to establish an authenticated session cookie.

Once the session cookie is negotiated, Home Assistant uses standard HTTPS REST calls to fetch usage, cost, and historical data.

## Configuration

This add-on requires no configuration. Simply start the add-on, enable **Start on boot** and **Watchdog**, and proceed with the integration setup in Home Assistant.
