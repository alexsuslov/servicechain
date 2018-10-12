## Webhook

### Test json
test.json
```
{
  "token":"oocah5Pi",
  "interface":"response",
  "to": "letual",
  "data": {
    "number": "00597108",
    "extId": "386543",
    "status": "5",
    "response": "test1 response"
  }
}
```

### Test command
```
curl -XPOST\
    -H 'Content-Type:application/json' \
    -H 'Accept: application/json' \
    --data-binary @./test.json \
    https://servicechain.ru/hook
```

## Response
look like:
```
{"ReqId":386545,"warning":"UpdateSC: ServiceCall not updated (may be equals)"}
```

"status": "1",

```
{"oldReqStatusExternal":"Отклонено","ReqId":386545,"281526732523427":"Выполнено","newReqStatusExternal":"Принят","281537387955975":"Отклонено"}

```

