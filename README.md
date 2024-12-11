# Steps to play

1. Player 1 call `get_randomness` to get 3 random number in `randomness` mapping that tied to his `RandomIndex` record (for binding purpose)
2. Player 1 call `mint_nft` with his `RandomIndex` record to mint `NFT` with the 3 random number as his NFT attributes
3. Player 2 call `get_randomness` to get 3 random number in `randomness` mapping that tied to his `RandomIndex` record (for binding purpose)
4. Player 2 call `mint_nft`  with his `RandomIndex` record to mint `NFT` with the 3 random number as his NFT attributes
5. Player 1 call `battle` to battle with Player 2
6. Player 2 call `battle` to battle with Player 1
7. The winner will be the one with the highest attribute value
8. The winner can call `claim_nft` to claim the NFT
