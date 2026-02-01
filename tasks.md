Collection: tasks


Description:
Stores tasks assigned for each topic.


Fields:
- _id (string) – unique task id
- title (string)
- topic_id (string → topics._id)
- due_date (date)
- submitted_users (array of user _id)