<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Chị Nhi Xinh Gái</title>
  <style>
    body {
      background-color: pink;
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 100px;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #ffb6c1;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h2>Em nhớ chị</h2>
  <button onclick="openMultipleWindows()">Nhấn vào đây</button>

  <script>
    function openPopupWindow(index) {
      const left = Math.floor(Math.random() * (screen.availWidth - 320));
      const top = Math.floor(Math.random() * (screen.availHeight - 220));
      const features = `width=300,height=200,top=${top},left=${left},resizable=no`;

      const popup = window.open("", "_blank", features);

      if (popup) {
        const content = `
          <!DOCTYPE html>
          <html lang="vi">
            <head>
              <meta charset="UTF-8">
              <title>Chị iu ${index + 1}</title>
              <style>
                body {
                  background-color: pink;
                  display: flex;
                  justify-content: center;
                  align-items: center;
                  height: 100vh;
                  font-family: Arial, sans-serif;
                  margin: 0;
                }
                h1 {
                  font-size: 18px;
                }
              </style>
              <script>
                setTimeout(() => window.close(), 10000);
              <\/script>
            </head>
            <body>
              <h1>Chị yêu ngủ ngon nhé</h1>
            </body>
          </html>
        `;
        popup.document.open();
        popup.document.write(content);
        popup.document.close();
      } else {
        alert("Safari đang chặn popup. Hãy bật cho phép popup trong phần cài đặt trình duyệt nha chị!");
      }
    }

    function openMultipleWindows() {
      for (let i = 0; i < 10; i++) {
        setTimeout(() => openPopupWindow(i), i * 150);
      }
    }
  </script>
</body>
</html>
