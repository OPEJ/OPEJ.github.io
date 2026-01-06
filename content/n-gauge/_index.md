---
title: "N規收藏"   # 這會顯示在網頁分頁的大標題
date: 2026-01-02
draft: false          # 記得檢查這裡是不是 false
---

## N規模型  

這裡按照分類顯示收藏的N規模型。  
我會簡單介紹模型細節與心得。 

**依種類分類：**

<style>
  .category-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 30px; }
  .category-card { 
    background: #f8f9fa; border: 1px solid #ddd; padding: 30px; text-align: center; 
    text-decoration: none; color: #2c3e50; border-radius: 8px; transition: 0.3s;
    font-size: 1.2rem; font-weight: bold; box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  }
  .category-card:hover { background: #2c3e50; color: #fff; transform: translateY(-5px); }
  .category-card i { display: block; font-size: 2.5rem; margin-bottom: 15px; }
</style>

<div class="category-grid">
  <a href="./n-collection/" class="category-card">
    <span>全部收藏清單</span>
  </a>
  <a href="./types/steam-locomotives/" class="category-card">
    <span>蒸汽機車</span>
  </a>
  <a href="./types/electric-locomotives/" class="category-card">
    <span>電力機車</span>
  </a>
  <a href="./types/passenger-cars/" class="category-card">
    <span>客車</span>
  </a>
  <a href="./types/freight-cars/" class="category-card">
    <span>貨車</span>
  </a>
</div>

<br>

**依品牌分類：**

<div class="category-grid">
  <a href="./brands/kato/" class="category-card">
    <span>KATO</span>
  </a>
  <a href="./brands/tomix/" class="category-card">
    <span>TOMIX</span>
  </a>
  <a href="./brands/sanying/" class="category-card" >
    <span>三鶯重工</span>
  </a>
  </div>

<br><br>

<div class="special-nav">
  <a href="/n-gauge/comparison/" class="big-nav-card comparison-bg">
    <div class="overlay">
      <span class="en-title">COMPARISON</span>
      <span class="zh-title">型式專欄</span>
    </div>
  </a>
</div>

<style>
  .special-nav {
    margin-top: 20px;
    width: 100%;
  }

  .big-nav-card {
    position: relative;
    display: block;
    height: 150px; /* 控制大按鈕的高度 */
    border-radius: 8px;
    overflow: hidden;
    text-decoration: none !important;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    background-size: cover;
    background-position: center;
    background-color: #2c3e50;
    /* 這裡替換成你想要的背景圖 */
    background-image: url('https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=1000'); 
  }

  .big-nav-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 15px rgba(0,0,0,0.2);
  }

  .overlay {
    position: absolute;
    inset: 0;
    background: rgba(0, 0, 0, 0.5); /* 遮罩深淺 */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white !important;
  }

  .en-title {
    font-size: 1.5rem;
    font-weight: bold;
    letter-spacing: 3px;
    margin-bottom: 5px;
  }

  .zh-title {
    font-size: 1rem;
    opacity: 0.9;
  }
</style>

