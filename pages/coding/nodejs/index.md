---
---

# COAP Config

```typescript {all|1|4,5,6,7|all}
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


```typescript {all|2|3,4,5,6,7,8|all|1}
import Request from "./Request"
import {Response, Request} from "express"

function Controller(req: Request, res: Response){
    const response = Request(option, payload)

    res.send(response)
}

```


---


```typescript {all|1|3|4|3,5|7,8,9,10,11,12,13,14,15,16,17|19,20,21,22|3,23|24|all}
import * as coap from 'coap';

function Request(options: coap.CoapRequestParams, payload: string){
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

# EndPoints

<ApiCalls />

---
src: ./requests.md
hide: false
---
