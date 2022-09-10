
# [Mustapp](https://mustapp.com) API

<details>
  <summary>
    <img src="https://via.placeholder.com/15/881ADF/881ADF.png" /> <b>POST</b> - <i><code>/api/acc/anonymous</code></i> - Obtaining a Bearer token.
  </summary>
  
 ### Request
 
  &emsp;&emsp;**POST** ```https://mustapp.com/api/acc/anonymous```
  
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
