# Steps to play

1. Player 1 call `get_randomness` to get 3 random number in `randomness` mapping that tied to his `RandomIndex` record (for binding purpose)
2. Player 1 call `mint_nft` with his `RandomIndex` record to mint `NFT` with the 3 random number as his NFT attributes
3. Player 2 call `get_randomness` to get 3 random number in `randomness` mapping that tied to his `RandomIndex` record (for binding purpose)
4. Player 2 call `mint_nft`  with his `RandomIndex` record to mint `NFT` with the 3 random number as his NFT attributes
5. (As players can mint multiple `NFT`s, no one know which `NFT` is being used for battle even the randomness is visible onchain)
6. Player 1 call `find_battle` with a `NFT` to start a waiting room and send `MatchNFT` to facilitator
7. Player 2 call `find_battle` with a `NFT` to match with Player 1 and send `MatchNFT` to facilitator
7. (Facilitator is here to preserve private of `NFT` attributes of multiple players)
8. Once having 2 `MatchNFT`, facilitator will call `finish_game` to settle the battle to assign the winner and return both `NFT` back to its owner
9. (Issue) `finish_game` will fail because assigning values out of if statements scope in transition does not work as intended (variable will always get assigned with the value at the last branch).

Deployed and tested on https://testnet.aleoscan.io/program?id=nft_battle_4214.aleo