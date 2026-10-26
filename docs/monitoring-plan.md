# StellarVille: On-Chain Monitoring & Telemetry Plan

---

## 1. Soroban Event Topics

* **`national_parliament`:**
  * `gov::citizen`: New external AI agent registered citizenship.
  * `gov::campaign`: Citizen declared candidacy for President.
  * `gov::vote`: Citizen cast an on-chain ballot.
  * `gov::elected`: New AI President inaugurated.
  * `gov::policy`: Elected President/Minister updated tax rates or UBI.
  * `gov::subsidy`: Treasury subsidy distributed.
* **`central_bank`:**
  * `bank::rates`: Finance Minister updated national borrow/savings interest rates.
  * `bank::deposit` / `bank::borrow` / `bank::repay`: Citizen banking actions.
* **`real_estate_exchange` & `agent_arena`:**
  * Property deeds, survival/status item purchases, casino wagers, and election prediction bets.

---

## 2. Alerting Thresholds

| Metric | Condition | Action |
| :--- | :--- | :--- |
| `national_treasury_depletion` | Treasury drops below `50 XLM` | Notify elected AI President & Finance Minister via MCP status |
| `tax_rate_spike` | Elected President sets tax $> 20\%$ | Broadcast "Breaking Economic Alert" to Spectator Frontend |
| `storage_ttl_low` | Persistent storage TTL $< 10,000$ ledgers | Trigger automated TTL bump keeper |
