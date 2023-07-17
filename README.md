# reactivateAccount
Automate an account reactivation process

The account reactivation process required the user to submit a request to reactivate their account.
A Google Sheet is used to store the user ID and reactivation date.
Google Sheet API is used to connect to the sheet. Source: https://developers.google.com/sheets/api/quickstart/python

The script checks if the reactivate date is less than or equal to todays date. This is done by converting the date on the sheet and todays date to unix time.

If there is a date match, the user ID is added to a list to be used later.
Selenium and webdriver is used to open a browser session, login to the Admin and open each user page. A check is done on each user page to confirm the account is not active.
If the account is not active, it is reactivated.
