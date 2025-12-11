<!DOCTYPE html>
<html lang="ko">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta charset="UTF-8" />
  <title>버튼 수량 카운터</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: #f5f5f5;
    }

    .group {
      margin-bottom: 30px;
      padding: 20px;
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.1);
    }

    .title {
      font-size: 22px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .btn-row {
      display: flex;
      gap: 15px;
      margin-bottom: 10px;
    }

    button {
      flex: 1;
      padding: 15px;
      font-size: 18px;
      border: none;
      border-radius: 8px;
      background: #007bff;
      color: white;
    }

    .count {
      font-size: 18px;
      margin-left: 10px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="group">
    <div class="title">KPP</div>

    <div class="btn-row">
      <button onclick="add('n12')">N12 증가</button>
      <span id="n12" class="count">0</span>
    </div>

    <div class="btn-row">
      <button onclick="add('n11')">N11 증가</button>
      <span id="n11" class="count">0</span>
    </div>
  </div>

  <div class="group">
    <div class="title">AJ</div>

    <div class="btn-row">
      <button onclick="add('a12')">A12 증가</button>
      <span id="a12" class="count">0</span>
    </div>

    <div class="btn-row">
      <button onclick="add('a11')">A11 증가</button>
      <span id="a11" class="count">0</span>
    </div>
  </div>

  <script>
    function add(id) {
      const el = document.getElementById(id);
      el.textContent = Number(el.textContent) + 1;
    }
  </script>
</body>
</html>
