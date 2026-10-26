# PSE&G Auth Companion Add-on

Automated sign-in companion service for the [PSE&G Home Assistant Integration](https://github.com/sidprax/ha-pseg).

## How it works

The companion add-on runs an isolated, headless Chromium browser to automate portal authentication:

1. **Direct MyMeter Account (Recommended — Zero 2FA)**:
   When connected using an invited MyMeter email and password (via MyMeter > Connect User), the add-on logs into `mysmartenergy.nj.pseg.com` directly with "Remember Me" enabled. Google reCAPTCHA invisible runs automatically and cookies are refreshed silently without ever requesting an SMS or Email OTP code.

2. **Primary PSE&G Okta Account (SMS/Email OTP)**:
   When connected using your primary `nj.pseg.com` credentials, the add-on navigates Okta SSO, automates reCAPTCHA challenges, and coordinates one-time verification passcodes (SMS/Email OTP) via Home Assistant during initial setup or re-authentication.

Once the session cookie is negotiated, Home Assistant uses standard HTTPS REST calls to fetch usage, cost, and historical data.

## Configuration

This add-on requires no configuration. Simply start the add-on, enable **Start on boot** and **Watchdog**, and proceed with the integration setup in Home Assistant.
