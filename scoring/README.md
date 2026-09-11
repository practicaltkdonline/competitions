# 搏擊計分遊戲 PWA

遊戲邏輯與畫面與原本 HTML 版本相同，只加上可安裝的 PWA 支援（manifest、圖示、Service Worker）。

## 本機使用

PWA 安裝與 Gamepad API 需要以本機伺服器開啟（不要直接雙擊 `index.html`）。

```bash
cd pwa
python3 -m http.server 8080
```

瀏覽器打開：`http://localhost:8080`

## 安裝成 App

1. 用 Chrome / Edge / Safari 打開上述網址  
2. 網址列右側選「安裝應用程式」／「加到主畫面」  
3. 安裝後會以全螢幕（standalone）橫向開啟

## 離線

第一次成功載入後，Service Worker 會快取頁面與 CDN（React、Babel、Tailwind）。之後即使沒有網路也可以再開啟已安裝的 App。

## 注意

- 請用 HTTPS 或 `localhost`，否則手掣（Gamepad）與安裝提示可能不可用  
- 遊戲本身仍建議接 PS4 手掣、用橫向大螢幕操作
