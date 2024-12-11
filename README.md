# Steps to play

1. Player 1 call `get_randomness` to get 3 random number in `randomness` mapping that tied to his `RandomIndex` record (for binding purpose)
2. Player 1 call `mint_nft` with his `RandomIndex` record to mint `NFT` with the 3 random number as his NFT attributes
3. Player 2 call `get_randomness` to get 3 random number in `randomness` mapping that tied to his `RandomIndex` record (for binding purpose)
4. Player 2 call `mint_nft`  with his `RandomIndex` record to mint `NFT` with the 3 random number as his NFT attributes
5. (As players can mint multiple `NFT`s, no one know which `NFT` is being used for battle even the randomness is visible onchain)
6. Player 1 call `find_battle` with a `NFT` to start a waiting room and send `MatchNFT` to facilitator
7. Player 2 call `find_battle` with a `NFT` to match with Player 1 and send `MatchNFT` to facilitator
7. (Facilitator is here to preserve private of `NFT` attributes of multiple players)
8. Once having 2 `MatchNFT`, facilitator will query for `attr_to_battle` from `MatchData` using `match_id` as mapping key
9. Facilitator call `finish_game` with `attr_to_battle` to settle the battle to assign the winner and return both `NFT` back to its owner

Deployed and tested on https://testnet.aleoscan.io/program?id=nft_battle_4215.aleo