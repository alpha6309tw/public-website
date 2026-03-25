# 縮小 CSS
為增進網站載入速度，用 [purgecss](https://purgecss.com/CLI.html) 縮小 css 檔案，它會透過分析既有 HTML，移除沒用到的 css selector，只留下用到的，因此減小檔案。經過縮減的檔名都附加 `required`，例如 `fontawesome580.required.css`. 

`purgecss --css assets/css/fontawesome580.css --content _site/**/*.html -o fontawesome580.required.css`

# [slick.js](https://kenwheeler.github.io/slick/)
a jquery plugin to create a carousel.