# 【Python+OpencV】ピンボケ写真の判定、Webカメラ映像のピントが合ったときに静止画を保存

## 【例3】Webカメラ映像のピントが合ったときに静止画を保存

Webカメラ映像のピントが合ったときに静止画を保存するプログラムをPythonとOpenCVで実装してみました。
以下のプログラムを実行し、キーボードの「S」を押した時にピンボケしていなければ画像を保存します。


```
import cv2

# ピンボケ写真か判定
def check_blurry_photo(img, lap_var_min=100):
    # グレースケール変換
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

    lap_var = cv2.Laplacian(gray, cv2.CV_64F).var()

    # しきい値より大きければピンボケ写真と判定してTrueを返す
    return lap_var < lap_var_min

def main():
    # カメラ起動（カメラが複数台存在する場合はカッコ内を1とかにする）
    cap = cv2.VideoCapture(0)

    # カウント変数(保存画像の連番用)
    image_number = 1

    while True:
        # フレーム取得
        ret, frame = cap.read()

        # フレームが取得できなければ終了
        if not ret:
            break

        # 映像を表示する
        cv2.imshow("Webcam", frame)

        # キー入力を待つ
        key = cv2.waitKey(1) & 0xFF

        # 's'キーが押されたら
        if key == ord('s'):
            # フレームがピンボケしていなければ保存
            if check_blurry_photo(frame)==False:
                # ピントが合っている場合のみ画像を保存
                image_number += 1
                cv2.imwrite(f"image_{image_number}.png", frame)

        elif key == ord('q'):
            # 'q'キーが押されたら終了
            break

    # 終了処理
    cap.release()
    cv2.destroyAllWindows()
```



