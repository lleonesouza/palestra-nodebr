---
---

# EndPoints

<ApiCalls />


---
---

# COAP Config

```typescript
import * as coap from 'coap';

const options: coap.CoapRequestParams = {
    hostname: '192.168.0.11',  
    port: 5683,                
    pathname: '/v1/f/Health',     
    method: 'POST'
}

```

<br>

# Controller



```typescript
import Request from "./Request"
import {Response, Request} from "express"

function Controller(req: Request, res: Response){
    const response = Request(option, payload)

    res.send(response)
}

```


---


```typescript
import * as coap from 'coap';

function Request(options: coap.CoapRequestParams, payload: any){
  return new Promise((resolve, reject) => {
    const req = coap.request(options);

    req.on('response', (res) => {
      let responseData = '';

      res.on('data', (chunk) => {
        responseData += chunk;
      });

      res.on('end', () => {
        resolve(responseData);
      });
    });

    req.on('error', (error) => {
      reject(error);
    });

    req.write(payload);
    req.end();
  });
}

```

---
src: ./requests.md
hide: false
---


# Request Health

<img src="pages/coding/nodejs/Peek 2023-06-28 00-16.gif" alt="GIF" />
<img v-click class="absolute" src="pages/coding/nodejs/Peek 2023-06-28 00-03.gif" alt="GIF" />

<style>
img.absolute { 
     position: fixed;
  bottom: 0;
  right: 0;
   width: 300px;
  border: 3px solid #73AD21;
}
</style>

---

