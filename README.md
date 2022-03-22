# nurbekdev foydalanuvchi hissasi grafigida

foydalanuvchi hissasi grafigida nurbekdev qiling, uning SVG tasvirini yarating va nihoyat uni omboringizga qaytaring.

Natijaga misol:
[![nurbekdev/n](gitartwork.svg)](https://github.com/nurbekdev/n)

## Foydalanish:

### Variant №1: nurbekdevdan GitHub harakati sifatida foydalaning
1. Ish jarayoni kodini omboringizdagi `.github/workflows/gitartwork.yml` fayliga nusxalang.

        name: gitartwork from a contribution graph
        on: 
          push:
          schedule:
            - cron: '* */24 * * *'
          workflow_dispatch:
        jobs:
          build:
            name: Make gitartwork SVG
            runs-on: ubuntu-latest
            steps:
              - uses: actions/checkout@v2
              - uses: jasineri/gitartwork@v1
                with:
                   # Use this username's contribution graph  
                   user_name: nurbek
                   # Text on contribution graph 
                   text: nurbek
              - uses: jasineri/simple-push-action@v1

2.Bir necha daqiqadan so'ng u sizning omboringizda `gitartwork.svg` tasvirini yaratadi, shuning uchun uni `![gitartwork](gitartwork.svg)` kabi `README.md` ga qo`shishingiz mumkin.

3. Bahra oling; vaqtni chog 'o'tkazing :)

