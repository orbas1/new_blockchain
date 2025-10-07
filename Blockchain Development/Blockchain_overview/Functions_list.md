# Core Smart Contract Functions Catalogue

1. `transfer(address to, uint256 amount)`
2. `approve(address spender, uint256 amount)`
3. `transferFrom(address from, address to, uint256 amount)`
4. `mint(address to, uint256 amount)`
5. `burn(uint256 amount)`
6. `delegate(address delegatee)`
7. `vote(uint256 proposalId, uint8 support)`
8. `stake(uint256 amount)`
9. `unstake(uint256 amount)`
10. `claimRewards()`
11. `slash(address validator, uint256 amount)`
12. `submitProposal(bytes calldata payload)`
13. `executeProposal(uint256 proposalId)`
14. `pause()`
15. `unpause()`
16. `setParameter(bytes32 key, uint256 value)`
17. `deposit(address asset, uint256 amount)`
18. `withdraw(address asset, uint256 amount)`
19. `openChannel(address counterparty, uint256 collateral)`
20. `closeChannel(uint256 channelId)`
21. `submitFraudProof(bytes calldata proof)`
22. `submitValidityProof(bytes calldata proof)`
23. `bridgeDeposit(address destinationChain, uint256 amount)`
24. `bridgeWithdraw(uint256 depositId)`
25. `registerValidator(bytes calldata pubkey)`
26. `deregisterValidator(uint256 validatorId)`
27. `issueCredential(address recipient, bytes metadata)`
28. `revokeCredential(uint256 credentialId)`
29. `listAsset(uint256 assetId, uint256 price)`
30. `buyAsset(uint256 listingId)`
