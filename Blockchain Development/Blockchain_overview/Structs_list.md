# Core Data Structures

1. `struct Validator { address operator; uint256 stake; uint256 commission; bool jailed; }`
2. `struct Delegation { address delegator; uint256 validatorId; uint256 shares; }`
3. `struct Proposal { uint256 id; address proposer; bytes metadata; uint64 startBlock; uint64 endBlock; }`
4. `struct Vote { uint256 proposalId; address voter; uint8 support; uint256 weight; }`
5. `struct Reward { uint256 epoch; address recipient; uint256 amount; }`
6. `struct Penalty { address validator; uint256 amount; string reason; }`
7. `struct Channel { uint256 id; address partyA; address partyB; uint256 balanceA; uint256 balanceB; }`
8. `struct BridgeDeposit { uint256 id; address depositor; uint256 amount; bytes destination; }`
9. `struct NFTMetadata { string uri; bytes32 checksum; uint256 royaltyBps; }`
10. `struct Order { uint256 id; address seller; uint256 assetId; uint256 price; bool active; }`
11. `struct ExecutionTrace { bytes32 txHash; bytes steps; uint256 gasUsed; }`
12. `struct TreasuryGrant { uint256 id; address recipient; uint256 amount; string milestone; }`
13. `struct Credential { uint256 id; address holder; string schema; uint64 issuedAt; bool revoked; }`
