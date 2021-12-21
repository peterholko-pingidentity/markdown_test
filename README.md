# PingOne


PingOne SSO is a cloud-based framework for secure identity access management.

## Connection Properties


 - Client ID
     - Description: The id for your client found in Ping's Dashboard
     - Type: textField
    
 - Client Secret
     - Description: Client Secret from your client in Ping's Dashboard
     - Type: textField
    
 - Region
     - Description: The region your PingOne environment is in.
     - Type: dropDown
    
 - Environment ID
     - Description: Your Environment ID provided by Ping.
     - Type: textField
    

## Capabilites

### Create User (createUser)


Create user in PingOne.

#### username


 - Description: undefined
 - Type: textField
 - Required: true

#### populationId


 - Description: ID of the Population
 - Type: textField

#### password


 - Description: undefined
 - Type: textField

#### given


 - Description: undefined
 - Type: textField

#### family


 - Description: undefined
 - Type: textField

#### email


 - Description: undefined
 - Type: textField

#### primaryPhone


 - Description: undefined
 - Type: textField

#### mobilePhone


 - Description: undefined
 - Type: textField

#### preferredLanguage


 - Description: undefined
 - Type: textField

#### locale


 - Description: undefined
 - Type: textField

#### additionalUserProperties


 - Description: Input additional properties as JSON.
 - Type: textField

#### lifecycleStatus


 - Description: Indicate whether the new user account must be verified after it is created.
 - Type: dropDown

---

### Read User (readUser)


Retrieves user information.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

---

### User Lookup (userLookup)


Look up a user in the directory with an identifier to determine the authentication authority

#### matchAttributes


 - Description: Schema attributes to match against.
 - Type: textFieldArrayView

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

---

### Update User (updateUser)


Update user information in PingOne.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### username


 - Description: undefined
 - Type: textField
 - Required: true

#### given


 - Description: undefined
 - Type: textField

#### family


 - Description: undefined
 - Type: textField

#### email


 - Description: undefined
 - Type: textField

#### primaryPhone


 - Description: undefined
 - Type: textField

#### mobilePhone


 - Description: undefined
 - Type: textField

#### preferredLanguage


 - Description: undefined
 - Type: textField

#### locale


 - Description: undefined
 - Type: textField

#### additionalUserProperties


 - Description: Input additional properties as JSON.
 - Type: textField

---

### Delete User (deleteUser)


Deletes a user.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

---

### Enable User (enableUser)


You can set enable status of a P1 User

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### enabled


 - Description: User enabled status in PingOne
 - Type: toggleSwitch

---

### Send Email Verification Code (sendVerificationCode)


Sends a verification code to the user that can be used to verify their email.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

---

### Verify Email (verifyUser)


Verifies a users email with a code sent to them

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### verificationCode


 - Description: Code to verify a user's account.
 - Type: textField

---

### Send Recovery Code (sendRecoveryCode)


Sends a one time use recovery code to the user's email that may be used to recover a forgotten password

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

---

### Check Password (checkPassword)


You can check a user's P1 password to verify its current state

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### password


 - Description: undefined
 - Type: textField

---

### Recover Password (recoverPassword)


Recovers a forgotten password using a one time use recovery code

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### recoveryCode


 - Description: The recovery code sent to the user.
 - Type: textField

#### newPassword


 - Description: The new password for the user.
 - Type: textField

---

### Reset Password (resetPassword)


User can reset their PingOne password

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### currentPassword


 - Description: Current Password of the user.
 - Type: textField

#### newPassword


 - Description: The new password for the user.
 - Type: textField

---

### Set Password (setPassword)


Set a user's password, optionally forcing user to change password and bypass ping password policy

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### passwordValue


 - Description: The new password to set for the user provided as clear text or pre-encoded.
 - Type: textField

#### forceChange


 - Description: User required to change password
 - Type: toggleSwitch

#### bypassPolicy


 - Description: PingOne Password Policies will be bypassed
 - Type: toggleSwitch

---

### Check User Agreement (checkUserAgreement)


Performs a check to determine if a user needs to accept an agreement. If required, agreement presentation resources are provided.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### agreementId


 - Description: ID of the PingOne Agreement
 - Type: textField

#### acceptLanguage


 - Description: IETF BCP 47 language tag
 - Type: textField

---

### Read User Agreements (readUserAgreements)


Retrieves user agreement acceptance information for all agreements in the PingOne environment.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### acceptLanguage


 - Description: IETF BCP 47 language tag
 - Type: textField

---

### Revoke User Agreement (revokeUserAgreement)


Revokes the agreement for a given user if they have accepted the agreement previously

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### agreementId


 - Description: ID of the PingOne Agreement
 - Type: textField

#### acceptLanguage


 - Description: IETF BCP 47 language tag
 - Type: textField

---

### Accept User Agreement (acceptAgreement)


Accepts an agreement for a user.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

#### agreementPresentationId


 - Description: Read User Agreement and Read Agreement capabilities generate this id in their agreement presentation output.
 - Type: textField

---

### Read Agreement Content (readAgreementContent)


Retrieves agreement content needed to present an agreement to a user that does not exist in PingOne.

#### agreementId


 - Description: ID of the PingOne Agreement
 - Type: textField

#### acceptLanguage


 - Description: IETF BCP 47 language tag
 - Type: textField

#### userLocale


 - Description: The user's location. A valid value is a language tag as defined in RFC 5646. Example: "en-US", "az-Arab"
 - Type: textField

---

### Read Population (readPopulation)


Retrieves population information.

#### populationId


 - Description: ID of the Population
 - Type: textField

---

### Read User Group Memberships (readUserGroupMemberships)


Retrieves information for all groups a user has membership for.

#### matchAttribute


 - Description: Schema attributes to match against.
 - Type: dropDown

#### identifier


 - Description: Identifier to match a user.
 - Type: textField

---
