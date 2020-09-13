# test-tesseract

&#x26a0; 2020/09/13現在 以下のエラーが発生して動作しません

```sh
[vagrant@localhost ~]$ tesseract /vagrant_data/Tesseract_OCR_logo.png out -l eng
Tesseract Open Source OCR Engine v3.04.02dev with Leptonica
Empty page!!
Empty page!!
```

# Usage

## host

```sh
vagrant up
vagrant ssh
```

## guest

```sh
export TESSDATA_PREFIX=/usr/local/src/tesseract/

# traineddataをコピー
sudo cp /vagrant_data/eng.traineddata /usr/local/src/tesseract/tessdata/eng.traineddata
sudo cp /vagrant_data/jpn.traineddata /usr/local/src/tesseract/tessdata/jpn.traineddata
tesseract /vagrant_data/Tesseract_OCR_logo.png out -l eng
```

## Link

- https://qiita.com/hatahata/items/4daddebb5e84ea575332
- https://github.com/tesseract-ocr/tessdata
