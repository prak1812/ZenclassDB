1. Topics and tasks taught in October


db.topics.find({
date: { $gte: ISODate("2020-10-01"), $lte: ISODate("2020-10-31") }
})


db.tasks.find({
due_date: { $gte: ISODate("2020-10-01"), $lte: ISODate("2020-10-31") }
})
any drives between 15–31 Oct 2020


db.company_drives.find({
date: { $gte: ISODate("2020-10-15"), $lte: ISODate("2020-10-31") }
})


3. Company drives and students appeared


db.company_drives.find({}, { company_name: 1, students_appeared: 1 })


4. Problems solved by a user
ekata.find({ user_id: "U1" })


5. Mentors with more than 15 mentees


db.mentors.find({
$expr: { $gt: [ { $size: "$mentees" }, 15 ] }
})


6. Users absent and task not submitted between 15–31 Oct


db.attendance.find({
status: "absent",
date: { $gte: ISODate("2020-10-15"),$lte: ISODate("2020-10-31") }
})