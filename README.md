<a href="https://www.twilio.com">
  <img src="https://static0.twilio.com/marketing/bundles/marketing/img/logos/wordmark-red.svg" alt="Twilio" width="250" />
</a>
  
# Twilio Account Security Quickstart - Twilio Authy and Twilio Verify

A simple Java, Spring and AngularJS implementation of a website that uses Twilio Authy to protect all assets within a folder with two-factor authentication. Additionally, it shows a Verify Phone Verification implementation.

It uses four channels for delivery, SMS, Voice, Soft Tokens, and Push Authentication. You should have the [Authy App](https://authy.com/download/) installed to try Soft Token and Push Authentication support.

Repository based on [this repository](https://github.com/TwilioDevEd/account-security-quickstart-spring/)

#### Requirements
- Java 8 (I used jdk-8u171)
- Code editor (I used IntelliJ IDEA Community Edition)

This project use one SQLite Database which it can explored by this software: [DB Browser](http://sqlitebrowser.org)

#### Two-Factor Authentication Demo
- URL path "/protected" is protected with both user session and Twilio Authy Two-Factor Authentication
- One Time Passwords (SMS and Voice)
- SoftTokens
- Push Notifications (via polling)

#### Phone Verification
- Phone Verification
- SMS or Voice Call

### URIs - URLs

- Index     http://localhost:8080/index.html
- Register  http://localhost:8080/register/index.html
- Login     http://localhost:8080/login/index.html
- Logout    http://localhost:8080/api/logout
- 2FA       http://localhost:8080/2fa/index.html
- Protected http://localhost:8080/protected/index.html (Only accessible by a logged in user and 2fa)

### Setup
- Clone this repo
- Run `gradle build`
- Register for a [Twilio Account](https://www.twilio.com/).
- Setup an Account Security app via the [Twilio Console](https://twilio.com/console).
- Grab an Application API key from the Dashboard and paste it in `.env.example`
- Save the `.env.example` file as `.env`
- Load the configuration with `source .env`
- Or set API Key in the method getAuthyId of the class Settings
- Run `gradle appRun` from the cloned repo to run the app

### License
- MIT
