# 目前仍在測試階段
# 參考
fork origin: https://github.com/otiai10/ocrserver

# 與原版差異
辨識圖片中井字型0~9的x,y位置。

# 條件限制
test0.0.1版本可辨識圖片中井字型1到9的XY位置，但0需要在7到9的下方，  
同水平中不可有重複數字。

# 目前可辨別錯誤
1. `find multiple same or shortage of numbers by y point line`  
圖片中鍵盤缺少或其他位置出現，123、456、789的三種數字組合。
2. `not found number : 0`  
0未被在數字789的底下找到。  

## TODO
1. 789底下若有多個0
2. 未確認井字X軸
3. 未確認多個井字組合
4. ...

# Quick Start

## Mac Install tesseract

```sh
brew install tesseract
```

## Go Get & Run

If you have tesseract-ocr and library files on your machine  

```sh
% go get github.com/otiai10/ocrserver/...
% go get github.com/jou66jou/go-orcnums-xy
% cd $GOPATH/github.com/jou66jou/go-orcnums-xy
% go run main.go -p 8080
```  

## or Ready-Made Docker Image

```sh
% docker-compose up -d
```

cf. [docker](https://www.docker.com/products/docker-toolbox)

## Upload Test Image

1. Open http://localhost:8080
2. Upload test image file from `./imagetest` folder 
3. Get json response!


## Result


<div align=center><img width="30%" height="30%" src="https://github.com/jou66jou/go-orcnums-xy/blob/master/imagetest/success.jpg" alt="success case"/></div>

