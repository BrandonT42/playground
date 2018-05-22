# RPC Errors

Here I will attempt to decipher the error messages that turtlecoind and walletd spit out, and try my best to give a reason behind the error, as well as a better possible error message. So let's start, shall we?

# Turtlecoind Errors

# Walletd Errors
## `Bad address`
**Description:**
This error can happen when an address you supply is invalid, or the address field in your request is improperly formatted.

**Solution:**
First make sure that the address you are attempting to send to is a valid 99 character long TRTL address. Next, make sure that your request is properly formatted - for instance, in a SendTransaction request where you are sending from multiple addresses, the address field must be an array of strings, and the address field within the transfers array must be a single string.

**Possible Alternative Error:**
> The supplied address parameter is invalid or in an incorrect format

## `Wrong amount`
**Description:**
This error can happen when the amount you are trying to send within a transaction is above the sum of your available inputs, or is in an incorrect format.

**Solution:**
This error can be solved by ensuring that the amount you are attempting to send is valid and within the bounds of your available balance, and that your wallet has been properly optimized/fused. 

**Possible Alternative Error:**
> The requested send amount is in an incorrect format, or your wallet does not have enough balance or available inputs to send the requested amount
