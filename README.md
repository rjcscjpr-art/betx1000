
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Online Betting – Real moneyOnly</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="betting site with Real Money." />

  <style>
    :root {
      --bg: #0b1020;
      --bg-card: #111827;
      --accent: #22c55e;
      --accent-soft: rgba(34, 197, 94, 0.1);
      --accent-2: #3b82f6;
      --accent-2-soft: rgba(59, 130, 246, 0.12);
      --text: #e5e7eb;
      --muted: #9ca3af;
      --danger: #f97373;
      --danger-soft: rgba(248, 113, 113, 0.12);
      --radius-lg: 1.25rem;
      --shadow-soft: 0 18px 40px rgba(15, 23, 42, 0.65);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Inter", sans-serif;
    }

    body {
      background: radial-gradient(circle at top, #1e293b 0, #020617 55%);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      align-items: stretch;
      justify-content: center;
      padding: 1.5rem;
    }

    .app {
      width: 100%;
      max-width: 1200px;
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 1.5rem;
    }

    @media (max-width: 900px) {
      body {
        padding: 1rem;
      }

      .app {
        grid-template-columns: 1fr;
      }
    }

    .card {
      background: linear-gradient(145deg, rgba(15,23,42,0.96), rgba(15,23,42,0.96));
      border-radius: var(--radius-lg);
      border: 1px solid rgba(148, 163, 184, 0.3);
      box-shadow: var(--shadow-soft);
      padding: 1.2rem 1.2rem 1.1rem;
    }

    .card-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.7rem;
      gap: 0.75rem;
    }

    .tagline {
      font-size: 0.75rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.2rem;
    }

    h1 {
      font-size: 1.65rem;
      font-weight: 700;
    }

    .subtext {
      font-size: 0.85rem;
      color: var(--muted);
      max-width: 24rem;
    }

    .badge {
      padding: 0.25rem 0.7rem;
      border-radius: 999px;
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      border: 1px solid rgba(55, 65, 81, 0.9);
      color: #e5e7eb;
      background: rgba(15,23,42,0.9);
      white-space: nowrap;
    }

    .badge--warning {
      border-color: rgba(248, 113, 113, 0.8);
      color: #fecaca;
      background: rgba(127, 29, 29, 0.65);
    }

    /* Balance section */
    .balance-card {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 0.75rem;
      padding: 0.7rem 0.85rem;
      border-radius: 1rem;
      background: radial-gradient(circle at top left, rgba(34, 197, 94, 0.2), rgba(15,23,42,0.9));
      border: 1px solid rgba(34, 197, 94, 0.4);
      margin-bottom: 0.9rem;
    }

    .balance-value {
      font-size: 1.35rem;
      font-weight: 700;
    }

    .balance-label {
      font-size: 0.8rem;
      color: var(--muted);
    }

    .btn {
      border-radius: 999px;
      border: none;
      padding: 0.4rem 0.85rem;
      font-size: 0.8rem;
      font-weight: 600;
      cursor: pointer;
      background: var(--accent-2);
      color: white;
      box-shadow: 0 10px 30px rgba(37, 99, 235, 0.5);
      transition: transform 0.1s ease, box-shadow 0.15s ease, background 0.15s ease;
      white-space: nowrap;
    }

    .btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 12px 40px rgba(37, 99, 235, 0.6);
      background: #1d4ed8;
    }

    .btn:active {
      transform: translateY(1px);
      box-shadow: 0 6px 18px rgba(37, 99, 235, 0.5);
    }

    .btn--ghost {
      background: transparent;
      color: var(--text);
      border: 1px solid rgba(148, 163, 184, 0.7);
      box-shadow: none;
    }

    .btn--ghost:hover {
      background: rgba(15, 23, 42, 0.9);
      box-shadow: 0 10px 24px rgba(15, 23, 42, 0.6);
    }

    /* Matches list */
    .section-title {
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--muted);
      margin-bottom: 0.4rem;
    }

    .match-list {
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
      margin-bottom: 0.7rem;
      max-height: 320px;
      overflow-y: auto;
      padding-right: 0.2rem;
    }

    .match-card {
      background: radial-gradient(circle at top left, rgba(59,130,246,0.1), rgba(15,23,42,0.96));
      border-radius: 0.9rem;
      padding: 0.65rem 0.7rem;
      border: 1px solid rgba(55, 65, 81, 0.9);
      display: grid;
      grid-template-columns: minmax(0, 1.6fr) minmax(0, 1.4fr);
      gap: 0.6rem;
      align-items: center;
      cursor: pointer;
      transition: border 0.13s ease, transform 0.1s ease, box-shadow 0.15s ease, background 0.15s ease;
    }

    .match-card:hover {
      border-color: rgba(59, 130, 246, 0.9);
      transform: translateY(-1px);
      box-shadow: 0 16px 34px rgba(15, 23, 42, 0.85);
      background: radial-gradient(circle at top left, rgba(59,130,246,0.18), rgba(15,23,42,0.98));
    }

    .match-card.active {
      border-color: var(--accent);
      box-shadow: 0 16px 38px rgba(16, 185, 129, 0.4);
      background: radial-gradient(circle at top left, rgba(34,197,94,0.18), rgba(15,23,42,0.98));
    }

    .match-teams {
      font-size: 0.9rem;
      font-weight: 600;
    }

    .match-league {
      font-size: 0.75rem;
      color: var(--muted);
      margin-top: 0.15rem;
    }

    .match-time {
      font-size: 0.78rem;
      color: var(--muted);
    }

    .odds {
      display: flex;
      gap: 0.4rem;
      justify-content: flex-end;
      flex-wrap: wrap;
    }

    .odd-pill {
      border-radius: 999px;
      padding: 0.28rem 0.55rem;
      font-size: 0.78rem;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(75, 85, 99, 0.9);
      color: #e5e7eb;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-width: 58px;
    }

    .odd-label {
      font-size: 0.72rem;
      color: var(--muted);
    }

    .odd-value {
      font-weight: 600;
    }

    /* Bet slip */
    .betslip-card {
      background: linear-gradient(145deg, #020617, #020617);
      border-radius: var(--radius-lg);
      border: 1px solid rgba(55, 65, 81, 0.9);
      padding: 1rem;
      box-shadow: var(--shadow-soft);
      margin-top: 0.3rem;
    }

    .betslip-row {
      display: flex;
      justify-content: space-between;
      gap: 0.5rem;
      font-size: 0.82rem;
      margin-bottom: 0.3rem;
    }

    .betslip-row strong {
      font-weight: 600;
    }

    .betslip-empty {
      font-size: 0.8rem;
      color: var(--muted);
      text-align: center;
      padding: 0.4rem 0;
    }

    .accent {
      color: var(--accent);
    }

    .input-group {
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
      margin-bottom: 0.5rem;
      font-size: 0.8rem;
    }

    label {
      color: var(--muted);
    }

    input[type="number"] {
      width: 100%;
      border-radius: 999px;
      border: 1px solid rgba(75, 85, 99, 0.85);
      padding: 0.38rem 0.75rem;
      background: rgba(15, 23, 42, 0.9);
      color: var(--text);
      font-size: 0.85rem;
      outline: none;
      transition: border 0.15s ease, box-shadow 0.15s ease, background 0.15s ease;
      -moz-appearance: textfield;
    }

    input[type="number"]:focus {
      border-color: var(--accent-2);
      box-shadow: 0 0 0 1px rgba(59, 130, 246, 0.8);
      background: #020617;
    }

    input[type="number"]::-webkit-outer-spin-button,
    input[type="number"]::-webkit-inner-spin-button {
      -webkit-appearance: none;
      margin: 0;
    }

    .betslip-actions {
      display: flex;
      justify-content: space-between;
      gap: 0.5rem;
      margin-top: 0.4rem;
      align-items: center;
    }

    .small-note {
      font-size: 0.7rem;
      color: var(--muted);
      line-height: 1.5;
    }

    .status {
      margin-top: 0.4rem;
      font-size: 0.8rem;
      padding: 0.3rem 0.6rem;
      border-radius: 999px;
      display: inline-block;
    }

    .status--error {
      background: var(--danger-soft);
      color: #fecaca;
      border: 1px solid rgba(248, 113, 113, 0.9);
    }

    .status--success {
      background: var(--accent-soft);
      color: #bbf7d0;
      border: 1px solid rgba(34, 197, 94, 0.9);
    }

    /* History */
    .history-list {
      margin-top: 0.4rem;
      max-height: 330px;
      overflow-y: auto;
      padding-right: 0.25rem;
    }

    .history-item {
      border-radius: 0.8rem;
      padding: 0.55rem 0.6rem;
      margin-bottom: 0.35rem;
      font-size: 0.8rem;
      border: 1px solid rgba(55, 65, 81, 0.9);
      background: radial-gradient(circle at top left, rgba(15,23,42,0.95), rgba(15,23,42,0.98));
    }

    .history-item.win {
      border-color: rgba(34, 197, 94, 0.9);
      background: radial-gradient(circle at top left, rgba(34,197,94,0.16), rgba(15,23,42,0.98));
    }

    .history-item.loss {
      border-color: rgba(248, 113, 113, 0.9);
      background: radial-gradient(circle at top left, rgba(248,113,113,0.16), rgba(15,23,42,0.98));
    }

    .history-top {
      display: flex;
      justify-content: space-between;
      margin-bottom: 0.15rem;
      gap: 0.5rem;
    }

    .history-teams {
      font-weight: 600;
    }

    .history-status {
      font-size: 0.72rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .history-status.win {
      color: #bbf7d0;
    }

    .history-status.loss {
      color: #fecaca;
    }

    .history-meta {
      display: flex;
      justify-content: space-between;
      gap: 0.5rem;
      color: var(--muted);
      font-size: 0.76rem;
      flex-wrap: wrap;
    }

    /* Scrollbar */
    .match-list::-webkit-scrollbar,
    .history-list::-webkit-scrollbar {
      width: 6px;
    }
    .match-list::-webkit-scrollbar-track,
    .history-list::-webkit-scrollbar-track {
      background: transparent;
    }
    .match-list::-webkit-scrollbar-thumb,
    .history-list::-webkit-scrollbar-thumb {
      background: rgba(75, 85, 99, 0.8);
      border-radius: 999px;
    }
  </style>
</head>
<body>
  <div class="app">
    <!-- LEFT SIDE: matches & balance -->
    <div class="card">
      <div class="card-header">
        <div>
          <div class="tagline"> • Real Real Money Only</div>
          <h1>Online Betting Real</h1>
          <p class="subtext">
            Ye sirf <strong>learning &</strong> ke liye hai. Yahan jo bhi bet lagegi wo
            <strong> Real Money</strong> real money se hogi –.
          </p>
        </div>
        <div>
          <div class="badge badge--warning">Real Money • No Any Real Only</div>
        </div>
      </div>

      <div class="balance-card">
        <div>
	Make Payment Before on - jaatdevta@axis>
          <div class="balance-label">Current Balance</div>
          <div class="balance-value" id="balance">250</div>
          <div class="balance-label">Real Money</div>
        </div>
        <div style="display:flex; gap:0.4rem;">
          <button class="btn btn--ghost" id="add-Real Money-btn">+ 500 Real Money</button>
          <button class="btn btn--ghost" id="reset-btn">Reset</button>
        </div>
      </div>

      <div>
        <div class="section-title">Upcoming Matches</div>
        <div class="match-list" id="match-list">
          <!-- Matches JS se inject honge -->
        </div>
      </div>
    </div>

    <!-- RIGHT SIDE: bet slip & history -->
    <div class="card">
      <div class="card-header">
        <div>
          <div class="section-title">Bet Slip</div>
          <p class="subtext">
            Koi match select karein, amount decide karein aur <strong>Place Bet</strong> dabayein.
          </p>
        </div>
      </div>

      <div class="betslip-card">
        <div id="betslip-content">
          <div class="betslip-empty">
            Pehle left side se ek match select karein.
          </div>
        </div>

        <div class="input-group">
          <label for="stake-input">Stake (Real Money)</label>
          <input
            id="stake-input"
            type="number"
            min="10"
            step="10"
            placeholder="e.g. 50"
          />
        </div>

        <div class="betslip-actions">
          <div class="small-note">
            Random result generate hota hai – <br/>real money.
          </div>
          <button class="btn" id="place-bet-btn">Place Bet</button>
        </div>

        <div id="status-message"></div>
      </div>

      <div style="margin-top: 1rem;">
        <div class="section-title">Bet History</div>
        <div class="history-list" id="history-list">
          <!-- history items -->
        </div>
      </div>
    </div>
  </div>

  <script>
    // ----------------------------
    // Real DATA: matches & odds
    // ----------------------------
    const matches = [
      {
        id: 1,
        league: "Premier League",
        teams: "City FC vs United FC",
        time: "Today · 08:30 PM",
        odds: { home: 1.9, draw: 3.4, away: 2.8 },
      },
      {
        id: 2,
        league: "La Liga",
        teams: "Madrid CF vs Barca FC",
        time: "Today · 11:00 PM",
        odds: { home: 2.2, draw: 3.3, away: 2.4 },
      },
      {
        id: 3,
        league: "Cricket T20",
        teams: "Rajasthan Royals vs Gujarat Titans",
        time: "Tomorrow · 07:30 PM",
        odds: { home: 1.7, draw: 0, away: 2.2 },
      },
      {
        id: 4,
        league: "Cricket ODI",
        teams: "India vs Australia",
        time: "Tomorrow · 02:00 PM",
        odds: { home: 1.8, draw: 0, away: 2.5 },
      },
      {
        id: 5,
        league: "Champions League",
        teams: "Red FC vs Blue FC",
        time: "Sun · 01:30 AM",
        odds: { home: 2.0, draw: 3.6, away: 3.0 },
      },
    ];

    let balance = 1000;
    let selectedMatch = null;
    let selectedOutcome = null; // "home" | "draw" | "away"
    let history = [];

    const balanceEl = document.getElementById("balance");
    const matchListEl = document.getElementById("match-list");
    const betslipContentEl = document.getElementById("betslip-content");
    const stakeInputEl = document.getElementById("stake-input");
    const placeBetBtn = document.getElementById("place-bet-btn");
    const historyListEl = document.getElementById("history-list");
    const statusMessageEl = document.getElementById("status-message");
    const addReal MoneyBtn = document.getElementById("add-Real Money-btn");
    const resetBtn = document.getElementById("reset-btn");

    // Utility: update balance UI
    function updateBalance() {
      balanceEl.textContent = balance.toFixed(0);
    }

    // Render matches
    function renderMatches() {
      matchListEl.innerHTML = "";
      matches.forEach((m) => {
        const card = document.createElement("div");
        card.className =
          "match-card" + (selectedMatch && selectedMatch.id === m.id ? " active" : "");
        card.dataset.id = m.id;

        card.innerHTML = `
          <div>
            <div class="match-teams">${m.teams}</div>
            <div class="match-league">${m.league}</div>
            <div class="match-time">${m.time}</div>
          </div>
          <div class="odds">
            <div class="odd-pill" data-outcome="home">
              <span class="odd-label">Home</span>
              <span class="odd-value">${m.odds.home.toFixed(2)}</span>
            </div>
            ${
              m.odds.draw > 0
                ? `<div class="odd-pill" data-outcome="draw">
                     <span class="odd-label">Draw</span>
                     <span class="odd-value">${m.odds.draw.toFixed(2)}</span>
                   </div>`
                : ""
            }
            <div class="odd-pill" data-outcome="away">
              <span class="odd-label">Away</span>
              <span class="odd-value">${m.odds.away.toFixed(2)}</span>
            </div>
          </div>
        `;

        // Click match card -> select match
        card.addEventListener("click", (e) => {
          const outcomeEl = e.target.closest(".odd-pill");
          if (outcomeEl) {
            const outcome = outcomeEl.dataset.outcome;
            onSelectMatch(m, outcome);
          } else {
            onSelectMatch(m, null);
          }
        });

        matchListEl.appendChild(card);
      });
    }

    function onSelectMatch(match, outcome) {
      selectedMatch = match;
      if (outcome) {
        selectedOutcome = outcome;
      } else if (!selectedOutcome) {
        selectedOutcome = "home"; // default
      }
      renderMatches();
      renderBetslip();
      clearStatus();
    }

    // Render bet slip based on selectedMatch & selectedOutcome
    function renderBetslip() {
      if (!selectedMatch) {
        betslipContentEl.innerHTML =
          '<div class="betslip-empty">Pehlay left se koi match select karein.</div>';
        return;
      }

      const odds = selectedMatch.odds[selectedOutcome];
      const outcomeLabel =
        selectedOutcome === "home" ? "Home" : selectedOutcome === "away" ? "Away" : "Draw";

      const potentialWin = calcPotentialWin(odds);

      betslipContentEl.innerHTML = `
        <div class="betslip-row">
          <span><strong>Match:</strong></span>
          <span>${selectedMatch.teams}</span>
        </div>
        <div class="betslip-row">
          <span><strong>Outcome:</strong></span>
          <span>${outcomeLabel} @ <span class="accent">${odds.toFixed(2)}</span></span>
        </div>
        <div class="betslip-row">
          <span><strong>Stake:</strong></span>
          <span id="stake-preview">${getStake() || 0} Real Money</span>
        </div>
        <div class="betslip-row">
          <span><strong>Potential Return:</strong></span>
          <span id="potential-win">${potentialWin.toFixed(0)} Real Money</span>
        </div>
      `;
    }

    function getStake() {
      const val = Number(stakeInputEl.value);
      return Number.isFinite(val) && val > 0 ? val : 0;
    }

    function calcPotentialWin(odds) {
      const stake = getStake();
      return stake * odds;
    }

    // Update stake preview on input
    stakeInputEl.addEventListener("input", () => {
      if (!selectedMatch) return;
      const odds = selectedMatch.odds[selectedOutcome];
      const stake = getStake();
      const stakePreviewEl = document.getElementById("stake-preview");
      const potentialWinEl = document.getElementById("potential-win");
      if (stakePreviewEl && potentialWinEl) {
        stakePreviewEl.textContent = `${stake.toFixed(0)} Real Money`;
        potentialWinEl.textContent = `${(stake * odds).toFixed(0)} Real Money`;
      }
      clearStatus();
    });

    // Place bet
    placeBetBtn.addEventListener("click", () => {
      clearStatus();
      if (!selectedMatch) {
        showStatus("Pehlay koi match select karein.", "error");
        return;
      }

      const stake = getStake();
      if (stake <= 0) {
        showStatus("Stake kam se kam 10 Real Money honi chahiye.", "error");
        return;
      }
      if (stake < 10) {
        showStatus("Minimum stake 10 Real Money hai.", "error");
        return;
      }
      if (stake > balance) {
        showStatus("Itne Real Money aapke balance me nahi hain.", "error");
        return;
      }

      // Deduct stake
      balance -= stake;

      // Simulate result
      const odds = selectedMatch.odds[selectedOutcome];
      const won = simulateResult(odds);

      let winAmount = 0;
      if (won) {
        winAmount = stake * odds;
        balance += winAmount;
      }

      updateBalance();
      addToHistory(selectedMatch, selectedOutcome, stake, odds, won, winAmount);
      renderHistory();

      showStatus(
        won
          ? `🎉 Bet WON! Aapko approx ${winAmount.toFixed(0)} Real Money mile.`
          : "❌ Bet LOST! Agli baar koshish karein.",
        won ? "success" : "error"
      );
    });

    function simulateResult(odds) {
      // Simple probability: higher odds => lower chance
      // probability = 1 / odds (clamped)
      const baseProb = 1 / odds;
      const probability = Math.max(0.18, Math.min(0.8, baseProb));
      const rnd = Math.random();
      return rnd < probability;
    }

    function showStatus(message, type) {
      statusMessageEl.innerHTML = "";
      const div = document.createElement("div");
      div.className = "status " + (type === "error" ? "status--error" : "status--success");
      div.textContent = message;
      statusMessageEl.appendChild(div);
    }

    function clearStatus() {
      statusMessageEl.innerHTML = "";
    }

    // History
    function addToHistory(match, outcome, stake, odds, won, winAmount) {
      const outcomeLabel =
        outcome === "home" ? "Home" : outcome === "away" ? "Away" : "Draw";

      history.unshift({
        id: Date.now(),
        teams: match.teams,
        league: match.league,
        outcome: outcomeLabel,
        stake,
        odds,
        won,
        winAmount,
        balanceAfter: balance,
        time: new Date().toLocaleTimeString(),
      });

      // limit
      if (history.length > 50) history.pop();
    }

    function renderHistory() {
      historyListEl.innerHTML = "";

      if (history.length === 0) {
        historyListEl.innerHTML =
          '<div class="betslip-empty">Abhi tak koi bet history nahi hai.</div>';
        return;
      }

      history.forEach((item) => {
        const div = document.createElement("div");
        div.className = "history-item " + (item.won ? "win" : "loss");
        div.innerHTML = `
          <div class="history-top">
            <div class="history-teams">${item.teams}</div>
            <div class="history-status ${item.won ? "win" : "loss"}">
              ${item.won ? "WON" : "LOST"}
            </div>
          </div>
          <div class="history-meta">
            <span>${item.league}</span>
            <span>Outcome: ${item.outcome} @ ${item.odds.toFixed(2)}</span>
          </div>
          <div class="history-meta">
            <span>Stake: ${item.stake.toFixed(0)} Real Money</span>
            <span>${item.won ? "Return" : "Lost"}: ${item.won ? item.winAmount.toFixed(0) : item.stake.toFixed(0)} Real Money</span>
          </div>
          <div class="history-meta">
            <span>Time: ${item.time}</span>
            <span>Balance after: ${item.balanceAfter.toFixed(0)} Real Money</span>
          </div>
        `;
        historyListEl.appendChild(div);
      });
    }

    // Add Real Money for testing
    addReal MoneyBtn.addEventListener("click", () => {
      balance += 500;
      updateBalance();
      showStatus("500 Real Money add kar diye gaye.", "success");
    });

    // Reset
    resetBtn.addEventListener("click", () => {
      balance = 1000;
      history = [];
      selectedMatch = null;
      selectedOutcome = null;
      updateBalance();
      renderMatches();
      renderBetslip();
      renderHistory();
      clearStatus();
      stakeInputEl.value = "";
    });

    // Init
    updateBalance();
    renderMatches();
    renderBetslip();
    renderHistory();
  </script>
</body>
</html>
