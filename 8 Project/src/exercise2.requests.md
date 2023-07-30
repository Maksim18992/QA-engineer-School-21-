# Какой запрос(-ы) отправляется на сервер для получения списка типов товаров в шторке "Каталог"?
- POST https://sbermegamarket.ru/api/mobile/v1/catalogService/catalog/menu
- GET https://extra-cdn.sbermegamarket.ru/static/dist/images/menu-spoiler-toggler.7fb779.svg

# Какой запрос(-ы) отправляется на сервер при использовании поиска товаров в каталоге?
- POST https://sbermegamarket.ru/api/mobile/v1/catalogService/filters/search
- POST https://sbermegamarket.ru/api/mobile/v1/seoService/seo/search
- POST https://sbermegamarket.ru/api/mobile/v1/catalogService/catalog/search
- POST https://sbermegamarket.ru/api/mobile/v2/cartService/cart/search
- POST https://sbermegamarket.ru/api/mobile/v3/catalogService/catalog/searchSuggest

# Какой запрос(-ы) отправляется на сервер при поиске региона или города в модалке выбора вашего региона?
- POST https://sbermegamarket.ru/api/mobile/v1/addressSuggestService/address/suggest
- POST https://sbermegamarket.ru/api/mobile/v1/profileService/address/list