# IAM: MFA

To defend users and groups from being compormised

1. Password Policy
2. Multi Factor Authentication


## 1. Password Policy

- Min length
- Specific character types requires
- Allow users to change their own passwords
- Require them to change there own passwords after some time. (password expiration).
- Prevent password re-use.

## 2. Multi factor Authentication - MFA

- Users have access to your account so you want to at least protect your root account and IAM users.
  - Users could change configurations or delete resources!

MFA = password you know + security device you own

- If a password is stolen or hacked the account is not compromised.

### MFA devices options in AWS

- Virtual MFA device
  - Google authenticator (phone only)
  - Authy (muti-device)
  - Support for multiple tokens on a single device

- Universal 2nd Factor (U2F) Security Key
  - Physical device
  - e.g. YubiKey by Yubico
  - Supports multiple root and IAM users using a single security key

- Hardware Key Fob MFA Device
  - e.g. Provided by Gemalto

- Hardware Key Fob MFA Device for AWS GovCloud (US)
  - Provided by SurePassID

# Steps to Create Password Policy and MFA

## Password Policy

1. IAM
2. Account Settings
3. Password policy - Edit
4. IAM default or Custom

## MFA for Root Account

1. Account name
2. Security credentials
3. Assign MFA device
4. Name e.g. iphone
5. Device type e.g. Authenticator app
6. Set up device
7. See list of compatible apps
