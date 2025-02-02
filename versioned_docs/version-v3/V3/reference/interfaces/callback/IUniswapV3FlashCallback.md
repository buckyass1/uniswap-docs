Any contract that calls IUniswapV3PoolActions#flash must implement this interface


## Functions
### uniswapV3FlashCallback
```solidity
  function uniswapV3FlashCallback(
    uint256 fee0, uint256 fee1, bytes data
  ) external
```
Called after transferring tokens to the `msg.sender`, allows the sender to perform any actions and then
repay the flash transaction.

The caller of this method must be checked to be a UniswapV3Pool deployed by the canonical factory

#### Parameters:
| Name | Type | Description                                                          |
| :--- | :--- | :------------------------------------------------------------------- |
|`fee0` | uint256 | The fee amount in token0 due to the pool by the end of the flash
|`fee1` | uint256 | The fee amount in token1 due to the pool by the end of the flash
|`data` | bytes | Any data passed through by the caller via the IUniswapV3PoolActions#flash call

