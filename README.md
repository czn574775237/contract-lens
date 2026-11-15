# contract-lens

A visual explainer for **option contract adjustments** — what happens to your contract when the underlying company gets acquired, split, or pays a special dividend.

Most options material describes adjustments in prose. This renders them as a **punch card**: three slots (underlying / strike / deliverable) and a punch head that rewrites one slot at a time.

## Why

If you hold a long-dated option through an M&A event, the contract you own afterwards is often not the contract you bought:

| Event | What changes |
|---|---|
| All-cash acquisition | Deliverable becomes cash (cash-settled or basket) |
| Stock-for-stock | Deliverable becomes *N* shares of the acquirer |
| 2:1 split | Strike halves, multiplier doubles — value unchanged |
| Special dividend | Deliverable gains a cash component |

OCC issues an adjustment memo for each corporate action. Brokers rarely surface it, and most holders find out at expiry.

## Demo

Open `demo/index.html` in a browser. No build step, no dependencies.

Four scenarios, click to switch. The punch head moves to the affected slot and the readout updates.

## Roadmap

- [ ] React component (`src/ContractCard.tsx`)
- [ ] Real adjustment memos as data fixtures
- [ ] Merged-contract (post-adjustment) calculator
- [ ] Export to SVG / PNG

## License

MIT
