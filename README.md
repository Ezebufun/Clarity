# Clarity

**Know what you're signing before you sign it.**

Clarity decodes raw blockchain transaction calldata into plain-English explanations and risk assessments, so users (and software agents) can understand what a transaction will actually do before approving it.

## The problem

Wallet prompts show hex data and cryptic function names. Users approve token drains, unlimited allowances, and malicious contract calls because they can't tell what they're signing. As AI agents start moving money on their own, this gets more dangerous: an agent needs a safety layer that checks intent before executing.

## What it does

1. **Decodes** transaction calldata into human-readable function calls and parameters.
2. **Scores risk** using rule-based checks (unlimited approvals, unknown contracts, suspicious recipients, unusual value transfers).
3. **Explains** the result in plain English with an AI explanation layer.
4. **Returns a verdict**: allow, warn, or block.

## Example

```
This transaction gives contract 0xAbC...123 permission to spend
ALL of your USDC, forever.
Risk: HIGH. Unlimited token approval to an unverified contract.
Recommendation: Do not sign. Approve a specific amount instead.
```

## Tech stack

- Next.js, React, Tailwind CSS
- Transaction decoding and risk scoring backend
- LLM-powered explanation layer
- EVM-compatible chains

## Getting started

```bash
git clone https://github.com/Ezebufun/Clarity.git
cd Clarity
npm install
cp .env.example .env.local
npm run dev
```

Open http://localhost:3000

## Roadmap

- [ ] Complete the UI phase
- [ ] Multi-chain support
- [ ] Agent guardrail API: let AI agents check a payment or transaction before executing
- [ ] Browser extension for in-wallet warnings

## Author

Built by **Tochukwu**: Web3 developer, QA tester, and motion designer.
