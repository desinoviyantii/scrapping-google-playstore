### SCRAPPING FOR SENTIMENT ANALYSIS

**Installation**<br>
```
pip install google-play-scraper
```

**Example**<br>
https://play.google.com/store/apps/details?id=id.bni.wondr&hl=en
```
app_id = 'id.bni.wondr'

result, token = reviews(
    app_id,                 # ID aplikasi
    lang='id',              # Bahasa Indonesia
    country='id',           # Review dari Indonesia
    sort=Sort.NEWEST,       # Urutkan dari yang terbaru
    filter_score_with=None, # Ambil semua skor (1-5)
    count=100000            # Ambil hingga 100.000 review (dibatasi oleh Google)
)
```

**Execution**<br>
Sentiment Analysis menggunakan Gemini API, salah satu model yang digunakan yaitu **gemini-2.5-flash**
```
model = genai.GenerativeModel('gemini-2.5-flash')
```
Model yang digunakan free, sehingga terdapat batasan setiap running code. Oleh karena itu dapat dilihat lebih detail melalui [dokumentasi berikut](https://share.google/zQmy9uIKLW9fpBIDq)

**Result**<br>


