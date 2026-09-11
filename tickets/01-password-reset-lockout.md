# Ticket #01 — User Locked Out After Password Reset

**Category:** Account/Access
**Priority:** High
**Tools used:** Active Directory, ticketing system

## Reported Issue
User reports being locked out of their workstation after multiple failed login attempts
following a recent password reset.

## Diagnosis
- Checked AD account status → account was locked (bad password count exceeded threshold)
- Verified the new password had not synced correctly on user's end (autocomplete issue in browser)

## Resolution
1. Unlocked the account in Active Directory Users and Computers
2. Manually reset password and set "must change at next logon"
3. Walked user through clearing cached credentials
4. Confirmed successful login

## Outcome
Ticket resolved in ~10 minutes. Verified with user before closing.

## Screenshot
![AD unlock](../screenshots/ad-unlock-example.png)
