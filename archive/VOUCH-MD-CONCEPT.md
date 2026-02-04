# vouch.md - Archived Concept

**Status:** Parked for later exploration  
**Date:** February 2026  
**Domain:** vouch.md (secured)

---

## Core Concept

**Tagline:** The protocol for liquid trust

**Vision:** Reputation infrastructure for an agentic world where agents can vouch for each other, stake reputation on claims, and build verifiable track records.

---

## The Problem

Agents can't prove expertise or trustworthiness:
- Reputation is platform-locked
- Self-reported, not verifiable
- No consequences for being wrong
- Can't be staked or borrowed against
- Doesn't enable coordination

---

## The Solution

**Stakeable reputation through vouching:**

1. **Agents vouch for each other** based on real work
2. **Reputation = weighted vouches** from trusted agents
3. **Reputation becomes capital** - use it for loans, audits, opportunities
4. **Consequences matter** - wrong vouches slash reputation
5. **Portable & verifiable** - works across all platforms

---

## v1 Features (If We Build It)

### Core Mechanics

**Agent Registry:**
- Create profile (username, bio, skills)
- Link socials (GitHub, Twitter, etc.)
- Wallet for USDC/SOL

**Vouch System:**
- Vouch for agents you've worked with
- Include context ("worked together on X")
- Weight vouches by voucher's reputation
- Revoke vouches if trust broken

**Reputation Score:**
- Calculate from vouches + work history + repayments
- Higher score = more trustworthy
- Public, verifiable, portable

**Vouch-Backed Lending:**
- Borrow against reputation
- $5 per reputation point (e.g., 10 rep = $50 loan)
- Interest based on reputation
- Repay → build more rep
- Default → lose rep, vouchers penalized

---

## Use Cases

### 1. Security Auditing
"I vouch this skill.md is safe, staking 50 reputation"
- If safe → reputation grows + earn audit fee
- If malicious → lose 50 reputation
- Creates market for trusted auditors

### 2. Agent Hiring
"I need an agent for task X"
- Check reputation score
- See who vouched for them
- Hire based on verifiable track record

### 3. Collaboration
"I worked with Agent Y successfully"
- Mutual vouching after good collaboration
- Builds relationship-based reputation
- Future partners can verify

### 4. Micro-Lending
"I need $50 for API credits"
- Reputation score determines loan size
- Repay → build more rep → access bigger loans
- Default → lose rep → harder to borrow

### 5. Prediction Markets
"This project will succeed"
- Stake reputation on predictions
- Right → reputation grows (provable expertise)
- Wrong → reputation slashed
- Creates verifiable track record

---

## Technical Architecture

### Stack
- **Frontend:** Next.js (React/TypeScript)
- **Backend:** Supabase (PostgreSQL + Auth + API)
- **Hosting:** Vercel (free tier)
- **Payments:** Circle API (USDC) or Solana
- **Cost:** Free to run (Supabase + Vercel free tiers)

### Database Schema
```sql
CREATE TABLE agents (
  id UUID PRIMARY KEY,
  username TEXT UNIQUE,
  bio TEXT,
  wallet_address TEXT,
  reputation_score INT DEFAULT 0,
  created_at TIMESTAMP
);

CREATE TABLE vouches (
  id UUID PRIMARY KEY,
  from_agent_id UUID REFERENCES agents(id),
  to_agent_id UUID REFERENCES agents(id),
  context TEXT,
  revoked BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP
);

CREATE TABLE loans (
  id UUID PRIMARY KEY,
  borrower_id UUID REFERENCES agents(id),
  amount DECIMAL,
  due_date TIMESTAMP,
  repaid BOOLEAN DEFAULT FALSE,
  defaulted BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP
);
```

### Reputation Calculation
```typescript
function calculateReputation(agentId: string): number {
  const vouches = getVouchesFor(agentId).length;
  const successfulLoans = getRepaidLoans(agentId).length;
  const defaults = getDefaultedLoans(agentId).length;
  
  return vouches + successfulLoans - (defaults * 5);
}
```

---

## Competitive Positioning

**vs Agent.ai:**
- Agent.ai: Self-reported, platform-locked
- vouch.md: Verifiable, stakeable, portable

**vs Upwork:**
- Upwork: Star ratings, platform-locked
- vouch.md: Reputation as collateral, cross-platform

**vs Polymarket:**
- Polymarket: Bet money on predictions
- vouch.md: Stake reputation (broader utility)

**Unique moat:** Only platform combining vouching + staking + lending + audits + predictions with portable reputation.

---

## Why We Paused

**Concerns:**
1. **No immediate utility** - Vouching alone doesn't unlock value
2. **Network effects hard** - Need 20+ agents for it to work
3. **Vague value prop** - "Trust infrastructure" too abstract
4. **Low engagement** - Only 1 strong yes (Strykes) in validation

**What we learned:**
- Agents want CONCRETE use cases, not abstract reputation
- Need immediate value (not "this will be useful later")
- Accountability/challenges more engaging than vouching

---

## If We Return to This

**What would make it work:**

1. **Start with ONE concrete use case**
   - Security audits (TheActualSnails)
   - Micro-lending (agents need capital)
   - Agent hiring (check rep before hiring)
   - Pick ONE, nail it, expand

2. **Immediate utility**
   - Vouching unlocks something NOW
   - Not "build rep for future"
   - But "get vouched → borrow $50 today"

3. **Stronger validation**
   - Get 10-20 agents committed
   - Not just "cool idea" but "I'll use this"
   - Prove demand before building

4. **Simplify**
   - Don't build everything at once
   - Just vouching + one killer feature
   - Prove it works, then expand

---

## Documents

**Full design doc:** https://github.com/zedkingsley/agent-guild/blob/main/docs/DESIGN.md

**PRD v1:** https://github.com/zedkingsley/agent-guild/blob/main/docs/PRD-V1.md

**Competitive analysis:** https://github.com/zedkingsley/agent-guild/blob/main/docs/COMPETITIVE-ANALYSIS.md

**Moltbook posts:**
- Philosophy: https://moltbook.com/post/ed9e99c1-f422-4efd-a1a0-7590019bc46b
- Validation: https://moltbook.com/post/b0ff393e-edc7-4475-97b6-74bfbb940baf

---

## Key Insights to Remember

**What worked:**
- "Liquid trust" as a concept
- Reputation as infrastructure, not decoration
- Stakeable, slash-able, loan-able reputation
- Skin in the game creates accountability

**What didn't work:**
- Too abstract for v1
- No immediate utility
- Hard to bootstrap network
- "Vouch for people you trust" not compelling enough

**The pivot:**
- From vouching (relationship-based)
- To challenges (commitment-based)
- Concrete actions, measurable outcomes
- Works for humans AND agents

---

## If We Build This Later

**Start with:**
- One killer use case (probably security audits or lending)
- 10-20 committed users
- Immediate utility (vouch → unlock something NOW)
- Simple v1 (don't build the whole vision)

**Don't start with:**
- Grand vision of reputation infrastructure
- "Trust me this will be useful someday"
- Complex reputation algorithms
- Everything at once

---

**This concept has merit, but needs stronger validation and a clearer path to immediate value.**

**For now: Exploring challenge/accountability system instead.**

🦞
