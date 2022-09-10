
<h1> Mustapp API <sup><code>1.0.0</code></sup></h1>

<details>
<summary>
<sub> <img src="/methods/post.png" width="50" /></sub> - <i><h4><code>/api/acc/anonymous</code></h4></i> <sub>Obtaining a Bearer token.</sub>
</summary>

| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |

</details>

<details>
  <summary>
    <h4><img src="https://via.placeholder.com/15/881ADF/881ADF.png" /> <b>POST</b> - <i><code>/api/acc/anonymous</code></i> - Obtaining a Bearer token.</h4>
  </summary>
  
 ### Request
 
  &emsp;&emsp;**POST** ```https://mustapp.com/api/acc/anonymous```
  
<h4>Response</h4>
	
```js
{
"id" : 638737,
"token" : "token"
}
```
  
  ### Curl
  
  ```curl
  curl "https://mustapp.com/api/acc/anonymous" \
	-X POST
  ```
  
</details>

# Account

<details>
  <summary>
    <h4><img src="https://via.placeholder.com/15/1ADFDF/1ADFDF.png" /> <b>PUT</b> - <i><code>/api/acc/apple</code></i> - Loggin whith apple ID.</h4>
  </summary>
	
 ### Request
 
  &emsp;&emsp;**PUT** ```https://mustapp.com/api/acc/apple```
	
### Header
	
  - `Bearer: <token>`
  
<h4>Body</h4>
	
```js
{
  "app_id": "ru.ayyo.must",
  "force": false,
  "code": "cd0c7fe25c1d14422843485df675f71b3.0.rwyu.hT8IxyN6M79k7X4vGphlVg",
  "name": " "
}
```
	
<h4>Response</h4>
	
```js
{
  "name": null,
  "phone": null,
  "facebook_name": null,
  "facebook_id": null,
  "twitter_name": null,
  "twitter_id": null,
  "is_private": false,
  "timezone": "MSK",
  "has_default_uri": false,
  "store_country_code": "ua",
  "cinema_country_code": "ua",
  "prefered_language_code": "ru",
  "gender": null,
  "image_uri": null,
  "bio_message": null,
  "links": {},
  "google_id": null,
  "google_name": null,
  "is_youtube_linked": null,
  "apple_id": "000684.38d3de46c2db4fc5849d741b4d645158.1647",
  "apple_email": "dm9gn9959z@privaterelay.appleid.com",
  "apple_name": null,
  "id": 489687,
  "uri": "anoncer",
  "is_anonymous": false
}
```
  
  ### Curl
  
```curl
curl "https://mustapp.com/api/acc/apple" \
	-X PUT \
	-H 'Bearer: <token>' \
	-d '{"code":"cd0c7fe25c1d14422843485df675f71b3.0.rwyu.hT8IxyN6M79k7X4vGphlVg","force":false,"app_id":"ru.ayyo.must","name":" "}'
```
  
</details>

<details>
  <summary>
    <h4><img src="https://via.placeholder.com/15/1ADFDF/1ADFDF.png" /> <b>PUT</b> - <i><code>/api/acc/facebook</code></i> - Loggin whith facebook.</h4>
  </summary>
	
 ### Request
 
  &emsp;&emsp;**PUT** ```https://mustapp.com/api/acc/facebook```
	
### Header
	
  - `Bearer: <token>`

</details>

<details>
  <summary>
    <h4><img src="https://via.placeholder.com/15/1ADFDF/1ADFDF.png" /> <b>PUT</b> - <i><code>/api/acc/google</code></i> - Loggin whith google.</h4>
  </summary>
	
 ### Request
 
  &emsp;&emsp;**PUT** ```https://mustapp.com/api/acc/google```
	
### Header
	
  - `Bearer: <token>`
  
<h4>Body</h4>
	
```js
{
  "force": false,
  "authorization_code": "4/0AdQt8qghlCTOq_2eWDs-ft2zTaGI3mGUqNaJXjY6wTVe-LD6B_RqLMYcZiwUlGog93v7Vg"
}
```
	
<h4>Response</h4>
	
```js
{
  "name": "AN0NC6R",
  "phone": "+380000000000",
  "facebook_name": null,
  "facebook_id": null,
  "twitter_name": null,
  "twitter_id": null,
  "is_private": true,
  "timezone": "Europe/Berlin",
  "has_default_uri": false,
  "store_country_code": "ua",
  "cinema_country_code": "ua",
  "prefered_language_code": "ru",
  "gender": "male",
  "image_uri": "/b250671a-3f42-4244-bce3-b14d951ff164.jpg",
  "bio_message": null,
  "links": {},
  "google_id": "example@gmail.com",
  "google_name": "Anoncer",
  "is_youtube_linked": true,
  "apple_id": null,
  "apple_email": null,
  "apple_name": null,
  "id": 356592,
  "uri": "MaximKov",
  "is_anonymous": false
}
```
  
  ### Curl
  
```curl
curl "https://mustapp.com/api/acc/google" \
	-X PUT \
	-H 'Bearer: <token>' \
	-d '{"force":false,"authorization_code":"4\/0AdQt8qghlCTOq_2eWDs-ft2zTaGI3mGUqNaJXjY6wTVe-LD6B_RqLMYcZiwUlGog93v7Vg"}'
```
  
</details>
<details>
  <summary>
    <h4><img src="https://via.placeholder.com/15/DF1A1A/DF1A1A.png" /> <b>DELETE</b> - <i><code>/api/acc/session</code></i> - Delete session.</h4>
  </summary>
	
 ### Request
 
  &emsp;&emsp;**DELETE** ```https://mustapp.com/api/acc/session```
	
### Header
	
  - `Bearer: <token>`
  
<h4>Body</h4>
	
```js
```
	
<h4>Response</h4>
	
```js
204
```
  
  ### Curl
  
```curl
curl "https://mustapp.com/api/acc/session" \
	-X DELETE \
	-H 'Bearer: <token>'
```
  
</details>
