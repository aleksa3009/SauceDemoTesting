# TestData

This folder contains test data files used during manual functional testing of the SauceDemo (Swag Labs) e‑commerce demo application.

## Contents

- `checkout_users.csv`  
  Contains 5 sample checkout user profiles for testing the **Checkout: Your Information** form.  
  Each row includes:
  - First Name  
  - Last Name  
  - ZIP/Postal Code  
  - Notes (e.g., valid, missing fields, special characters)

- `login_credentials.md`  
  A markdown file listing valid and invalid user credentials used to test login functionality, including:
  - `standard_user`  
  - `locked_out_user`  
  - `problem_user`  
  - `performance_glitch_user`  
  - Invalid combinations for negative testing (wrong password, empty fields, SQL injection)

## Purpose

These files support data-driven test execution by allowing repeatable and consistent input during:
- Login form validation (positive and negative scenarios)
- Checkout form validation using diverse user profiles
- Edge-case testing for missing, invalid, or unusual inputs