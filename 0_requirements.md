# Requirements

## Description
- At least three type of bank accounts: blocked, normal, premium
- depends on type of account, there are different limitation of daily and monthly transfer and withdraw.
- Transfer will be done next work day, but it will blocked the money.
- After withdraw, transfer or deposit money, the amount of money should be shown.
- There is monthly interest, but also possible yearly interest depends on account type
- if user failed to login 3 times, blocked the account
- Transfer information can be saved for next time.
- During transfer, user can select previours saved transfer setting.
- User can select print result, or show result on monitor after operation.
- One person can have several account
- Store information about account owner.
- Only the person above 18 years old can have an account.
- if the person have no account, delete him/her after half year.

## Chanllenges
- The system might be used abroad in the country in different time zone.

## Basic Functions

### API for Bank
- Create Account
- Create Person

### Withdraw
- Daily Limit 300€ or 1000€
- Monthly Limit 720€ or 5000€

### Transfer
- Daily and Monthly limit 720 or 10000€

### LogIn
- Wrong Password: up to 3 times

### Export Info 
