# **Usage Instruction**

**==Docker is needed==**

1. First, set up the consul server for service registry:

`docker pull hashicorp/consul`

`docker run -d -p 8500:8500 hashicorp/consul consul agent -dev -client=0.0.0.0`

2. Then, download the executable files from [5594_Executable_Files](https://drive.google.com/drive/folders/115Memb2WfJusZ6Rt71P85IXIigN5wXFw?usp=sharing), and execute them to run the server:
3. Finally, use Postman or other tools to send the requests to `0.0.0.0:8080`.

e.g. Send a GET request to `0.0.0.0:8080/hello` with the following JSON body:

```json
{
  "user": {
    "id": "1",
    "name": "Aaron",
    "avatar": "IronMan",
    "address": "NUS",
    "mobile": "99999999"
  }
}
```

Send a POST request to 0.0.0.0:8080/product/insert with the following JSON body:

```json
{
  "product": {
    "id": "1",
    "name": "Infinity Gauntlet",
    "description": "A metal gauntlet used to house the six Infinity stones.",
    "amount": "0"
  }
}
```

| HTTP Method | Body    | URL                             |
| ----------- | ------- | ------------------------------- |
| `GET`       | User    | `localhost:8080/hello`          |
| `POST`      | User    | `localhost:8080/user/insert`    |
| `POST`      | Product | `localhost:8080/product/insert` |
