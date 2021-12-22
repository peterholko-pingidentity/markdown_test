# PingOne


PingOne SSO is a cloud-based framework for secure identity access management.

## Connection Properties

#### Client ID `textField`


The id for your client found in Ping's Dashboard

#### Client Secret `textField`


Client Secret from your client in Ping's Dashboard

#### Region `dropDown`


The region your PingOne environment is in.


 - North America - US
 - North America - Canada
 - Europe
 - Asia - Australia

#### Environment ID `textField`


Your Environment ID provided by Ping.

## Capabilites

### Create User (createUser)


Create user in PingOne.

#### Username `textField` `required`


undefined

#### Population ID `textField`


ID of the Population

#### Password `textField`


undefined

#### Given Name `textField`


undefined

#### Family Name `textField`


undefined

#### Email `textField`


undefined

#### Primary Phone `textField`


undefined

#### Mobile Phone `textField`


undefined

#### Preferred Language `textField`


undefined

#### Locale `textField`


undefined

#### Additional Properties `textField`


Input additional properties as JSON.

#### Lifecycle Status `dropDown`


Indicate whether the new user account must be verified after it is created.

---

### Read User (readUser)


Retrieves user information.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

---

### User Lookup (userLookup)


Look up a user in the directory with an identifier to determine the authentication authority

#### Match Attributes `textFieldArrayView`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

---

### Update User (updateUser)


Update user information in PingOne.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Username `textField` `required`


undefined

#### Given Name `textField`


undefined

#### Family Name `textField`


undefined

#### Email `textField`


undefined

#### Primary Phone `textField`


undefined

#### Mobile Phone `textField`


undefined

#### Preferred Language `textField`


undefined

#### Locale `textField`


undefined

#### Additional Properties `textField`


Input additional properties as JSON.

---

### Delete User (deleteUser)


Deletes a user.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

---

### Enable User (enableUser)


You can set enable status of a P1 User

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Enable User `toggleSwitch`


User enabled status in PingOne

---

### Send Email Verification Code (sendVerificationCode)


Sends a verification code to the user that can be used to verify their email.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

---

### Verify Email (verifyUser)


Verifies a users email with a code sent to them

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Verification Code `textField`


Code to verify a user's account.

---

### Send Recovery Code (sendRecoveryCode)


Sends a one time use recovery code to the user's email that may be used to recover a forgotten password

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

---

### Check Password (checkPassword)


You can check a user's P1 password to verify its current state

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Password `textField`


undefined

---

### Recover Password (recoverPassword)


Recovers a forgotten password using a one time use recovery code

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Recovery Code `textField`


The recovery code sent to the user.

#### New Password `textField`


The new password for the user.

---

### Reset Password (resetPassword)


User can reset their PingOne password

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Current Password `textField`


Current Password of the user.

#### New Password `textField`


The new password for the user.

---

### Set Password (setPassword)


Set a user's password, optionally forcing user to change password and bypass ping password policy

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Password Value `textField`


The new password to set for the user provided as clear text or pre-encoded.

#### Force Change Password `toggleSwitch`


User required to change password

#### Bypass PingOne Password Policy `toggleSwitch`


PingOne Password Policies will be bypassed

---

### Check User Agreement (checkUserAgreement)


Performs a check to determine if a user needs to accept an agreement. If required, agreement presentation resources are provided.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Agreement ID `textField`


ID of the PingOne Agreement

#### Accept Language `textField`


IETF BCP 47 language tag

---

### Read User Agreements (readUserAgreements)


Retrieves user agreement acceptance information for all agreements in the PingOne environment.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Accept Language `textField`


IETF BCP 47 language tag

---

### Revoke User Agreement (revokeUserAgreement)


Revokes the agreement for a given user if they have accepted the agreement previously

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Agreement ID `textField`


ID of the PingOne Agreement

#### Accept Language `textField`


IETF BCP 47 language tag

---

### Accept User Agreement (acceptAgreement)


Accepts an agreement for a user.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

#### Agreement Presentation ID `textField`


Read User Agreement and Read Agreement capabilities generate this id in their agreement presentation output.

---

### Read Agreement Content (readAgreementContent)


Retrieves agreement content needed to present an agreement to a user that does not exist in PingOne.

#### Agreement ID `textField`


ID of the PingOne Agreement

#### Accept Language `textField`


IETF BCP 47 language tag

#### User Locale `textField`


The user's location. A valid value is a language tag as defined in RFC 5646. Example: "en-US", "az-Arab"

---

### Read Population (readPopulation)


Retrieves population information.

#### Population ID `textField`


ID of the Population

---

### Read User Group Memberships (readUserGroupMemberships)


Retrieves information for all groups a user has membership for.

#### Match Attributes `dropDown`


Schema attributes to match against.

#### Identifier `textField`


Identifier to match a user.

---
