<!DOCTYPE html>
<html lang="zh-CN">

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>梦想清单</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9c0c2;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #8aa9d9;
      color: white;
      text-align: center;
      padding: 20px 0;
    }

    .container {
      max-width: 800px;
      margin: 20px auto;
      padding: 20px;
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: all 0.3s ease-in-out;
    }

    .container:hover {
      border: 2px solid #fee26d;
      box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
    }

    h2 {
      color: #333;
    }

    ul {
      padding-left: 20px;
      color: #555;
    }

    li {
      margin-bottom: 10px;
      color: #555;
      transition: all 0.3s ease-in-out;
    }

    li:hover {
      color: #fee26d;
      transform: scale(1.1);
    }

    input {
      padding: 10px;
      width: calc(100% - 40px);
      margin-right: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      padding: 10px 20px;
      background-color: #fee26d;
      color: black;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s ease-in-out;
    }

    button:hover {
      background-color: #fee26d;
    }

    footer {
      background-color: #ffd1dc;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 20px;
    }

    footer p {
      margin: 0;
      font-size: 16px;
      transition: color 0.3s ease-in-out;
    }

    footer p:hover {
      color: #287ac5;
    }

    .music-control {
      text-align: center;
      margin: 20px 0;
    }

    .music-control button {
      background-color: #eb5486;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      color: white;
      margin: 5px;
    }

    .music-control button:hover {
      background-color: #ebd686;
    }
  </style>
</head>

<body>
  <header>
    <h1>我的梦想清单</h1>
  </header>
  <div class="container">
    <h2>我的梦想</h2>
    <ul id="dreamList">
      <li><input type="checkbox">体验一次跳伞，看看从高空飞下的感觉</li>
      <li><input type="checkbox">去海上看看鲸鱼，近距离感受它们的震撼</li>
      <li><input type="checkbox">看一次极光，看看它有多美</li>
      <li><input type="checkbox">去日本体验二次元世界，感受动漫氛围</li>
    </ul>
    <div>
      <input type="text" id="newDream" placeholder="输入你的新梦想">
      <button onclick="addDream()">添加梦想</button>
    </div>
  </div>
  <div class="music-control">
    <audio id="backgroundMusic" loop>
      <source src="https://drive.google.com/uc?export=download&id=1qSyLXKzHzncExH9L5i-MtoEFt88d4RFO"type="audio/mpeg">
      您的浏览器不支持音频播放
    </audio>
    <button onclick="playMusic()">播放音乐</button>
    <button onclick="pauseMusic()">暂停音乐</button>
    <footer>
      <p>关于我: 我是一个懒人，梦想嘛，就是想着能懒一点，过得随意一些。</p>
      <p>有什么大目标吗? 也许吧，但谁知道呢，反正慢慢来。</p>
    </footer>
    <script>
      function addDream() {
          const dream = document.getElementById('newDream').value;
          if(dream) {
          const list = document.getElementById('dreamList');
          const newItem = document.createElement('li');
          newItem.textContent=dream;
          list.appendChild(newItem);
          document.getElementById('newDream').value='';
          }
      }
      const music = document.getElementById('backgroundMusic');

      function playMusic() {
          music.play();
      }

      function pauseMusic() {
          music.pause();
      }
    </script>
</body>

</html>