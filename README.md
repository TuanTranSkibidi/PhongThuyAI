# PhongThuyAI
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Phong Thủy AI</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 600px;
      margin: 40px auto;
      padding: 20px;
      background: #f9f9f9;
      border-radius: 12px;
    }
    h1 {
      text-align: center;
      color: #333;
    }
    label {
      display: block;
      margin-top: 12px;
      font-weight: bold;
    }
    input, select, button {
      width: 100%;
      padding: 10px;
      margin-top: 6px;
      margin-bottom: 12px;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    #result {
      font-weight: bold;
      color: #006400;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>🧭 Tư vấn Phong Thủy AI</h1>

  <label for="year">Năm sinh:</label>
  <input type="number" id="year" placeholder="VD: 1990" />

  <label for="gender">Giới tính:</label>
  <select id="gender">
    <option value="nam">Nam</option>
    <option value="nu">Nữ</option>
  </select>

  <label for="direction">Hướng nhà:</label>
  <select id="direction">
    <option>Bắc</option>
    <option>Nam</option>
    <option>Đông</option>
    <option>Tây</option>
  </select>

  <button onclick="consult()">Xem tư vấn</button>

  <div id="result"></div>

  <script>
    function consult() {
      const year = document.getElementById('year').value;
      const gender = document.getElementById('gender').value;
      const direction = document.getElementById('direction').value;
      const result = document.getElementById('result');

      if (gender === 'nam' && direction === 'Bắc') {
        result.innerText = `✅ Hướng Bắc hợp với nam mệnh năm ${year}.`;
      } else {
        result.innerText = `⚠️ Hướng ${direction} không hợp với ${gender} mệnh năm ${year}. Nên cân nhắc hóa giải.`;
      }
    }
  </script>
</body>
</html>
