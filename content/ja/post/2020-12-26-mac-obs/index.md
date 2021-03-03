---
title: Mac+OBSでタイマーをキャプチャする
author: ''
date: '2020-12-26'
slug: mac-obs
categories:
  - Mac
tags: ["Mac", "Zoom", "オンライン", "OBS"]
subtitle: '備忘録も兼ねてます。'
summary: 'Zoom学会のときに便利そうです。'
authors: []
featured: no
image:
  placement: 1
  focal_point: "Center"
  preview_only: false
projects: []
draft: false
---
# <b>はじめに</b>
最近は学会や発表会が軒並みオンラインで行われています。

そのとき多くの場合問題になっているのが、<b><span style="color: #dc143c; ">タイムをどうやって管理するか</span></b>
だと思います。
いくつかのオンライン学会に参加した際は、チャットに残り時間を記載する仕組みを取っていました。

しかしこのような方法は個人的にはいくつか不便な点があるように感じました。

<b>発表者側</b>
- Zoomで画面共有をしていたら、チャットに気が付かない
- 自分側でのタイムキープと運営側とで時間差がある

<b>司会側</b>
- 発表者を遮って、声を出したくない
- タイムキープに気を使わなければならない

といった点があり、少し改良が必要そうです。

<br>

# 顔出し画面にタイムを表示する

個人の顔出しの画面にカウントダウン画面をキャプチャする方法です。
この方法を取っていれば、画面共有をしていてもその画面は発表者側からも見えるようになると思います。

<span style="color: #dc143c; "><b>※注意※</b></span>

私の使用しているPCはMacなので、Mac使用者向けの説明が中心になります。
Windowsの方は他サイトをご参照ください。

<br>

## <b>1. OBS Studioをインストールする</b>
[OBS Studio](https://obsproject.com/ja/download)の真ん中のりんごのマークから、ダウンロードを開始。

他のブログなどを参照すると、OBS Studioの他に、OBS Virtual Camera というものをインストールする必要があると書いてありますが、
最近リリースされた<b>OBS Studio 26.1</b>からはvirtual cameraはインストールする必要がなくなったみたいです。

反対に、すでにインストールしてあったら削除する必要がありそうです。

[参照](https://github.com/johnboiles/obs-mac-virtualcam/releases)

<br>

## <b>2. Zoomに画面をキャプチャする手順</b>
OBS Studioをインストールし終えたあと、実際にZoomに任意の画面をキャプチャする手順を示します。

### OBS側の設定

1. OBS Studioを立ち上げる

2. 下の方の「ソース」というところの「＋」から「映像キャプチャデバイス」を選択

3. そのまま「ok」を選択

4. プロパティも「ok」を選択

5. 再び下の方の「ソース」というところの「＋」から「ウィンドウキャプチャ」を選択

6. そのまま「ok」を選択

7. 「ウィンドウ」のタブから、参照したいページ(Safariなど)を選択し、「ok」を選択

<span style="color: #dc143c; "><b>※注意※</b></span>

もしここで「Safari」などブラウザが表示されない場合は、[こちら](https://qiita.com/sendaiharu1/items/83aa20f8e5c96bf0a573)を行うと良さそうです。
私はこれを行ったら、Macの<b>「セキュリティとデバイス > プライバシー > 画面収録」</b>にOBSが反映されました。

8. 下の方の「コントロール」の「仮想カメラ開始」を選択

ここまでがOBS側での設定です。

### Zoom側の設定

9. Zoomの「ビデオの停止」の右側の上三角を選択し，カメラを選択の部分を「OBS Virtual Camera」に変更

10. もし映し出された映像が反転していたら、OBS側のSafariなどの画面を反転して、Zoomに映るものが正しくなるように調整する

これでZoom側の設定も終わりました。

<br>

# おわりに

MacにおけるZoomの顔出し画面にタイマーをキャプチャする方法を書きました。

はたしてこれがZoom学会での最適解なのかと言われると、どうなのかな、と思う点もありますが、小さな発表会や少し表示したい時などは便利になると思いました。

なにかの参考になれば幸いです。

<br>

# 参考にしたサイト

- [座長@Zoom会議で映像＋タイマー表示](https://qiita.com/kojiyam/items/36f48e0b7a8aef6bf3be)
- [macOS CatalinaでOBS（ウインドウキャプチャ）を使う](https://qiita.com/sendaiharu1/items/83aa20f8e5c96bf0a573)

