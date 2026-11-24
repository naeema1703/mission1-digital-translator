# Tier 2 — ATM Withdrawal Algorithm

## 1. Card Insertion and Verification

1. Prompt the customer to insert their ATM card.
2. Read the card information to verify that the card is valid and has not expired.
3. Check whether the card can be successfully read.

   - **If the card cannot be read or is invalid:** Display an error message: "Invalid or unreadable card." Eject the card and terminate the transaction.
   - **If the card is valid:** Proceed to Stage 2.

## 2. PIN Authentication

1. Prompt the customer to enter their four-digit PIN.
2. Compare the entered PIN with the authentication information held by the banking system.

   - **If the PIN is incorrect:**
     - Display "Incorrect PIN. Try again."
     - Allow up to three total attempts.
     - If all three attempts fail, block further attempts according to the bank's security policy, retain or handle the card according to the ATM's security procedure, and terminate the transaction.
   - **If the PIN is correct:** Grant access and proceed to Stage 3.

## 3. Withdrawal Amount

1. Display the ATM's main menu.
2. Prompt the customer to select the Withdrawal option.
3. Ask the customer to select or enter the desired withdrawal amount.
4. Validate the requested amount.

   - The amount must be a positive number.
   - The amount must be within the ATM's permitted withdrawal limits.
   - The amount must be compatible with the available banknote denominations.

   - **If the amount is invalid:** Display "Invalid amount" and request another amount.
   - **If the amount is valid:** Proceed to Stage 4.

## 4. Balance Verification and Cash Availability

1. Retrieve the customer's available account balance.
2. Compare the available balance with the requested withdrawal amount.

   - **If the balance is insufficient:** Display "Insufficient funds." Allow the customer to enter a smaller amount or cancel the transaction.

3. Check whether the ATM has enough physical cash to dispense the requested amount.

   - **If the ATM has insufficient cash:** Display "Unable to dispense requested amount. ATM has insufficient cash." Allow the customer to enter a smaller amount or cancel.

4. If both checks are successful:
   - Authorize the transaction.
   - Dispense the requested cash.
   - Confirm that the cash was successfully dispensed.
   - Update the customer's account balance to reflect the completed withdrawal.

5. If cash dispensing fails after authorization, initiate the appropriate transaction reversal or recovery process so the customer is not incorrectly charged.

6. Proceed to Stage 5 after successful transaction completion.

## 5. Transaction Completion

1. Prompt the customer to collect their cash.
2. Ask whether they want a printed receipt.
3. Print the receipt if requested.
4. Eject the ATM card.
5. Prompt the customer to retrieve their card.
6. Display "Thank you for banking with us."
7. Reset the ATM screen for the next customer.

## Failure Handling Summary

| Situation | Expected System Response |
|---|---|
| Card cannot be read | Display an error and terminate the transaction. |
| Invalid card | Reject the card and terminate the transaction. |
| Incorrect PIN | Allow another attempt, up to the permitted limit. |
| Three failed PIN attempts | Block further attempts according to security policy. |
| Invalid withdrawal amount | Request a valid amount. |
| Insufficient account balance | Request a smaller amount or allow cancellation. |
| Insufficient ATM cash | Request a smaller amount or allow cancellation. |
| Cash dispensing failure | Initiate transaction recovery or reversal. |

## Algorithm Objective

The objective of this algorithm is to describe the logical sequence of operations required to complete an ATM cash withdrawal safely and correctly.

It demonstrates how a computer system uses sequential instructions, conditional decisions, input validation and error handling to solve a real-world problem.

## Key Programming Concepts Demonstrated

- **Sequence:** Instructions are executed in an organized order.
- **Selection:** The system makes decisions based on conditions.
- **Input Validation:** The system checks whether supplied information is acceptable.
- **Error Handling:** The system responds appropriately when something goes wrong.
- **Data Processing:** The system retrieves and updates account information.
- **Transaction Management:** The system ensures that account records reflect the actual transaction outcome.