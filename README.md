# 대동유어지도 로그인

#### api endpoint: https://wtdhqxavjk.execute-api.us-east-2.amazonaws.com/auth/

#### signiture(axios)

```
axios.post('https://wtdhqxavjk.execute-api.us-east-2.amazonaws.com/auth/', {
                id: 'id',
                password: 'password'
            })
```

#### response body
- success
```
body: JSON.stringify({
                // 암호화 토큰
                token: hmacDigest,
                // 사용자 정보
                id: ID,
                password: PASSWORD,
                name: NAME
            })
```
- fail

```
// 403 not authorized response
statusCode: 403
```


### sample app

#### 로그인 - 올바르지 않은 정보 기입


![image](https://user-images.githubusercontent.com/66404645/230878973-889c9432-d076-415f-b9ea-4a556d81af59.png)

![image](https://user-images.githubusercontent.com/66404645/230879097-c4e16824-fc57-4c45-870d-199d803fd71f.png)

- 403 not authorized response
- 에러 메세지 출력


#### 로그인 - 올바른 정보 기입

![image](https://user-images.githubusercontent.com/66404645/230879902-d993556a-ce58-4f0d-aa9b-82ed970df7dd.png)

![image](https://user-images.githubusercontent.com/66404645/230879788-2cd65be0-ca1f-4da6-9eb7-d95c3fedb663.png)

- 200 response
- main page routing
