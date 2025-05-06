# 🪙 Custom Token Smart Contract

This project is a custom token smart contract built on the **Soroban** smart contract platform of the **Stellar** blockchain. It extends the default token interface with **administrative capabilities**, such as:

- ✅ Custom minting and burning logic
- 🧊 Account freezing feature
- 👮 Admin management
- 🔐 Standard token features (transfer, approve, burn, etc.)

---
## 🚀 Contract Address

**`CDXZQLZMQLCC2F3FMSQAEWXMJCDIBHNW6SQ3DUJFFGDEASY4BYJAG6EJ`**

---

## 📦 Features

- 🔐 **Admin-controlled Minting**  
  Only the administrator can mint new tokens.

- 🧊 **Freeze Accounts**  
  The admin can freeze accounts. Frozen accounts cannot burn tokens.

- 🔄 **ERC20-like Token Interface**  
  Supports functions such as `transfer`, `approve`, `allowance`, `burn`, `transfer_from`.

- 📊 **Metadata Support**  
  Includes token `name`, `symbol`, and `decimals`.

- 🔁 **TTL Extensions**  
  Storage entries have TTL (time to live) mechanics to manage storage efficiently.

---

## 🛠️ Contract Functions

### `initialize(admin, decimal, name, symbol)`
Initializes the token with metadata and sets the admin.

### `mint(to, amount)`
Mints `amount` tokens to `to` address. Admin only.

### `burn(from, amount)`
Burns tokens from an address. Cannot burn if account is frozen.

### `freeze_account(account)`
Freezes a given account.

### `set_admin(new_admin)`
Transfers admin rights to another address.

### ERC20 Functions:
- `transfer(from, to, amount)`
- `approve(from, spender, amount, expiration)`
- `allowance(from, spender)`
- `balance(id)`
- `burn_from(spender, from, amount)`

---

## 🧪 Testing

You can run tests with:
```bash
cargo test
