# Hook

[POST] https://call.servicechain.ru/hook

```
{
  "token":"token",
  "interface": "Name",
  "to": "client1",
  "from": "client",
  "data": {
    "id":"ID", 
    "extId": "ExtId",
    "status":"${Status}", 
    "response": "${реплика}"
    "chain": "chain"
   }
}
```
- token --  токен из авторизации
- interface -- 
- toAdress -- Ключ получателя в системе ServiceChain !!! не равен ID клиента в личном кабинете для предотвращения инъекций

- data.id -- ID заявки в системе отправителя
- data.extId -- ID заявки в системе получателя
- data.status -- статус в системе отправителя
- data.response -- реплика, данные дабавляются в ленту
- data.chain -- chain hash
