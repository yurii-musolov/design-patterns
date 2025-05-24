# Facade

Facade is a structural design pattern that provides a simplified (but limited) interface to a complex system of classes, library or framework.

While Facade decreases the overall complexity of the application, it also helps to move unwanted dependencies to one place.

pub struct WalletFacade hides a complex logic behind its API. A single method add_money_to_wallet interacts with the account, code, wallet, notification and ledger behind the scenes.

Run

```bash
cargo run --bin facade
```

Output

```bash
Starting create account
Account created

Starting add money to wallet
Account verified
Security code verified
Sending wallet credit notification
Make ledger entry for accountId abc with transaction type credit for amount 10

Starting debit money from wallet
Account verified
Security code verified
Sending wallet debit notification
Make ledger entry for accountId abc with transaction type debit for amount 5
```
