# 3Dメッシュライブストリーミングについて
本発表では、遠隔地からの3Dライブストリーミングを実演する予定です（※不特定多数へのウェブアプリでのメッシュライブストリーミングの実演は、おそらく世界初になります。まだ実験段階のため中止あるいは録画の可能性もあります）。 当日は、各種プラットホームのブラウザから下記のアドレスで視聴する事が可能です。 

http://depstreamer.shop/live.html

## PC, スマートフォン(Android, iOS)の非AR環境の場合
「Start 3D/VR」ボタンをクリックして視聴してください。マウスの左右ボタンドラッグで視点の回転や移動、スクロールホイールで拡大、縮小を行う事が出来ます。
	
## 各種VR, MagicLeap1環境の場合
VR対応ブラウザ上で「Start 3D/VR」ボタンをクリックして視聴してください。ブラウザのウィンドウ下端に「ENTER VR」というボタンがでたら、そのボタンもクリックすると没入モードに切り替わります。「VR(WEBXR) NOT FOUND」と表示される場合は、何らかの理由により再生環境がVRに対応していない、あるいは適切に設定されていない可能性があります。 足元の高さにオフセットがある場合、適切な高さで位置リセットを行えば補正が可能な場合があります。例えばOculus  Questの場合、自分の頭を適切な高さに移動させた後、ホームボタン長押しでリセットが可能です。

## HoloLensの場合
Edgeブラウザ上で「Start HoloLens」ボタンをクリックして視聴してください。ブラウザのウィンドウ下端に「ENTER VR」というボタンが表示されたら、そのボタンもクリックすると没入モードに切り替わります。「VR NOT FOUND」と表示される場合は、何らかの理由により再生環境がVRに対応していない、あるいは適切に設定されていない可能性があります。その際には下記の設定の確認をお願いします。
足元の高さのオフセットについては、Edgeブラウザの空間内の位置によって変わるようなのですが、実は挙動が良く分かっていません…
	
	※なお、HoloLensのEdgeブラウザはデフォルトでWebVR対応が無効にされているため、下記の手順で有効化が必要になります。

## HoloLensのEdgeブラウザのWebVR有効化方法
アドレスバーにabout:flags と入力して、フラグ設定画面に移動してください。一番下に「Enable WebVR」があるのでチェックしてください。OSが最新の場合だとチェック無しでも動くようですが、動かない場合は上記の設定をお願いします。  

## ARCore対応AndroidもしくはARKit対応iOS環境の場合
ARCoreに対応したAndroid端末のChrome上、あるいはARKitに対応したiOS端末のWebXR Viewerで「Start AR」ボタンをクリックして視聴してください。ブラウザのウィンドウ下端に「ENTER AR」というボタンが表示されたら、そのボタンもクリックするとARモードに切り替わります。「AR NOT SUPPORTED」と表示される場合は、Android端末がARCoreに対応していない、Chromeブラウザが最新ではない、あるいは適切に設定されていない可能性があります。  
ARモードに切り替え後、カメラを床面に向けながら並進移動させて床面の検出を行ってください。床面が検出されたら正面に円形のレチクル（印）が出現するので、
タップするとその位置に3D動画が出現します。

	※なお、AndroidのChromeブラウザも何故かデフォルトでWebXR対応が無効にされているため、下記の手順で有効化が必要になります。

## AndroidのChromeブラウザのWebXR有効化方法
アドレスバーにchrome://flags と入力して、フラグ設定画面に移動してください。「WebXR Device API」「WebXR AR Module」「WebXR Hit Test」を全てEnableに設定します。バージョン次第ではデフォルトで設定されているかもしれませんが、念のためこれらが有効化されているかのチェックをお願いします。  

## 動作確認環境
現時点では下記の環境でVRモードの動作を確認しています。他の環境でも動いた、動かないという方がいらっしゃれば、報告いただけると大変ありがたいです。  

- 3Dモード
	- WebGL対応の各種ブラウザ（全ては確認できていません）

- VRモード
	- Windows MR + Edgeブラウザ
	- Oculus Quest + Oculusブラウザ
	- Oculus Go + Oculusブラウザ（※移動不可）
	- DaydreamVR + Chromeブラウザ（※Mirage Solo以外は移動不可）
	- Magic Leap 1 + Helioブラウザ (※現在ライブ時にコマ落ちする症状を確認しています)

- ARモード
	- Android ARCore + Chromeブラウザ (Google Pixelで確認済)
  - iOS ARKit + WebXR Viewer（iPad 第6世代で確認済。WebXR Viewer以外のブラウザでは動作しません）
	
- HoloLensモード (実質VRモードですが、最新のThree.jsでは動作しないため、旧実装を使用しています)
	- HoloLens + Edgeブラウザ　(※光学シースルーによるAR環境になります)
  
