---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
footer: false
---

<!-- Matrix 背景层 -->
<div style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1; overflow: hidden; background: black;">
  <iframe src="https://rezmason.github.io/matrix/?numColumns=100&fallSpeed=0.25&slant=0&glyphRotation=90&bloomStrength=0.1&cycleSpeed=0.01&skipIntro=true&bloomSize=0&version=resurrections" style="width: 100%; height: 100%; border: none; opacity: 0.6;"></iframe>
</div>

<style>
  /* 强制禁止滚动条 */
  html, body {
    overflow: hidden !important;
    height: 100%;
    margin: 0;
    padding: 0;
  }

  :root {
    --matrix-green: #00FF41;
    --text-main: #e0e0e0;
    --text-dim: #a0a0a0;
  }

  /* 容器 */
  .main-content {
    position: relative;
    z-index: 1;
    max-width: 850px;
    margin: 60px auto 0 auto;
    padding: 20px;
    background: transparent; 
    color: var(--text-main);
    font-family: 'Courier New', Courier, monospace; 
  }

  /* 顶部台词 */
  summary {
    list-style: none;
    font-family: 'Courier New', Courier, monospace;
    font-style: italic;
    font-size: 14px;
    text-align: center;
    cursor: pointer;
    color: var(--matrix-green);
    transition: all 0.3s;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    padding: 10px;
  }
  summary:hover {
    text-shadow: 0 0 10px var(--matrix-green);
  }
  summary::-webkit-details-marker { display: none; }

  /* 顶部按钮 */
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
  }

  /* H2 标题 */
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

  /* 经历项 */
  .exp-item {
    margin-bottom: 25px;
    text-shadow: 1px 1px 3px rgba(0,0,0,0.9);
  }
  .exp-header {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
  }
  
  /* --- 经历标题（修改处） --- */
  .exp-title {
    font-family: 'Courier New', Courier, monospace;
    font-size: 17px;
    font-weight: normal;    /* 核心修改：改为 normal，之前是 600 */
    color: var(--matrix-green);
  }

  /* 时间 */
  .exp-date {
    font-family: 'Courier New', monospace;
    font-size: 13px;
    color: var(--matrix-green);
  }

  /* 副标题 */
  .exp-sub {
    font-family: 'Courier New', Courier, monospace;
    font-size: 13px;
    color: var(--text-dim);
    margin-top: 4px;
  }
</style>

<div class="main-content">
  <details>
    <summary>If the Matrix ever becomes a reality, I just hope they leave out Neo this time...</summary>
    
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
  </details>
</div>