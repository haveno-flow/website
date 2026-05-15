## How do I get started?
tags: Getting Started

**1. Install and back up seed phrase**

Download and install HavenoFlow. On first launch, a Monero wallet is automatically created and embedded in the app. Open 'Settings → Wallet' and back up your seed phrase before doing anything else. This seed phrase can be used to access your XMR in any Monero-compatible wallet.

**2. Fund your wallet**

XMR is the base currency of HavenoFlow, you will need some before you can trade. If you don't have any yet, use the 'No Deposit' filter in the order book to find listings where you can acquire up to 1.5 XMR without a deposit.

**3. Add payment accounts**

Go to 'Settings → Payment Accounts' and add an account for each cryptocurrency you want to trade. This registers the addresses where you will receive funds when a trade completes.

**4. Place or take an offer**

You have two options:

- Taker — browse the order book and accept an existing offer.
- Maker — post your own offer for others to take.

Either way, a security deposit in XMR is required to open a trade. It is held in escrow and returned when the trade completes. If you are buying XMR, you post the deposit. If you are selling XMR, you post the deposit plus the XMR being sold.

Once both sides commit, the app coordinates the rest. The XMR seller's payment account details — the address where they'll receive the other crypto — are shared with the buyer, who sends the funds. Once the seller confirms receipt, the XMR is released from escrow and both deposits are returned.

## How do I secure my wallet?
tags: Security & Privacy

When you first open HavenoFlow, before you do anything else, set a password and write down your seed phrase. The seed phrase is everything — it is the master key to your funds. If your device is lost, stolen, or broken, you can restore your wallet and access your XMR on any Monero-compatible wallet. This works regardless of whether HavenoFlow is running, available, or even exists. Your XMR is your XMR, HavenoFlow is just one interface you can use it with.

## What is a security deposit?
tags: Getting Started

Before a trade begins, both parties lock a small amount of XMR into a shared multisig wallet as a security deposit. It is not a fee — it is returned to you when the trade completes successfully. Its purpose is to discourage bad actors: if you abandon a trade or act dishonestly, you risk losing your deposit.

## What are arbitrators? Why do you need them?
tags: Getting Started

Arbitrators are the last line of dispute resolution. If two traders can't complete a trade — after first attempting to settle it themselves — an arbitrator can step in and release or return funds based on the circumstances. Arbitrators never have custody of your funds. Each trade uses a 2-of-3 multisig wallet where the arbitrator holds only one of three keys, and two keys are always required to move anything.

Arbitrators are also what prevents HavenoFlow from being fully trustless — you still have to trust that the arbitrator acts fairly. Being crypto-to-crypto only was one deliberate step toward reducing this problem: disputes in fiat trading often come down to unprovable he-said-she-said situations that require a high degree of arbitrator trust and discretion. Crypto-to-crypto disputes are largely verifiable on-chain. Did the payment arrive? The blockchain knows. The arbitrator's job here is mostly straightforward. Over time, the goal is to move toward fully programmatic solutions that remove the need for human arbitrators entirely. For now they're a useful and necessary part of the network — but also a necessary evil HavenoFlow intends to eliminate.

## Which cryptocurrencies are supported?
tags: Other

Currently HavenoFlow supports:

- Monero (XMR)
- Bitcoin (BTC)
- Ether (ETH)
- Litecoin (LTC)
- Tether USD (USDT)
- Dai Stablecoin (DAI)
- Tron (TRX)
- Solana (SOL)
- Ripple (XRP)
- Dogecoin (DOGE)
- Cardano (ADA)
- Zcash (ZEC)

## Do I need to create an account?
tags: Getting Started

No. HavenoFlow has no accounts, no sign-up, and no identity verification. Download the app and you're ready to trade. Your wallet lives on your own device — HavenoFlow never holds your funds or your data.

## Are fiat currencies or precious metals supported?
tags: Other

At this time, HavenoFlow only supports crypto-to-crypto trading — for example trading XMR for BTC. PayPal, Cash by Mail, Gold (XAU), and similar options are not available. These options account for a tiny fraction of trading volume on Haveno networks, while also accounting for a large portion of the problems. Excluding them allows HavenoFlow to focus on providing the best possible crypto-to-crypto experience.

## What are the trading fees?
tags: Getting Started

HavenoFlow currently charges no trading fees. 0% maker and 0% taker.

## What happens to my funds if HavenoFlow shuts down?
tags: Security & Privacy

Nothing, as long as you have your seed phrase. HavenoFlow is, at its core, a Monero wallet with a trading interface built on top — your funds live on your own device, not on any server. If the network disappeared tomorrow, you would simply import your seed into any Monero wallet and your funds would be right there, untouched. The platform going away cannot take your money with it.

