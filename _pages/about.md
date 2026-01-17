---
permalink: /
title: ""
excerpt: "About me"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
footer: false
---

<!-- 
  Matrix 背景层 
  修改点：
  1. z-index: 0 (原为-1，防止被手机浏览器画布覆盖)
  2. pointer-events: none (防止背景层拦截手机触摸操作)
  3. numColumns=50 (原为100，手机屏幕窄，减少列数可大幅降低GPU负担，防止黑屏)
-->
<div style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: 0; pointer-events: none; overflow: hidden; background: black;">
  <iframe src="https://rezmason.github.io/matrix/?numColumns=100&fallSpeed=0.25&slant=0&glyphRotation=90&bloomStrength=0.1&cycleSpeed=0.01&skipIntro=true&bloomSize=0&version=resurrections" style="width: 100%; height: 100%; border: none; opacity: 0.6;"></iframe>
</div>

<style>
  /* ====== 核心修改区：暴力解决手机端背景被遮挡问题 ====== */
  
  /* 1. 强制所有 Jekyll 主题容器透明 */
  /* Minimal Mistakes 主题在移动端会给 masthead 和 body 加背景色，必须用 !important 覆盖 */
  html, body, #main, .initial-content, .page__content, .page, .page__footer, footer, .masthead, .archive, .author__urls-wrapper {
    background: transparent !important;
    background-color: transparent !important;
  }

  /* 2. 隐藏可能存在的伪元素背景遮罩 */
  body::before, body::after, .masthead::before, .masthead::after {
    background: transparent !important;
    display: none !important;
  }

  /* 3. 字体和颜色定义 */
  :root {
    --matrix-green: #00FF41;
    --text-main: #e0e0e0;
    --text-dim: #a0a0a0;
  }

  /* ====== 布局与滚动控制 ====== */
  
  html, body {
    height: 100%;
    margin: 0;
    padding: 0 !important;
  }

  /* 手机端：允许垂直滚动，启用平滑滚动 */
  body {
    overflow-y: auto; 
    overflow-x: hidden;
    -webkit-overflow-scrolling: touch; /* iOS 滚动优化 */
  }

  /* 电脑端：保持无滚动条设计 (如果内容很少的话) */
  @media (min-width: 768px) {
    html, body {
      overflow: hidden !important;
    }
  }

  /* ====== 内容容器 (核心逻辑) ====== */
  .main-content {
    position: relative; /* 必须是 relative */
    z-index: 10; /* 必须高于背景层的 0 */
    max-width: 850px;
    margin: 40px auto 0 auto;
    padding: 20px;
    background: transparent; 
    color: var(--text-main);
    font-family: 'Courier New', Courier, monospace; 
  }

  /* ====== 具体的元素样式 (保持原设计) ====== */

  /* 主标题 */
  .home-title {
    text-align: center;
    font-family: 'Courier New', Courier, monospace;
    font-size: 24px;
    color: var(--matrix-green);
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 10px;
    font-weight: normal; 
  }

  /* 导航链接 */
  .nav-links {
    text-align: center;
    margin: 20px 0 40px 0;
  }
  .nav-links a {
    text-decoration: none;
    color: var(--matrix-green);
    font-family: 'Courier New', monospace;
    padding: 4px 10px;
    border: 1px solid var(--matrix-green);
    border-radius: 4px;
    margin: 0 5px;
    font-size: 13px;
    transition: all 0.3s;
    /* 增加微弱的背景色，防止代码雨干扰文字阅读 */
    background: rgba(0, 0, 0, 0.4); 
  }
  .nav-links a:hover {
    background: rgba(0, 255, 65, 0.1);
  }

  /* H3 标题 */
  h3 {
    font-family: 'Courier New', Courier, monospace;
    font-weight: normal; 
    color: var(--matrix-green);
    border-bottom: 2px solid rgba(0, 255, 65, 0.3);
    padding-bottom: 8px;
    margin-top: 40px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: 1.2rem;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
  }

  /* 经历列表 */
  .exp-item {
    margin-bottom: 25px;
    /* 增加文字阴影，确保在亮色代码划过时依然清晰 */
    text-shadow: 1px 1px 2px rgba(0,0,0,1); 
  }
  .exp-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
  }
  
  .exp-title {
    font-family: 'Courier New', Courier, monospace;
    font-size: 17px;
    font-weight: normal;
    color: var(--matrix-green);
  }

  .exp-date {
    font-family: 'Courier New', monospace;
    font-size: 13px;
    color: var(--matrix-green);
  }

  .exp-sub {
    font-family: 'Courier New', Courier, monospace;
    font-size: 13px;
    color: var(--text-dim);
    margin-top: 4px;
  }

  /* 底部 Quote */
  .bottom-quote {
    margin-top: 60px;
    text-align: center;
    font-family: 'Courier New', Courier, monospace;
    font-style: italic;
    font-size: 13px;
    color: var(--text-dim);
    opacity: 0.8;
    padding-bottom: 20px;
  }
</style>

<div class="main-content">
  
  <div class="home-title">Zhong Tianqi's Homepage</div>
    
  <div class="nav-links">
    <a href="https://www.rslog.cc" target="_blank">blog</a>
    <a href="https://scholar.google.com/citations?hl=en&user=UNNLJX4AAAAJ" target="_blank">scholar</a>
    <a href="https://github.com/tqzhong" target="_blank">github</a>
    <a href="mailto:ztq1047@gmail.com">email</a>
  </div>

  <h3>Experience</h3>
  
  <div class="exp-item">
    <div class="exp-header">
      <span class="exp-title">Intelligent Conversation</span>
      <span class="exp-date">2025.04 ~ Now</span>
    </div>
    <div class="exp-sub">ByteDance, Data</div>
  </div>

  <div class="exp-item">
    <div class="exp-header">
      <span class="exp-title">Internship in User Platform Department</span>
      <span class="exp-date">2024.06 ~ 2024.08</span>
    </div>
    <div class="exp-sub">Tencent, IEG</div>
  </div>

  <div class="exp-item">
    <div class="exp-header">
      <span class="exp-title">M.Eng. in Information and Communication Engineering</span>
      <span class="exp-date">2022.09 ~ 2025.06</span>
    </div>
    <div class="exp-sub">University of Science and Technology of China</div>
  </div>

  <div class="exp-item">
    <div class="exp-header">
      <span class="exp-title">B.Eng. in Electronic Information Engineering</span>
      <span class="exp-date">2018.09 ~ 2022.06</span>
    </div>
    <div class="exp-sub">University of Science and Technology of China</div>
  </div>

  <div class="bottom-quote">
    If the Matrix ever becomes a reality, I just hope they leave out Neo this time...
  </div>

</div>