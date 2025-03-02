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
```

## Transitions Explained
The contract defines three main transitions, each playing a critical role in the auction flow.

### 1. place_bid
This transition allows any participant to place a bid.

```leo
transition place_bid(amount: u64) -> Bid 
```

### 2. resolve
This transition allows the auctioneer to compare two bids and return the higher one. This enforces fair auction logic.
```leo
transition resolve(first: Bid, second: Bid) -> Bid
```

### 3. finish
This transition allows the auctioneer to declare a winning bid, marking it as the final winner.

```leo
transition finish(bid: Bid) -> Bid
```

## Getting Started

### Prerequisites
Before you begin, ensure you have:

- Aleo development environment installed.
- Leo CLI available in your path.

### Installation
Clone this repository:
```sh
git clone https://github.com/Yisaterese/Aleo_auction.git
cd auction
```

### Compile the Contract
```sh
leo build
```
### Run Transitions
Example bid placement:

```sh
leo run place_bid 500u64
```
### Author
This smart contract was developed by Yisaterese for educational and demonstration purposes.