## How does a trade work?
tags: Getting Started

**1. Find or post an offer**

Browse the order book and take an existing offer, or post your own.

**2. Commit deposits**

Both sides lock a security deposit in XMR into a 2-of-3 multisig escrow wallet shared between buyer, seller, and an arbitrator. If you are buying XMR, you lock in the deposit. If you are selling XMR, you lock in the deposit plus the XMR being sold.

**3. Send payment**

The XMR seller's payment account details are shared with the buyer. The buyer sends the funds and marks payment as sent in the app.

**4. Complete the trade**

The seller confirms receipt. The XMR is released from escrow and both deposits are returned.

## Is HavenoFlow available in my country?
tags: Other

HavenoFlow is a decentralized network with no central authority restricting access by region. All traffic runs through Tor, so there is no server that can block you by location. However, cryptocurrency laws vary widely — it is your responsibility to understand and comply with the regulations in your jurisdiction.

## How long does a trade take?
tags: Getting Started

It depends on the payment method. Instant methods typically wrap up within an hour; standard methods are usually done within 24 hours. Those aren't hard guarantees though — on-chain confirmation times aren't included in the clock and can add some time. If a trade hasn't completed within the expected window, you can open a dispute and an arbitrator will step in.

## Does HavenoFlow collect or store any data about me?
tags: Security & Privacy

**The HavenoFlow network**

Within what HavenoFlow controls, no data of any kind is collected, logged, or stored — not your IP address, not your trading activity, not your identity. There is nothing to hand over, sell, or leak, because nothing is ever recorded.

**Website hosting**

This website is served by a third-party hosting provider widely regarded as trustworthy, transparent, and respectful of user privacy. By the nature of how web hosting works, the provider has access to data generated by your visit — and they acknowledge logging visitor IP addresses for security purposes. 

**Third-party services**

HavenoFlow makes use of various external services — including GitHub, chat platforms, and social media. These are outside HavenoFlow's control. Each may log or store data independently of HavenoFlow, and HavenoFlow has no visibility into or influence over what they collect.

## Can I buy Monero (XMR) without a security deposit?
tags: Getting Started

Yes. Click the "No Deposit" button at the top of the order book to filter to these listings. Up to 1.5 XMR is available this way, making it possible for new users who don't yet hold any XMR to get started.

## What is Haveno? What is the difference between Haveno and HavenoFlow?
tags: Other

Haveno is open-source software for building a decentralized, non-custodial peer-to-peer Monero exchange. Anyone can use it to run their own network. HavenoFlow is this project's network — built on top of Haveno. Think of Haveno as the engine and HavenoFlow as the network running on it. You can learn more about Haveno at [haveno.exchange](https://haveno.exchange/).

## What do I do if a trade goes wrong?
tags: Getting Started

First, try to resolve it with your trading partner using the built-in chat. If that fails, you can open a dispute, which summons an arbitrator. The arbitrator will review the trade history and any evidence both sides submit, then make a decision. Opening a dispute is a last resort — most issues are resolved in chat without needing one.

## Is KYC required?
tags: Security & Privacy

"No" is the short answer. The long answer: HavenoFlow is a decentralized network, so in terms of the network itself — asking you to KYC is not even really possible. All trading is done peer-to-peer. While your trading partner could theoretically ask you to KYC, that is something that typically only happens with fiat trading — which HavenoFlow does not support. If it did ever happen on HavenoFlow, you can open a dispute and the arbitrator will cancel the trade without penalty.

## Who should I contact for technical questions about Haveno?
tags: Other

For deep technical questions — about the software, the trade protocol, Tor, or anything under the hood — the Haveno project itself might be a better starting point. They maintain it, so they'll likely have answers HavenoFlow doesn't. You can find them at [haveno.exchange](https://haveno.exchange/).

## What is Bisq and how does Haveno differ from it?
tags: Other

Bisq is a decentralized peer-to-peer exchange that Haveno forked from. The core difference is that Bisq is built on Bitcoin and Haveno is built on Monero. Bitcoin transactions are fully traceable on a public blockchain — blockchain surveillance companies actively flag Bisq trades, and there are documented cases of users having exchange accounts frozen after moving funds out of Bisq. Monero was chosen because privacy is built into the protocol itself. Every Monero transaction hides the sender, receiver, and amount by default. That makes it the right foundation for an exchange that takes privacy seriously. 

For a full breakdown, [the Haveno team covers it in detail here](https://haveno.exchange/faq/#why-a-new-platform-what-are-the-key-differences-compared-to-bisq).
