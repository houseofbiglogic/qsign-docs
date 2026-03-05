# Genel Hata Kodları

Aşağıda bulunan bütün metodların geri dönüş değerleri dokümantasyon içinde yazmaktadır.

Ancak aşağıda yazılı olan dönüş tipleri bütün metodlar için geçerlidir. Bu yüzden
bu dönüş tipleri her method içine ayrıca bir kere daha yazılmadı.

|HTTP Status Code|Kısa Açıklama|Detay|
|--|--|--|
|429| Too many request | Method'a yapılan çağrı belirlenen birim süre içinde çok fazla yapılmış. Her bir method'un çağrı aralığı bilgisi, method'un açıklama kısmında verilmiştir. Bu çağrı sonucunda bir çıktı olmaz, sadece HTTP Status Code geri döner. |
|400| Bad request | Birçok durumda girişi yapılan veride hata olabiliyor. Bu durumda sistemin üzerinde tanımlı olan kontrol mekanizmaları otomatik olarak size hatalı olan alan ile ilgili bilgi veriyor. [see](#badrequest)|

### Bad Request (400)
<a name="badrequest" />

```javascript
{
	"Errors": [
	{
		"Message": "<string>",
		"Reason": "<string>"
	},
	...
	]
}
```
