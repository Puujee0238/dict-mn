# dict-mn

Энэхүү монгол хэлний толь нь [hunspell](http://hunspell.github.io) үгийн алдаа шалгагчид тулгуурлан ажиллах бөгөөд 36 мянга орчим үндэс, тэдгээрийн 200 сая гаруй хувилал бүхий үгийн санг агуулсан.

Толийн онцлогийг дурдвал:

-   Эрдэмтэн Ц. Дамдинсүрэн нарын "Монгол үсгийн дүрмийн толь", "Монгол хэлний хадмал толь", "Монгол хэлний их тайлбар толь" болон "Монгол хэлний зөв бичих дүрмийн журамласан толь" зэрэг бүтээлүүдийг тусгасан
-   Нөхцөлийн угсруулан холбох зарчимд тулгуурласан (hunspell v1.3.3-аас хойших хувилбарт ажиллана)
-   Алдаатай үгийн зөв хувилбарыг оновчтой тодорхойлно
-   Morphological analysis
-   Stemming

# hunspell ашиглах

Хэрэв таны ашиглаж буй программ hunspell дэмждэггүй эсвэл та их хэмжээний өгөгдлийн бүх алдаатай үгсийг давхцалгүйгээр жагсаалт болгон харахыг хүсвэл hunspell программыг дараах байдлаар ашиглахыг зөвлөж байна.

Юун түрүүнд [hunspell](https://github.com/hunspell/hunspell) алдаа шалгагчаа суулгасан байх хэрэгтэй. Хэрхэн суулгах мэдээллийг [https://github.com/hunspell/hunspell](https://github.com/hunspell/hunspell) хаягаас мөн авах боломжтой.

## hunspell суулгах

Linux үйлдлийн систем дээр суулгах бол

```
sudo apt install hunspell
```

Mac үйлдлийн систем дээр суулгах бол

```
brew install hunspell
```

Windows үйлдлийн систем дээр суулгах бол [Chocolatey](https://chocolatey.org) ашиглаж болно

```
choco install hunspell.portable
```

Ийнхүү суулгасан бол толь (`mn_MN.aff`, `mn_MN.dic`) байрлаж буй замыг дараах байдлаар оруулж өгнө

```
hunspell -d <your-location>/mn_MN,en_US -l input.txt | sort | uniq > output.txt
```

Дээрх жишээнд монгол, англи толиудыг зэрэг ашигласан байна. Ихэнх программуудад олон толийг нэгэн зэрэг ашиглах боломжгүй байдаг бөгөөд энэ тохиолдолд толиудаа нэгтгэх хэрэгтэй болдог. Үүний тулд [hunspell-merge](https://github.com/arty-name/hunspell-merge) ашиглахыг зөвлөж байна.
