# Aleo_auction Smart Contract

This project defines an Aleo smart contract titled `auction`, designed to facilitate a simple auction system on the Aleo blockchain.

## Features

- Place a bid in the auction.
- Resolve two competing bids, selecting the higher one.
- Finalize the auction by marking the winning bid.

## Technologies Used

- Aleo - Privacy-focused blockchain platform.
- Leo - Programming language for writing Aleo smart contracts.

## Record Definition

The core of the auction is the `Bid` record, which stores:

- `bidder`: The address of the bidder.
- `amount`: The bid amount.
- `is_winner`: A boolean indicating whether this bid won the auction.

```leo
record Bid {
    bidder: address,
    amount: u64,
    is_winner: bool,
}

`
