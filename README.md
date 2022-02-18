# yolox-bytetrack-mcmot-sample
[Kazuhito00/yolox-bytetrack-sample](https://github.com/Kazuhito00/yolox-bytetrack-sample)のマルチクラス拡張版です。<br>

https://user-images.githubusercontent.com/37477845/154706131-4fd00207-fbeb-4403-8fc7-aee5c2f4de04.mp4

# Requirement 
* OpenCV 3.4.2 or later
* onnxruntime 1.5.2 or later
* lap 0.4.0 or later 
* Cython 0.29.27 or later 
* cython_bbox 0.1.3 or later
<br>
※Windowsでcython_bbox のインストールが失敗する場合は、GitHubからのインストールをお試しください(2022/02/13時点)<br>

`pip install -e git+https://github.com/samson-wang/cython_bbox.git#egg=cython-bbox`

# Demo
デモの実行方法は以下です。
```bash
python sample.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：960
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：540
<details>
<summary>YOLOXパラメータ</summary>
  
* --yolox_model<br>
ロードするモデルの格納パス<br>
デフォルト：model/yolox_nano.onnx
* --input_shape<br>
モデルの入力サイズ<br>
デフォルト：416,416
* --score_th<br>
クラス判別の閾値<br>
デフォルト：0.3
* --nms_th<br>
NMSの閾値<br>
デフォルト：0.45
* --nms_score_th<br>
NMSのスコア閾値<br>
デフォルト：0.1
* --with_p6<br>
Large P6モデルを使用するか否か<br>
デフォルト：指定なし
</details>

<details>
<summary>ByteTrackパラメータ</summary>
  
* --track_thresh<br>
デフォルト：0.5
* --track_buffer<br>
デフォルト：30
* --match_thresh<br>
デフォルト：0.8
* --min_box_area<br>
デフォルト：10
* --mot20<br>
デフォルト：指定なし
  
※パラメータ詳細は[ByteTrack](https://github.com/ifzhang/ByteTrack)を参照ください。
</details>


# Reference
* [Megvii-BaseDetection/YOLOX](https://github.com/Megvii-BaseDetection/YOLOX)
* [YOLOX-ONNX-TFLite-Sample](https://github.com/Kazuhito00/YOLOX-ONNX-TFLite-Sample)
* [ByteTrack](https://github.com/ifzhang/ByteTrack)
* [Kazuhito00/yolox-bytetrack-sample](https://github.com/Kazuhito00/yolox-bytetrack-sample)

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
yolox-bytetrack-mcmot-sample is under [MIT License](LICENSE).

# License(Movie)
サンプル動画は[NHKクリエイティブ・ライブラリー](https://www.nhk.or.jp/archives/creative/)の[ケニア共和国キツイ 町並み(4) ふかんショット](https://www2.nhk.or.jp/archives/creative/material/view.cgi?m=D0002040395_00000)を使用しています。
