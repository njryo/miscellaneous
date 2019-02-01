# kaggle用のスニペット

## Google Colabにkaggleのデータをダウンロード

kaggleのAPIでデータをダウンロードする方法。

あらかじめ、kaggleのアカウントページのCreate New API Tokenでkaggle.jsonをダウンロードしておく。

以下で、kaggle.jsonをアップロード。
```
from google.colab import files
files.upload()
```

kaggle.jsonを適切なとこに移動させて、pipでパッケージをインストール。
```
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 /root/.kaggle/kaggle.json
!pip install kaggle
```

あとは
```
!kaggle competitions download -c <competition_name>
```
でデータをダウンロード（competition_nameのとこは各コンペのDataのページを参照）。
