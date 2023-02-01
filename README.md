# Dog API 🐶🦴💾


Your task is to implement the Create and Read parts of a CRUD API, i.e. a CR API (pronounced KERRRR 🙃).


## Guidelines


You are not expected to use a real database for your solution, but you should structure your code so that adding a database would have minimal impact on your code.
Try to structure your code as if it where a part of a professional codebase. Your solution will be reviewed and a potential follow-up meeting might be scheduled to discuss the solution.




## Dog Entity


This data type represents how the API is expected to respond with a Dog that is persited on the backend.


| field | type | format | required |
| :--- | :--- | :--- | :--- |
| id | string | uuid | ✅ |
| birthDate | string | ISO Date | ✅ |
| breed | string |  |  |
| name | string |  | ✅ |


Here's an example of how that payload might look like:


```json
{
   "id":"eedf7f04-a4c4-4049-876d-fad6413bb435",
   "birthDate":"2022-02-02",
   "breed":"Rough Collie",
   "name":"Lassie"
}


```


## Dog Request Entity
This data type represent how the API should expect a Dog as request payload:
| field | type | format | required |
| :--- | :--- | :--- | :--- |
| birthDate | string | ISO Date | ✅ |
| breed | string |  |  |
| name | string |  | ✅ |


Here's an example of how that payload might look like:


```json
{
   "birthDate":"2022-02-02",
   "breed":"Rough Collie",
   "name":"Lassie"
}


```
## Endpoints
This section describes the endpoints that you're expected to implement.
### `POST /dogs`


This endpoint creates/persists a new dog on the server


| Body | Content-Type | Response
| :--- | :--- | :--- |
| [Dog Request](#dog-request-entity) | `application/json` |  [Dog](#dog-entity) |


The expected status codes are


| Status Code | Description |
| :--- | :--- |
| 200 | `OK` |
| 400 | `BAD REQUEST` |


### `GET /dogs`
This endpoint returns an array of all dogs. In the case where there are no existing dogs, it's fine to return an empty array.


| Body | Content-Type | Response
| :--- | :--- | :--- |
| `NONE` | `application/json` |  [Dog](#dog-entity)[] |


The expected status codes are


| Status Code | Description |
| :--- | :--- |
| 200 | `OK` |




### `GET /dogs/:id`


This endpoint returns a [Dog](#dog-entity) given its `id` provided as a parameter in the path.


The expected status codes are


| Status Code | Description |
| :--- | :--- |
| 200 | `OK` |
| 400 | `BAD REQUEST` |
| 404 | `NOT FOUND` |


## Test
Since we are mostly interested in how you solve a problem rather than checking if you have covered all edge-cases. We have provided a testfile for you to run and validate your solutions against.


To install all the dependencies for the test, execute the following command:


```bash
pip3 install -r requirements.txt
```


This can be executed from the root of this repository via:
```bash
python3 test.py <URL_TO_YOUR_API>
```


## Submitting

When you are finished with the implementation, please share the code with us so that we can review it.
Please add some information on how to start your server and any dependencies in the section below. Bonus points if you package your application with Docker, but it's not required for this task.


## How to run
```bash
PLEASE INSERT START COMMAND HERE
```

