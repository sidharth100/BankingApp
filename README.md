# BankingApp
Which test cases failed?

Some of the Bank and Account test cases failed.

a)	Which cases fail?
•	Public void testGetBalance  failed in Account Class.
•	Public void testOpenAccount() throws AccountExistsException in BankTest Class.
•	Public void testDeposit() throws AccountDoesNotExistException in BankTest Class
•	Public void testwithdraw() throws AccountDoesNotExistException in BankTest Class
•	Public void testGetBalance() throws AccountDoesNotExistException in BankTest Class
•	Public void testTransfer() throws AccountDoesNotExistException in BankTest Class


b)	Why do they fail?

Account Class:
The testGetBalance failed because the object by the name content of money class was declared private in Account class so it was not accessible from AccountTest Class. When we changed it from private to public we were able pass the test for this function.

Bank Class:
Main Problem was in the openAccount() function as in the else case get() was used to add the names. As get() function is used to get the information not save so it was not saving anything. We have to use Put() function to save data in hashtables .
This was the reason we were not able to perform any transaction or action on the accounts using all of the above listed function as it was saying Account does not exist.
As soon as we changed the get() to put(), we were able pass the tests for the mentioned failed test cases.
