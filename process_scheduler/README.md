🧩 Endpoints:

i. 📌 POST /add
Adds a new process to the scheduler and registers its memory usage with the shared memory microservice, through the form created using index.html

Request Body (JSON):
{
  "pid": "P1",
  "arrival_time": 0,
  "burst_time": 5,
  "memory_required": 100
}
