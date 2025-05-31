<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>24H Work Online</title>
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
  <style>
    html, body {
      background: #FFF5EF;
      font-family: 'Segoe UI', Arial, sans-serif;
      margin: 0;
      padding: 0;
      color: #222;
      width: 100vw;
      min-height: 100vh;
      max-width: 100vw;
      overflow-x: hidden;
      -webkit-tap-highlight-color: transparent;
    }
    .container {
      width: 100vw;
      max-width: 100vw;
      margin: 0 auto;
      padding: 0 0 88px 0;
      min-height: 100vh;
      box-sizing: border-box;
      position: relative;
    }
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 0 0 24px 0;
      padding: 0 16px 0 16px;
    }
    .title {
      font-size: 2.1rem;
      font-weight: bold;
      color: #222;
    }
    .lang-select {
      background: #F4A259;
      border: none;
      border-radius: 6px;
      padding: 4px 18px;
      color: #fff;
      font-weight: 500;
      font-size: 1.04rem;
      cursor: pointer;
    }
    .form-section {
      margin: 0 16px;
    }
    .input-group {
      margin-bottom: 18px;
      position: relative;
    }
    .input-group input {
      width: 100%;
      padding: 16px 14px 16px 45px;
      border-radius: 12px;
      border: none;
      background: #fff;
      font-size: 1.09rem;
      color: #222;
      box-shadow: 0 2px 12px #e7e7e7;
      outline: none;
    }
    .input-group .icon {
      position: absolute;
      top: 13px;
      left: 13px;
      font-size: 1.13em;
      color: #F4A259;
    }
    .input-group input::placeholder {
      color: #b3b3b3;
      font-size: 1.07rem;
    }
    .btn {
      display: block;
      width: 100%;
      padding: 15px 0;
      border: none;
      border-radius: 13px;
      margin-bottom: 14px;
      font-size: 1.14rem;
      font-weight: 500;
      cursor: pointer;
      transition: background 0.18s;
      letter-spacing: 0.02em;
    }
    .btn-main { background: linear-gradient(90deg, #F4A259, #F9B17A); color: #fff; }
    .btn-main:active { background: #F4A259; }
    .btn-secondary { background: #181818; color: #fff; }
    .btn-tertiary { background: #981ae4; color: #fff; margin-bottom: 28px; }

    .logo {
      margin: 36px auto 0;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .logo img {
      width: 90px;
      height: 90px;
      border-radius: 50%;
      background: #f7be4b;
      border: 7px solid #f7be4b;
    }
    .profile-section {
      width: 100%;
      background: transparent;
      padding: 24px 0 0 0;
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 18px;
      margin-left: 16px;
    }
    .profile-img {
      width: 55px;
      height: 55px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid #fff;
      background: #e8e8e8;
      flex-shrink: 0;
    }
    .profile-phone {
      font-size: 1.28rem;
      font-weight: 600;
      color: #222;
      word-break: break-word;
    }
    .profile-code-row {
      display: flex;
      align-items: center;
      font-size: 1.03rem;
      color: #888;
      gap: 12px;
      margin: 6px 0 0 0;
    }
    .code-badge {
      background: #f0f0f0;
      border-radius: 6px;
      padding: 0 10px;
      color: #222;
      font-weight: 500;
      margin-left: 4px;
      margin-right: 5px;
      font-size: 0.98em;
      letter-spacing: 0.02em;
    }
    .copy-btn {
      border: none;
      background: #F4A259;
      color: #fff;
      border-radius: 6px;
      padding: 2px 10px;
      font-size: 1em;
      cursor: pointer;
      margin-left: 4px;
    }
    .balance-card {
      background: #fff;
      border-radius: 18px;
      margin: 18px 16px 0 16px;
      padding: 22px 22px 16px 22px;
      box-shadow: 0 3px 16px #e7e7e7;
      position: relative;
    }
    .balance-row {
      display: flex;
      align-items: center;
      justify-content: flex-start;
      gap: 18px;
    }
    .balance-label {
      color: #222;
      font-size: 1.09em;
      font-weight: 500;
      margin-bottom: 8px;
      display: block;
    }
    .balance-value {
      font-size: 2rem;
      color: #F4A259;
      font-weight: bold;
      margin-right: 15px;
      letter-spacing: 0.014em;
    }
    .support-badges {
      font-size: 0.99em;
      color: #2E7D32;
      display: flex;
      gap: 12px;
      margin-top: 6px;
      font-weight: 500;
      align-items: center;
      letter-spacing: 0.01em;
    }
    .quote {
      color: #868686;
      font-size: 1em;
      margin-top: 18px;
      font-style: italic;
      line-height: 1.6;
    }
    .task-section {
      margin: 20px 16px 0 16px;
    }
    .task-label {
      font-weight: bold;
      font-size: 1.13em;
      margin-bottom: 6px;
      color: #222;
    }
    .task-card {
      background: #f7fff4;
      border-radius: 16px;
      margin: 0;
      padding: 18px 18px 13px 18px;
      box-shadow: 0 1px 8px #e7e7e7;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }
    .task-title {
      font-weight: bold;
      color: #22b300;
    }
    .task-title-hindi {
      color: #888;
      font-size: 1em;
      font-weight: normal;
      margin-bottom: 3px;
    }
    .task-earn {
      margin: 5px 0 0 0;
      font-weight: 500;
      color: #222;
      font-size: 1.08em;
    }
    .task-btn {
      margin: 13px 0 0 0;
      align-self: flex-end;
      width: 90px;
      background: linear-gradient(90deg, #F4A259, #F9B17A);
      color: #fff;
      border: none;
      border-radius: 8px;
      padding: 11px 0;
      font-size: 1.05em;
      font-weight: 500;
      cursor: pointer;
      transition: background 0.18s;
    }
    .account-panel {
      margin: 18px 16px 0 16px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }
    .panel-btn {
      background: #fff;
      border-radius: 13px;
      border: none;
      padding: 22px 0 11px 0;
      font-size: 1.05em;
      font-weight: 500;
      color: #222;
      text-align: center;
      cursor: pointer;
      box-shadow: 0 2px 8px #e7e7e7;
      transition: background 0.13s;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 7px;
    }
    .panel-btn.main {
      grid-column: span 3;
      background: #d13a00;
      color: #fff;
      font-size: 1.12em;
    }
    .nav-bar {
      display: none;
    }
    .show-nav .nav-bar {
      display: flex !important;
    }
    .nav-bar {
      justify-content: space-around;
      align-items: flex-end;
      position: fixed;
      left: 0; right: 0; bottom: 0;
      background: #F4A259;
      padding: 13px 0 3px 0;
      z-index: 2;
      box-shadow: 0 -2px 12px #e7e7e7;
      width: 100vw;
      max-width: 100vw;
      height: 58px;
    }
    .nav-item {
      color: #fff;
      font-size: 1.13rem;
      text-align: center;
      font-weight: 500;
      text-decoration: none;
      flex: 1;
      transition: color 0.16s;
      padding-bottom: 2px;
    }
    .nav-item.active {
      color: #2e6cff;
      border-bottom: 3px solid #2e6cff;
      border-radius: 2px;
    }
    .nav-icon {
      display: block;
      font-size: 1.43em;
      margin-bottom: 1px;
    }
    .modal-bg {
      position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
      background: #0003;
      z-index: 100;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .modal {
      background: #fff;
      border-radius: 13px;
      padding: 29px 22px 22px 22px;
      max-width: 340px;
      width: 94vw;
      box-shadow: 0 7px 36px #2222;
      position: relative;
    }
    .modal input {
      margin-bottom: 12px;
      width: 100%;
      border-radius: 7px;
      border: 1px solid #f4a25955;
      padding: 10px 11px;
      font-size: 1rem;
    }
    .close-btn {
      position: absolute;
      right: 16px;
      top: 10px;
      border: none;
      background: none;
      font-size: 1.5rem;
      color: #F4A259;
      cursor: pointer;
    }
    .hidden { display: none; }
    @media (max-width: 480px) {
      html, body { max-width: 100vw; }
      .container { max-width: 100vw; }
    }
  </style>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
  <!-- Register Screen -->
  <div class="container" id="registerScreen">
    <div class="header">
      <span class="title">Register</span>
      <select class="lang-select"><option>English</option></select>
    </div>
    <form id="registerForm" class="form-section">
      <div class="input-group">
        <span class="icon"><i class="fa fa-phone"></i></span>
        <input type="tel" name="phone" required placeholder="Please enter phone number">
      </div>
      <div class="input-group">
        <span class="icon"><i class="fa fa-lock"></i></span>
        <input type="password" name="password" required placeholder="Please enter password">
      </div>
      <div class="input-group">
        <span class="icon"><i class="fa fa-lock"></i></span>
        <input type="password" name="repassword" required placeholder="Re-enter password">
      </div>
      <div class="input-group">
        <span class="icon"><i class="fa fa-ticket"></i></span>
        <input type="text" name="invite" placeholder="InvitationCode(Optional)">
      </div>
      <button type="submit" class="btn btn-main">Register Now</button>
      <button type="button" class="btn btn-secondary" onclick="showLogin()">Login</button>
      <button type="button" class="btn btn-tertiary" onclick="window.open('https://t.me/letseranXXXX839638386','_blank')">Online Customer Service</button>
    </form>
    <div class="logo"><img src="https://i.imgur.com/0xwWzYt.png" alt="App Logo"></div>
  </div>

  <!-- Login Screen (hidden initially) -->
  <div class="container hidden" id="loginScreen">
    <div class="header">
      <span class="title">Login</span>
      <select class="lang-select"><option>English</option></select>
    </div>
    <form id="loginForm" class="form-section">
      <div class="input-group">
        <span class="icon"><i class="fa fa-phone"></i></span>
        <input type="tel" name="phone" required placeholder="Please enter phone number">
      </div>
      <div class="input-group">
        <span class="icon"><i class="fa fa-lock"></i></span>
        <input type="password" name="password" required placeholder="Please enter password">
      </div>
      <button type="submit" class="btn btn-main">Login Now</button>
      <button type="button" class="btn btn-secondary" onclick="showRegister()">Register</button>
      <button type="button" class="btn btn-tertiary" onclick="window.open('https://t.me/letseranXXXX839638386','_blank')">Online Customer Service</button>
    </form>
    <div class="logo"><img src="https://i.imgur.com/0xwWzYt.png" alt="App Logo"></div>
  </div>

  <!-- Home Screen (hidden initially) -->
  <div class="container hidden" id="homeScreen">
    <div class="profile-section">
      <img class="profile-img" src="profile9.jpg" alt="profile">
      <div class="profile-phone" id="userPhone">9635774083</div>
    </div>
    <div class="balance-card">
      <div class="balance-row">
        <div>
          <span class="balance-label">Balance</span>
          <div class="balance-value" id="userBalance">₹8773</div>
        </div>
        <div>
          <div class="support-badges">
            <span><i class="fa fa-shield-halved"></i> SSL Encrypted</span>
          </div>
          <div class="support-badges" style="margin-top: 2px;">
            <span><i class="fa fa-circle-check"></i> 24/7 Support</span>
          </div>
        </div>
      </div>
      <div class="quote">
        "Can't believe I got ₹500 on Day 1 — no downloads, no stress!"<br>
        — Arjun, Bangalore
      </div>
    </div>
    <div class="task-section">
      <div class="task-label">Task</div>
      <div class="task-card">
        <span class="task-title">WhatsApp Forwarding Task</span>
        <span class="task-title-hindi">वट्सएप फॉरवर्डिंग टास्क</span>
        <span class="task-earn">Earn ₹20</span>
        <button class="task-btn">Start</button>
      </div>
    </div>
  </div>

  <!-- Account Screen (hidden initially)-->
  <div class="container hidden" id="accountScreen">
    <div class="profile-section">
      <img class="profile-img" src="profile9.jpg" alt="profile">
      <div>
        <div class="profile-phone" id="accountPhone">9635774083</div>
        <div class="profile-code-row">
          Code: <span class="code-badge" id="accountCode">997255</span>
          <button class="copy-btn" onclick="copyCode()">Copy</button>
        </div>
      </div>
    </div>
    <div class="balance-card">
      <div class="balance-row">
        <div>
          <span class="balance-label">Account Balance</span>
          <div class="balance-value" id="accountBalance">8773</div>
        </div>
      </div>
    </div>
    <div class="account-panel">
      <button class="panel-btn" onclick="window.open('https://t.me/letseranXXXX839638386','_blank')"><i class="fa fa-headset"></i> Customer Service</button>
      <button class="panel-btn" onclick="showWithdrawModal()"><i class="fa fa-wallet"></i> Account Withdraw</button>
      <button class="panel-btn" onclick="showEarnings()"><i class="fa fa-money-bill-wave"></i> Earnings Details</button>
      <button class="panel-btn" onclick="showWithdrawOrders()"><i class="fa fa-list-check"></i> Withdraw Orders</button>
      <button class="panel-btn" onclick="showMessageCenter()"><i class="fa fa-comments"></i> Message Center</button>
      <button class="panel-btn" onclick="showChangePassword()"><i class="fa fa-pen"></i> Change Password</button>
      <button class="panel-btn main" onclick="logout()"><i class="fa fa-right-from-bracket"></i> Logout</button>
    </div>
  </div>

  <!-- Withdraw Modal -->
  <div class="modal-bg hidden" id="withdrawModal">
    <div class="modal">
      <button class="close-btn" onclick="closeWithdrawModal()">&times;</button>
      <h3 style="margin-bottom: 20px;">Add Bank Account</h3>
      <form id="bankForm">
        <input type="text" name="card" placeholder="Card Number" required><br>
        <input type="text" name="name" placeholder="Name" required><br>
        <input type="text" name="ifsc" placeholder="IFSC Code" required><br>
        <button type="submit" class="btn btn-main">Save Bank Account</button>
      </form>
      <button class="btn btn-secondary" style="margin-top:10px;" onclick="requestWithdraw()">Withdraw</button>
    </div>
  </div>
  <!-- Withdraw Orders Modal -->
  <div class="modal-bg hidden" id="withdrawOrdersModal">
    <div class="modal">
      <button class="close-btn" onclick="closeWithdrawOrdersModal()">&times;</button>
      <h3>Withdraw Orders History</h3>
      <ul id="withdrawOrdersList"></ul>
    </div>
  </div>
  <!-- Earnings Details Modal -->
  <div class="modal-bg hidden" id="earningsModal">
    <div class="modal">
      <button class="close-btn" onclick="closeEarningsModal()">&times;</button>
      <h3>Earnings Details</h3>
      <ul id="earningsList"></ul>
    </div>
  </div>
  <!-- Hidden Admin Panel Login -->
  <div class="modal-bg hidden" id="adminLoginModal">
    <div class="modal">
      <button class="close-btn" onclick="closeAdminLogin()">&times;</button>
      <h3>Admin Panel Login</h3>
      <form id="adminLoginForm">
        <input type="tel" name="adminPhone" placeholder="Phone Number" required><br>
        <input type="password" name="adminPassword" placeholder="Password" required><br>
        <button type="submit" class="btn btn-main">Login as Admin</button>
      </form>
    </div>
  </div>
  <!-- Hidden Admin Panel (future features) -->
  <div class="container hidden" id="adminPanel">
    <div class="header">
      <span class="title">Admin Panel</span>
    </div>
    <form id="adminSearchForm" class="form-section">
      <input type="tel" name="searchPhone" placeholder="Search user by phone" required>
      <button type="submit" class="btn btn-main" style="margin-top: 8px;">Search</button>
    </form>
    <div id="adminUserDetails" class="form-section"></div>
    <form id="adminAddPointsForm" class="hidden form-section" style="margin-top:10px;">
      <input type="number" name="points" placeholder="Add points" required>
      <button type="submit" class="btn btn-secondary" style="margin-top:8px;">Add Points</button>
    </form>
  </div>

  <div class="nav-bar">
    <a class="nav-item active" onclick="showHome()"><span class="nav-icon"><i class="fa fa-house"></i></span>Home</a>
    <a class="nav-item" onclick="showPromotion()"><span class="nav-icon"><i class="fa fa-paper-plane"></i></span>Promotion</a>
    <a class="nav-item" onclick="showTutorial()"><span class="nav-icon"><i class="fa fa-book"></i></span>Tutorial</a>
    <a class="nav-item" onclick="showAccount()"><span class="nav-icon"><i class="fa fa-user"></i></span>Account</a>
  </div>

  <script>
    function showHome() {
      hideAll();
      document.body.classList.add('show-nav');
      document.getElementById('homeScreen').classList.remove('hidden');
      setNavActive(0);
    }
    function showRegister() {
      hideAll();
      document.body.classList.remove('show-nav');
      document.getElementById('registerScreen').classList.remove('hidden');
      setNavActive(-1);
    }
    function showLogin() {
      hideAll();
      document.body.classList.remove('show-nav');
      document.getElementById('loginScreen').classList.remove('hidden');
      setNavActive(-1);
    }
    function showAccount() {
      hideAll();
      document.body.classList.add('show-nav');
      document.getElementById('accountScreen').classList.remove('hidden');
      setNavActive(3);
    }
    function setNavActive(idx) {
      document.querySelectorAll('.nav-item').forEach((el, i) => {
        if (i === idx) el.classList.add('active');
        else el.classList.remove('active');
      });
    }
    function hideAll() {
      document.querySelectorAll('.container').forEach(el => el.classList.add('hidden'));
    }
    function showWithdrawModal() {
      document.getElementById('withdrawModal').classList.remove('hidden');
    }
    function closeWithdrawModal() {
      document.getElementById('withdrawModal').classList.add('hidden');
    }
    function showWithdrawOrders() {
      document.getElementById('withdrawOrdersModal').classList.remove('hidden');
      document.getElementById('withdrawOrdersList').innerHTML = `
        <li>₹500 - 2025-05-14 - Success</li>
        <li>₹800 - 2025-05-10 - Pending</li>
      `;
    }
    function closeWithdrawOrdersModal() {
      document.getElementById('withdrawOrdersModal').classList.add('hidden');
    }
    function showEarnings() {
      document.getElementById('earningsModal').classList.remove('hidden');
      document.getElementById('earningsList').innerHTML = `
        <li>+₹200 | Task Complete | 2025-05-29</li>
        <li>+₹300 | Referral | 2025-05-28</li>
      `;
    }
    function closeEarningsModal() {
      document.getElementById('earningsModal').classList.add('hidden');
    }
    function showMessageCenter() { alert('Message Center (Coming Soon)'); }
    function showChangePassword() { alert('Change Password (Coming Soon)'); }
    function showPromotion() { alert('Promotion (Coming Soon)'); }
    function showTutorial() { alert('Tutorial (Coming Soon)'); }
    function logout() {
      showLogin();
    }
    function copyCode() {
      const code = document.getElementById('accountCode').textContent;
      navigator.clipboard.writeText(code);
      alert('Code copied!');
    }
    let tapCount = 0;
    document.getElementById('registerScreen').addEventListener('click', function() {
      tapCount++;
      if (tapCount === 7) {
        tapCount = 0;
        document.getElementById('adminLoginModal').classList.remove('hidden');
      }
      setTimeout(() => { tapCount = 0; }, 2000);
    });
    function closeAdminLogin() {
      document.getElementById('adminLoginModal').classList.add('hidden');
    }
    document.getElementById('adminLoginForm').onsubmit = function(e) {
      e.preventDefault();
      const phone = e.target.adminPhone.value;
      const pass = e.target.adminPassword.value;
      if (phone === "6297417223" && pass === "INDIA12342008") {
        closeAdminLogin();
        hideAll();
        document.body.classList.remove('show-nav');
        document.getElementById('adminPanel').classList.remove('hidden');
      } else {
        alert("Invalid credentials.");
      }
    };
    document.getElementById('adminSearchForm').onsubmit = function(e) {
      e.preventDefault();
      const phone = e.target.searchPhone.value;
      // Demo mock data, adjust as needed
      document.getElementById('adminUserDetails').innerHTML = `
        <b>User:</b> ${phone}<br>
        <b>Password:</b> demoPassword123<br>
        <b>Rights:</b> User<br>
        <b>Withdrawals:</b>
        <ul>
          <li>₹500 - 2025-05-14 - Success (Card: 1234xxxx7890, IFSC: ICIC0000)</li>
          <li>₹800 - 2025-05-10 - Pending (Card: 9876xxxx1234, IFSC: SBIN0001)</li>
        </ul>
      `;
      document.getElementById('adminAddPointsForm').classList.remove('hidden');
    };
    document.getElementById('adminAddPointsForm').onsubmit = function(e) {
      e.preventDefault();
      alert("Points added!");
      document.getElementById('adminAddPointsForm').classList.add('hidden');
    };
    document.getElementById('registerForm').onsubmit = function(e) {
      e.preventDefault();
      showHome();
      document.getElementById('userPhone').innerText = e.target.phone.value;
      document.getElementById('accountPhone').innerText = e.target.phone.value;
      document.getElementById('userBalance').innerText = '₹0';
      document.getElementById('accountBalance').innerText = '0';
    };
    document.getElementById('loginForm').onsubmit = function(e) {
      e.preventDefault();
      showHome();
      document.getElementById('userPhone').innerText = e.target.phone.value;
      document.getElementById('accountPhone').innerText = e.target.phone.value;
      document.getElementById('userBalance').innerText = '₹8773';
      document.getElementById('accountBalance').innerText = '8773';
    };
    document.getElementById('bankForm').onsubmit = function(e) {
      e.preventDefault();
      alert('Bank account saved!');
      closeWithdrawModal();
    };
    function requestWithdraw() {
      alert('Withdrawal request submitted!');
      closeWithdrawModal();
    }
    showRegister();
  </script>
</body>
</html>,
