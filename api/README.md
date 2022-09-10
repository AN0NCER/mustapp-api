
# [Mustapp](https://mustapp.com) API

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

# Authorization

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
    <img src="https://via.placeholder.com/15/f03c15/f03c15.png" /> <b>METHOD</b> - <i><code>url</code></i> - This is a web request template.
  </summary>
  
  ### Request
 
  **METHOD** ```https://localhost/url```
  
  ### Headers
  
  - `Bearer = token`
  
  ### Curl
  
  ```curl
  curl "https://localhost/url/" \
	-H 'Bearer: <token>'
  ```
  
</details>
