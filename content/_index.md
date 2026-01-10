<style>
  .home-split-container {
    position: relative;
    width: 100%;
    height: 65vh; 
    overflow: hidden;
    display: flex;
    font-family: sans-serif;
    border-radius: 12px;
    margin: 20px 0;
    background: #000; /* 背景設為黑色，變暗時才有質感 */
  }

  .split-side {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none !important;
    /* 增加 transition 時間讓變暗效果更平滑 */
    transition: all 0.7s cubic-bezier(0.16, 1, 0.3, 1);
    filter: brightness(0.7); /* 預設稍微暗一點點 */
  }

  /* 左側：N 規 */
  .n-gauge-side {
    left: 0;
    background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=1000');
    background-size: cover;
    background-position: center;
    clip-path: polygon(0 0, 65% 0, 35% 100%, 0% 100%);
    z-index: 1;
  }

  /* 右側：1/64比例 */
  .scale-64-side {
    right: 0;
    background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('/images/car-index.jpg');
    background-size: cover;
    background-position: center;
    clip-path: polygon(65% 0, 100% 0, 100% 100%, 35% 100%);
  }

  /* --- 核心修改：變暗邏輯 --- */

  /* 當滑鼠進入容器時，先讓兩邊都變得很暗 */
  .home-split-container:hover .split-side {
    filter: brightness(0.3) grayscale(0.5); /* 降低亮度並稍微去色 */
    opacity: 0.6; /* 增加透明度感 */
  }

  /* 唯獨滑鼠指到的那一邊，恢復亮度並放大 */
  .home-split-container .split-side:hover {
    filter: brightness(1.1) grayscale(0); /* 恢復明亮彩色 */
    opacity: 1;
    z-index: 2;
  }

  /* 保持原本的斜線擴張效果 */
  .n-gauge-side:hover {
    clip-path: polygon(0 0, 80% 0, 50% 100%, 0% 100%);
  }

  .scale-64-side:hover {
    clip-path: polygon(50% 0, 100% 0, 100% 100%, 20% 100%);
  }

  /* 文字容器保持不變 */
  .split-text {
    color: white !important;
    text-shadow: 2px 2px 15px rgba(0,0,0,0.8);
    transition: transform 0.6s ease, opacity 0.6s ease;
    width: 300px;
    pointer-events: none;
  }

  /* 未選中的文字稍微變透明 */
  .home-split-container:hover .split-side:not(:hover) .split-text {
    opacity: 0.3;
  }

  .n-gauge-side .split-text { text-align: left; transform: translateX(-15%); }
  .scale-64-side .split-text { text-align: right; transform: translateX(15%); }
  .n-gauge-side:hover .split-text { transform: translateX(-10%); opacity: 1; }
  .scale-64-side:hover .split-text { transform: translateX(10%); opacity: 1; }

  .split-text .en { display: block; font-size: 2.2rem; font-weight: 900; letter-spacing: 3px; line-height: 1; }
  .split-text .zh { display: block; font-size: 1rem; margin-top: 10px; font-weight: 300; letter-spacing: 1px; }

  @media (max-width: 768px) {
    .home-split-container { height: 500px; flex-direction: column; }
    .n-gauge-side, .scale-64-side { position: relative; height: 50%; clip-path: none !important; filter: brightness(0.8) !important; opacity: 1 !important; }
    .n-gauge-side .split-text, .scale-64-side .split-text { text-align: center; transform: none !important; width: 100%; }
  }
</style>

這裡將記錄我的長期收藏與心得。

<div class="home-split-container">
  <a href="/n-gauge/" class="split-side n-gauge-side">
    <div class="split-text">
      <span class="en">N-GAUGE</span>
      <span class="zh">模型鐵道收藏記錄</span>
    </div>
  </a>

  <a href="/64scale/" class="split-side scale-64-side" title="Image source: BMW PressClub">
    <div class="split-text">
      <span class="en">1:64 SCALE</span>
      <span class="zh">模型車與耐力賽事記錄</span>
    </div>
  </a>
</div>