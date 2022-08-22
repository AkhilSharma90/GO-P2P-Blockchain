We built a blockchain recently on my youtube channel.
Since then, I've added 2 projects on my github account - one containing proof of work blockchain and the other containing proof of stake blockchain.

So, now we know how to build a blockchain and how the two most popular consensus mechanisms work. But blockchains themselves need to be propagated across peers.

This means - communication across multiple peers. In this example, I wanted to show that.
You need to open up multiple terminals to see this happen.

1. 1st terminal - `go run main.go -secio -l 10000`
2. 2nd terminal - `go run main.go -l 10001 -d /ip4/127.0.0.1/tcp/10000/ipfs/QmZ8NayvdXc2U2A1cwh9qGaHK7uxXXVrZQEYwDqbfFydfj -secio`
3. 3rd teminal - `go run main.go -l 10002 -d /ip4/127.0.0.1/tcp/10001/ipfs/QmRAj9JJVKRJmWHbDKzvzKDVVFPWxuWYio3bPym4SgGPgF -secio`

The actual hashes for you will be different and they will be shown in your terminal. So, use those instead in point 2 and 3 and you will be asked for BPM just like on the proof of work blockchain example.
Your blockchain will be broadcasted to all terminals. (don't forget to keep the terminals open! LOL!)