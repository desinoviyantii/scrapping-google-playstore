### SCRAPPING GOOGLE PLAYSTORE

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

**Result**<br>
```
df_playstore = pd.DataFrame(np.array(result), columns=['review'])
df_playstore = df_playstore.join(pd.DataFrame(df_playstore.pop('review').tolist()))
```


