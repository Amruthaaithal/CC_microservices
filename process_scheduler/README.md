🧩 Endpoints: All these are effectively handled through UI written in index.html

i. 📌 `POST /add`

Adds a new process to the scheduler and registers its memory usage with the shared memory microservice, through the form created using index.html

Request Body (JSON):
{
  "pid": "P1",
  "arrival_time": 0,
  "burst_time": 5,
  "memory_required": 100
}

ii. 📌 `GET /processes`

Returns the list of all currently added processes in the form of table.

eg:
[
  {
    "arrival_time": 12,
    "burst_time": 4,
    "memory_required": 123,
    "pid": "6"
  },
  {
    "arrival_time": 12,
    "burst_time": 4,
    "memory_required": 123,
    "pid": "6"
  }
]

iii. 📌 `GET /simulate?method=<algorithm>&quantum=<optional>`

Simulates process scheduling using the specified algorithm.

Response (JSON):
[
  {
    "pid": "P1",
    "start_time": 0,
    "completion_time": 5,
    "turnaround_time": 5,
    "waiting_time": 0
  },
  ...
]
