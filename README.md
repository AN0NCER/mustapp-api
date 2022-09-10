
## **Mustapp API** <sup><code>1.0.0</code></sup>

[Base URL: https://mustapp.com]

This API was taken from the Mustapp application. To use requests, you need to specify Bearer which I designated as <token>

<details>
<summary>
<sub> <img src="/methods/post.png" width="50" /></sub> - <i><h4><code>/api/acc/anonymous</code></h4></i> <sub>Obtaining a Bearer token.</sub>
</summary>

<table role="table">
 <thead>
  <tr align="Left"><th colspan="2">Responses</th></tr>
  <tr align="left"><th>Code</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td>200<br><br><br><br><br><br><br></td>
   <td>
   
   Successful operation
   
   ```js
   {
    "id" : 0,
    "token" : "string"
   }
   ```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Curl</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">
   
```curl
   curl "https://mustapp.com/api/acc/anonymous" \
	-X POST
```
 
 </td>
  </tr>
 </tbody>
</table>

</details>
	
<sup>We can say that everything starts with this request. This request creates a user in guest mode, then you can authorize</sup>

## View management

<details>
<summary>
<sub> <img src="/methods/post.png" width="50" /></sub> - <i><h4><code>/api/search</code></h4></i> <sub>Search in DB (users, movies, shows, pesons, users, generes).</sub>
</summary>

<table role="table">
 <thead>
  <tr align="Left"><th colspan="2">Headers</th></tr>
  <tr align="left"><th>Name</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td><b>Bearer</b> <br><code>string</code><br><sup>token</sup></td>
   <td>A unique token that is needed to link to the user's account. Not required for search<br><br><br></td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Body</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">

```js
{
  "query": "string",
  "types": [
    "movies",
    "shows",
    "persons",
    "users",
    "genres"
  ]
}
```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Responses</th></tr>
  <tr align="left"><th>Code</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td>200<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
   <td>
   
   Successful operation
   
```js
{
  "persons" : [
    0
  ],
  "users" : [
    0
  ],
  "genres" : [
    0
  ],
  "movies" : [
    0
  ],
  "shows" : [
    0
  ],
  "products" : [
    0
  ]
}
```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Curl</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">
   
```curl
curl "https://mustapp.com/api/search" \
	-X POST \
	-H 'Content-Type: application/json; charset=utf-8' \
	-d '{"query":"string","types":["movies","shows","persons","users","genres"]}'
```
 
 </td>
  </tr>
 </tbody>
</table>

</details>
	
## Authorization

<details>
<summary>
<sub> <img src="/methods/put.png" width="50" /></sub> - <i><h4><code>/api/acc/apple</code></h4></i> <sub>Loggin whith apple ID.</sub>
</summary>

<table role="table">
 <thead>
  <tr align="Left"><th colspan="2">Headers</th></tr>
  <tr align="left"><th>Name</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td><b>Bearer</b> <br><code>string</code><br><sup>token</sup></td>
   <td>A unique token that is needed to link to the user's account<br><br><br></td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Body</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">

```js
{
  "app_id": "ru.ayyo.must",
  "force": false,
  "code": "string",
  "name": "string"
}
```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Responses</th></tr>
  <tr align="left"><th>Code</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td>200<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br></td>
   <td>
   
   Successful operation
   
```js
{
  "name": null,
  "phone": null,
  "facebook_name": null,
  "facebook_id": null,
  "twitter_name": null,
  "twitter_id": null,
  "is_private": false,
  "timezone": "string",
  "has_default_uri": false,
  "store_country_code": "string",
  "cinema_country_code": "string",
  "prefered_language_code": "string",
  "gender": null,
  "image_uri": null,
  "bio_message": null,
  "links": {},
  "google_id": null,
  "google_name": null,
  "is_youtube_linked": null,
  "apple_id": "string",
  "apple_email": "string",
  "apple_name": null,
  "id": 0,
  "uri": "string",
  "is_anonymous": false
}
```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Curl</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">
   
```curl
curl "https://mustapp.com/api/acc/apple" \
	-X PUT \
	-H 'Bearer: <token>' \
	-d '{"code":"string","force":false,"app_id":"ru.ayyo.must","name":"string"}'
```
 
 </td>
  </tr>
 </tbody>
</table>

</details>

<details>
<summary>
<sub> <img src="/methods/d-put.png" width="50" /></sub> - <i><h4><code>/api/acc/facebook</code></h4></i> <sub>Loggin whith facebook.</sub>
</summary>

<table role="table">
 <thead>
  <tr align="Left"><th colspan="2">Headers</th></tr>
  <tr align="left"><th>Name</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td><b>Bearer</b> <br><code>string</code><br><sup>token</sup></td>
   <td>A unique token that is needed to link to the user's account<br><br><br></td>
  </tr>
 </tbody>
</table>

</details>

<details>
<summary>
<sub> <img src="/methods/put.png" width="50" /></sub> - <i><h4><code>/api/acc/google</code></h4></i> <sub>Loggin whith Google.</sub>
</summary>

<table role="table">
 <thead>
  <tr align="Left"><th colspan="2">Headers</th></tr>
  <tr align="left"><th>Name</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td><b>Bearer</b> <br><code>string</code><br><sup>token</sup></td>
   <td>A unique token that is needed to link to the user's account<br><br><br></td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Body</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">

```js
  {
    "force": false,
    "authorization_code": "string"
  }
```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Responses</th></tr>
  <tr align="left"><th>Code</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td>200<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br></td>
   <td>
   
   Successful operation
   
```js
{
    "name": "string",
    "phone": "string",
    "facebook_name": null,
    "facebook_id": null,
    "twitter_name": null,
    "twitter_id": null,
    "is_private": true,
    "timezone": "string",
    "has_default_uri": false,
    "store_country_code": "string",
    "cinema_country_code": "string",
    "prefered_language_code": "string",
    "gender": "string",
    "image_uri": "string",
    "bio_message": null,
    "links": {},
    "google_id": "string",
    "google_name": "string",
    "is_youtube_linked": true,
    "apple_id": null,
    "apple_email": null,
    "apple_name": null,
    "id": 0,
    "uri": "string",
    "is_anonymous": false
  }
```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Curl</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">
   
```curl
curl "https://mustapp.com/api/acc/google" \
	-X PUT \
	-H 'Bearer: <token>' \
	-d '{"force":false,"authorization_code":"string"}'
```
 
 </td>
  </tr>
 </tbody>
</table>

</details>
	
## Session

<details>
<summary>
<sub> <img src="/methods/delete.png" width="50" /></sub> - <i><h4><code>/api/acc/session</code></h4></i> <sub>Delete activity session.</sub>
</summary>

<table role="table">
 <thead>
  <tr align="Left"><th colspan="2">Headers</th></tr>
  <tr align="left"><th>Name</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td><b>Bearer</b> <br><code>string</code><br><sup>token</sup></td>
   <td>A unique token that is needed to link to the user's account<br><br><br></td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Responses</th></tr>
  <tr align="left"><th>Code</th><th>Description</th></tr>
 </thead>
 <tbody>
  <tr>
   <td>204<br><br><br><br></td>
   <td>
   
   Successful operation
   
```js

```
   
   </td>
  </tr>
 </tbody>
 <thead>
  <tr align="Left"><th colspan="2">Curl</th></tr>
 </thead>
 <tbody>
  <tr>
   <td colspan="2">
   
```curl
curl "https://mustapp.com/api/acc/session" \
	-X DELETE \
	-H 'Bearer: <token>'
```
 
 </td>
  </tr>
 </tbody>
</table>

</details>
