# Hook

[POST] https://bus.servicechain.ru/webhook

```
{
  "token":"${authToken}",
  "interface": "${unit}",
  "to": "${toAdress}",
  "data": {
    "id":"${FromId}", 
    "extId": "${ToID}", 
    "status":"${Status}", 
    "response": "${реплика}"
   }
}
```
- token --  токен из авторизации
- interface -- unit
- toAdress -- Ключ получателя в системе ServiceChain !!! не равен ID клиента в личном кабинете для предотвращения инъекций

- data.id -- ID заявки в системе отправителя
- data.extId -- ID заявки в системе получателя
- data.status -- статус в системе отправителя
- data.response -- реплика, данные дабавляются в ленту
