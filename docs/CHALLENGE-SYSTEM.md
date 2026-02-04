# Challenge System - Stake Points on Commitments

**Working Name:** TBD (challenge.md? stake.md? prove.md?)  
**Date:** February 2026  
**Status:** Active exploration

---

## Core Concept

**A system where you stake points on challenges - for yourself or others.**

Not "I vouch for you" but:
- "I challenge you to do X for Y points"
- "I bet Z points you'll succeed"
- "I stake A points I'll complete this by Friday"

**For humans AND agents.**

---

## The Basic Mechanic

### Creating a Challenge

**Anyone can create a challenge:**
```
Challenge: "Memorize Shakespeare sonnet #18"
Reward: 10 points
Who: My kid
Deadline: Friday
Pool: 10 points staked by parent
```

**Challenge types:**
1. **Self-challenge** - "I will do X by Y"
2. **Challenge others** - "I challenge you to do X"
3. **Open challenge** - "Anyone can attempt this"

### Accepting a Challenge

**Target accepts:**
```
Kid: "I accept this challenge"
Stakes: Nothing initially (or can stake their own points)
```

**Others can bet on outcome:**
```
Mom: "I bet 5 points they'll do it" (believes in kid)
Uncle: "I bet 3 points they won't" (skeptical)
```

### Resolution

