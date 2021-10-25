# Microservice Product

* Projede db olarak posgtresql kullanılmıştır. Uygulama ayağa kaldırılmadan önce db settingler yapılmalıdır.
## Postgresql DB Settings
* db name:db_product
* login group Role: admin  (burada yeni bir role tanımlanmış ve bu rol ile işlem yapılmıştır.)
* group role password:12345
* db schema:sc_product

* Db ayarları yapıldıktan sonra proje içindeki lokal istekler isimli yardımcı dosya ile postman üzerinden test edilebilir. Örnek get post metodları ise aşağıdaki gibidir. Ayrıca proje heroku ya deploy edildiğinden dolayı heroku istekler isimli dosyadaki metodlar ile heroku ya istek atabilirsiniz.

### Endpoints:

#### Save Product

````
POST /api/product HTTP/1.1
Host: localhost:3333
Authorization: Basic base64(username:password)
Content-Type: application/json
Content-Length: 42

{
    "name": "test-1",
    "price": 1.2
}
````

#### Get Products

```
GET /api/product HTTP/1.1
Host: localhost:3333
Authorization: Basic base64(username:password)
```

#### Delete Product

```
DELETE /api/product/{productId} HTTP/1.1
Host: localhost:3333
Authorization: Basic base64(username:password)
```
