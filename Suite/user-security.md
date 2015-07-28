---
title: 'User Security in Suite'
tags: 'Security, SuiteAdmin'
old_url: 'http://emarsys.dev/resources/data-security/user-security/'
---

Keeping your data safe, and that of your customers, is of paramount importance to us. Below you can find an overview of the security precautions in place for user access to the Suite platform.

### Password requirements

 All Suite users are required to use a suitably strong password. When entering a new password for the first time, Suite will check its complexity and inform youÂ if it is not complex enough. In addition to this:

- Passwords are valid for a maximum of 180 days, after which Suite will require you to change it.
- You may be requested to change your passwords earlier than that, for example if a new security feature has been enabled for you, or if suspicious activity related to your account is detected.
- You cannot reuse any of your last three passwords.

 We encourage you to use an established password management tool to take care of your Suite passwords. Emarsys does not endorse any tool in particular, but advises you to choose the one that best suits your requirements. Examples of such tools are:

- [LastPass](http://lastpass.com/)
- [Keypass](http://keepass.info/)
- [1Password](http://1password.com/)

#### Lockout

 To prevent brute-force attacks from being successful, users are temporarily locked out if a wrong password is entered multiple times. The default lockout period is 24 hours, but this can vary from account to account.Â After the lockout period expires, the account is automatically unlocked, although Emarsys Technical Support can bypass the expiration period and unlock the account for you if required.

### Two-factor authentication

 We offer the possibility to further enhance the security level by providing a two-factor authentication. This can be done via the following methods:

- **Time-based two-factor authentication (in development)** This requires a one-off synchronization between your smartphone and our server, which creates an encrypted secret string. One-time passwords are then generated using this secret, which allow you to log in securely. This method does not require any kind of mobile connectivity, which means deliverability issues are bypassed, and the login codes are generated every minute to avoid the possibility of them being reused. Applications will be available for all major smartphone platforms.
- **SMS/email-based two-factor authentication** This requires a dedicated mobile phone number or email address for the authentication to be sent to. When logging in to Suite, a one-time password (typically a numeric code) is sent via the preferred channel, and you then use this password on along with your usual credentials to log in. It is valid for five minutes only, and lasts for the duration of your session. This means that you need to use a new code every time you log in.

##### Trusted devices

 For user convenience, your device(s) can be defined as trusted in Suite by using the â&#128;&#156;Remember this deviceâ&#128;&#157; checkbox on the Suite login page. If a trusted device authenticates successfully, then you will not need to enter any further password or login information. As an extra layer of protection a device can only be remembered for 14 days; after this time, or if the admin password is changed in Suite, you will be prompted to log in again. If a password is compromised (lost or stolen), you should immediately log in and update the two-factor authentication settings in Suite, and also log in again with the trusted device using the new credentials. If a trusted device is lost or stolen, then the Suite password should be changed immediately to prevent the device from being used to log in. A password reset automatically revokes all trust relationships from previously configured devices, and you may re-enable two-factor authentication at any time. **Note:** It is highly risky to enable this feature on public or shared computers, and we do not recommend it.

### IP Whitelisting

 You can also request that access to your account is restricted to specific IP addresses, or ranges of addresses. When logging in from these whitelisted addresses, your user credentials (admin password, user name, account name) are sufficient to log in, and two-factor authentication is not needed. When logging in from an unknown IP address (i.e. non-whitelisted address), then two-factor authentication will be required to proceed.

### Disabling on inactivity

 Emarsys automatically disables user accounts where no login has occurred for 180 days. All data related to these users is retained indefinitely, and the account can be re-activated by Emarsys Technical Services at any time. A password change will be necessary upon the next login for a reactivated account, and the Dashboard will automatically redirect to the password change screen.

### Error messages

 For a full list of error messages that you might seen after a failed login attempt, and their explanation, click [here](/Resources/login-faq.md "Failed Login â&#128;&#147; FAQ").