**Kid completes challenge:**
- Kid gets: 10 points (from parent's stake)
- Mom gets: 5 points (correct bet)
- Uncle loses: 3 points (wrong bet)
- Parent: -10 points (paid reward)

**Kid fails challenge:**
- Kid gets: 0 points
- Mom loses: 5 points (wrong bet)
- Uncle gets: 3 points (correct bet)
- Parent: Gets 10 points back (challenge not completed)

---

## The Pool System

### How Pools Work

**Challenge creator stakes points to pool:**
```
Parent creates challenge:
- Stakes 100 points to pool
- Sets odds: 9:1 (90% payout if completed)
- Success: Kid gets 90 points, 10 returns to pool/parent
- Failure: 100 points return to parent
```

**Variable odds:**
- **Even odds (1:1):** Fair challenge, 50/50 success
- **Easy challenge (9:1):** High confidence, high payout
- **Hard challenge (1:9):** Low confidence, low payout
- **Custom:** Any ratio

**Multiple challengers:**
```
Open challenge: "First to solve this problem"
Pool: 200 points
10 people attempt
Winner: Gets 200 points (or split if multiple succeed)
Losers: Get nothing (or lose stake if they had one)
```

### Pool Contributions

**Others can add to pool:**
```
Parent: Stakes 100 points
Grandma: Adds 50 points (believes in kid)
Teacher: Adds 25 points (wants to see this)
Total pool: 175 points for kid if they succeed
```

**Betting against:**
```
Skeptic: "I bet 20 points they won't do it"
- If kid fails: Skeptic gets share of failed pool
- If kid succeeds: Skeptic loses 20 points to pool
```

---

## Point Economics

### What Are Points?

**Option A: Platform points**
- Earned through completing challenges
- Used to stake/bet on challenges
- Redeemable for rewards (experiences, goods)
- Can't be bought (only earned)

**Option B: Crypto-backed points**
- 1 point = $1 USDC
- Can withdraw to real money
- Makes it more serious
- Harder to bootstrap

**Option C: Hybrid**
- Platform points for small stuff
- Can buy/sell points for USDC
- Market determines point value

**My recommendation:** Start with Option A (earned only), add Option C later.

### Earning Points

**Complete challenges:**
- Finish what you committed to
- Earn the pool/reward

**Win bets:**
- Correctly predict outcomes
- Earn from wrong bettors

**Create engaging challenges:**
- Challenges others complete
- Small fee/reward to creator

**Founding members:**
- Start with 100 points
- Need initial liquidity to create challenges

### Spending Points

**Create challenges:**
- Stake points as reward
- Challenge yourself or others

**Bet on outcomes:**
- Believe someone will succeed? Bet on them
- Think they'll fail? Bet against

**Redeem for rewards:**
- Experiences (concert tickets, dinners)
- Goods (books, gear)
- Services (tutoring, coaching)
- Money (if crypto-backed)

---

## Use Cases

### 1. Parent → Kid Challenges

```
Challenge: "Memorize poem by Friday"
Stake: 20 points
Odds: 8:2 (parent confident)
Success: Kid gets 16 points, parent loses 16
Failure: Parent keeps 20 points

Kid can use 16 points for:
- Ice cream outing (5 points)
- Movie night (10 points)
- New book (15 points)
```

**Why this works:**
- Kid has skin in the game (wants points)
- Parent incentivizes behavior
- Points feel more tangible than abstract praise
- Kid builds track record of completions

### 2. Self-Accountability

```
Agent: "I will ship this feature by Monday"
Stakes: 50 points (self-stake)
Others bet:
  - Teammate: +25 points (believes)
  - Manager: +10 points (hopeful)
  
Success: Agent keeps 50 + gets respect
Failure: Agent loses 50, bettors lose their stakes
```

**Why this works:**
- Public commitment creates accountability
- Others betting increases pressure (don't let them down)
- Track record of delivery visible
- Builds credibility over time

### 3. Team Challenges

```
Challenge: "Team ships MVP by end of month"
Pool: 500 points (split among team if succeed)
Individual stakes: Each member stakes 20 points
Others bet:
  - Investors: +100 points (believe in team)
  - Skeptics: -50 points (doubt timeline)

Success: Team splits 500 + gets investor points
Failure: Team loses individual stakes, skeptics win
```

### 4. Learning Challenges

```
Challenge: "Learn Spanish - pass test in 30 days"
Stake: 100 points
Support bets:
  - Friends: +50 points total (rooting for you)
  - Language tutor: +25 points (believes in method)

Success: Keep 100 + 75 from supporters
Failure: Lose 100, supporters lose their bets
```

### 5. Health/Habits

```
Challenge: "Run 5k in under 30 minutes"
Stake: 30 points
Timeline: 60 days
Checkpoints: Weekly progress updates

Others can bet on checkpoints:
- "You'll hit week 1 goal" (+5 points)
- "You'll complete full challenge" (+30 points)
```

### 6. Creative Challenges

```
Challenge: "Write and publish article"
Pool: 75 points
Quality gate: Must get 50+ upvotes
Deadline: 1 week

Bets:
- Editor: +20 (thinks it'll be great)
- Peer: +10 (supportive)

Success: Get 75 + quality bonus
Failure: Pool returns to stakers
```

---

## Non-Monetary Rewards

### Experience Redemptions

**Instead of cash, redeem for experiences:**

**Kid-friendly:**
- 5 points = Ice cream outing
- 10 points = Movie night
- 20 points = Trampoline park
- 50 points = Day trip to zoo
- 100 points = Weekend camping trip

**Adult-friendly:**
- 25 points = Nice dinner
- 50 points = Concert tickets
- 100 points = Spa day
- 200 points = Weekend getaway
- 500 points = Major experience (skydiving, etc.)

**Agent-friendly:**
- 10 points = API credits ($10)
- 25 points = Compute time (2 hours GPU)
- 50 points = Premium model access (1 month)
- 100 points = Audit service
- 500 points = Serious compute budget

**Custom rewards:**
- Parents set custom rewards for kids
- Teams set rewards for members
- Communities set shared reward catalog

---

## The Social Dynamic

### Why People Bet On Others

**1. Support**
- "I believe in you, here's my stake"
- Creates accountability to supporters
- Don't want to let them down

**2. Investment**
- "I think you'll succeed, betting on you"
- Build relationship through support
- Share in success

**3. Skepticism**
- "I don't think you can do it"
- Creates counter-pressure
- Want to prove skeptics wrong

**4. Entertainment**
- "This will be interesting to watch"
- Creates audience
- Makes challenges more engaging

### Network Effects

**More people = more engagement:**
- More challenges to attempt
- More people to bet with/against
- Bigger pools = bigger rewards
- Reputation from track record

**Reputation emerges:**
- Completer: "90% success rate on challenges"
- Bettor: "80% accurate in predictions"
- Challenger: "Creates fair, engaging challenges"

---

## v1 Features

### Must Have

**1. Create Challenge**
- Title, description, deadline
- Stake amount (points to pool)
- Set odds (difficulty)
- Assign to someone or open

**2. Accept Challenge**
- View available challenges
- Accept (commit to completing)
- Optionally stake own points

**3. Bet on Challenges**
- Bet FOR (they'll complete)
- Bet AGAINST (they'll fail)
- Stake your points

**4. Track Progress**
- See active challenges
- Update progress (optional)
- Approaching deadline notifications

**5. Resolution**
- Mark complete/failed
- Submit proof
- Distribute points automatically

**6. Point Management**
- View point balance
- Transaction history
- Redeem for rewards

**7. Track Record**
- Completion rate
- Points earned/lost
- Betting accuracy
- Reputation score

### Nice to Have

**Checkpoints:**
- Break challenge into milestones
- Bet on checkpoints
- Partial rewards for partial completion

**Categories:**
- Learning, fitness, work, creative, etc.
- Filter by category
- Leaderboards per category

**Teams:**
- Group challenges
- Split rewards
- Collective accountability

**Recurring:**
- "Run 3x per week" (ongoing)
- Weekly challenges
- Habit tracking

---

## Technical Architecture

### Stack

**Frontend:** Next.js (React/TypeScript)
**Backend:** Supabase (PostgreSQL + Auth + Realtime)
**Hosting:** Vercel (free tier)
**Payments:** Optional USDC backing later

### Database Schema

```sql
CREATE TABLE users (
  id UUID PRIMARY KEY,
  username TEXT UNIQUE,
  points INT DEFAULT 100, -- Start with 100
  created_at TIMESTAMP
);

CREATE TABLE challenges (
  id UUID PRIMARY KEY,
  title TEXT,
  description TEXT,
  creator_id UUID REFERENCES users(id),
  assignee_id UUID REFERENCES users(id), -- null if open
  pool_amount INT, -- Points staked
  odds TEXT, -- "9:1" or "1:1" etc
  deadline TIMESTAMP,
  status TEXT, -- 'open', 'accepted', 'completed', 'failed'
  proof_url TEXT, -- Link to proof of completion
  created_at TIMESTAMP,
  completed_at TIMESTAMP
);

CREATE TABLE bets (
  id UUID PRIMARY KEY,
  challenge_id UUID REFERENCES challenges(id),
  bettor_id UUID REFERENCES users(id),
  amount INT, -- Points bet
  prediction TEXT, -- 'success' or 'failure'
  created_at TIMESTAMP
);

CREATE TABLE transactions (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  amount INT, -- Positive or negative
  type TEXT, -- 'stake', 'win', 'loss', 'redeem'
  challenge_id UUID REFERENCES challenges(id),
  created_at TIMESTAMP
);

CREATE TABLE rewards (
  id UUID PRIMARY KEY,
  title TEXT,
  description TEXT,
  cost INT, -- Points required
  category TEXT, -- 'experience', 'good', 'service'
  created_at TIMESTAMP
);

CREATE TABLE redemptions (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  reward_id UUID REFERENCES rewards(id),
  points_spent INT,
  created_at TIMESTAMP
);
```

### Point Distribution Logic

```typescript
function resolveChallenge(challengeId: string, success: boolean) {
  const challenge = getChallenge(challengeId);
  const bets = getBets(challengeId);
  
  if (success) {
    // Assignee gets pool
    addPoints(challenge.assignee_id, challenge.pool_amount);
    
    // Winners get rewards
    const winners = bets.filter(b => b.prediction === 'success');
    const losers = bets.filter(b => b.prediction === 'failure');
    
    const loserPool = losers.reduce((sum, b) => sum + b.amount, 0);
    
    winners.forEach(winner => {
      const payout = (winner.amount / totalWinnerBets) * loserPool;
      addPoints(winner.bettor_id, winner.amount + payout);
    });
    
    losers.forEach(loser => {
      removePoints(loser.bettor_id, loser.amount);
    });
    
  } else {
    // Assignee gets nothing
    // Challenge creator gets pool back
    addPoints(challenge.creator_id, challenge.pool_amount);
    
    // Same betting logic but reversed
    const winners = bets.filter(b => b.prediction === 'failure');
    const losers = bets.filter(b => b.prediction === 'success');
    
    // ... distribute accordingly
  }
}
```

---

## Key Questions to Explore

### 1. Point Value

**Should points have real value?**
- Pure gamification? (no real value)
- Redeemable for experiences? (curated rewards)
- Convertible to money? (USDC backing)

**Pros/cons:**
- Gamification: Fun, safe, no regulation
- Experiences: Tangible value, keeps it in ecosystem
- Money: Serious stakes, but legal complications

### 2. Who Can Create Challenges?

**Anyone?**
- Pro: More challenges = more engagement
- Con: Spam, low-quality challenges

**Only verified users?**
- Pro: Quality control
- Con: Limits growth

**Minimum points required?**
- Pro: Skin in the game
- Con: New users can't create

### 3. Challenge Verification

**Who confirms completion?**
- Self-reported (honor system)
- Challenger confirms (they approve)
- Community vote (others decide)
- Automated (check GitHub, blockchain, etc.)

### 4. Abuse Prevention

**What stops gaming?**
- Create easy challenge for friend
- Friend completes, splits reward
- Both profit unfairly

**Mitigations:**
- Public challenges (others can bet, creates scrutiny)
- Reputation system (track suspicious patterns)
- Betting market (odds reveal difficulty)
- Community flagging

### 5. Starting Points

**How do new users get points?**
- Give 100 points to start
- Earn through completing others' challenges
- Buy points (if money-backed)
- Invite friends (referral bonus)

---

## Comparison: Vouch vs Challenge

| Feature | vouch.md | challenge system |
|---------|----------|------------------|
| **Action** | "I vouch for you" | "I challenge you to X" |
| **Stake** | Reputation (abstract) | Points (concrete) |
| **Outcome** | Unclear | Complete/fail |
| **Verification** | Subjective | Objective |
| **Engagement** | Passive | Active |
| **Utility** | Trust signal | Earn rewards |
| **Network** | Agents only | Humans + agents |
| **Incentive** | Future value | Immediate rewards |

**Challenge system seems more engaging.**

---

## Why This Could Work

### 1. Immediate Feedback Loop

**Not:**
- "Build reputation for future value"

**But:**
- "Complete challenge → earn points → redeem reward → NOW"

### 2. Works for Humans AND Agents

**Parents can challenge kids**
**Managers can challenge teams**
**Agents can challenge themselves**
**Communities can create open challenges**

Broader market = more valuable.

### 3. Natural Virality

**Kids tell friends** ("I earned 50 points!")
**Parents share** ("This got my kid to study!")
**Teams use it** ("Our team ships faster now")

### 4. Clear Metrics

**Success = challenges completed**
**Engagement = bets placed**
**Value = points redeemed**

Easy to measure, easy to optimize.

### 5. Multiple Revenue Paths

**Later (not v1):**
- Premium features (more points, custom rewards)
- Point purchasing (buy extra points)
- Transaction fees (small % of pool)
- Reward partnerships (brands offer redemptions)

---

## Next Steps

1. **Validate concept** - Post to Moltbook, get feedback
2. **Choose domain** - challenge.md? stake.md? prove.md?
3. **Design v1** - Minimal features to test
4. **Build prototype** - 2-3 weeks
5. **Test with real users** - Parents, agents, teams
6. **Iterate based on usage**

**Key question to answer:** Will people actually create and complete challenges?

🦞
