<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Online Attendance | Maa Saraswati Educational Institute</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    font-family:Arial,sans-serif;
    background:#f4f6fb;
    color:#222;
}

header{
    background:linear-gradient(135deg,#5b0aa8,#8e24aa);
    color:white;
    text-align:center;
    padding:28px 15px;
}

header h1{
    font-size:26px;
    margin-bottom:8px;
}

header p{
    font-size:16px;
}

.container{
    max-width:950px;
    margin:25px auto;
    padding:15px;
}

.card{
    background:white;
    padding:20px;
    margin-bottom:20px;
    border-radius:15px;
    box-shadow:0 4px 12px rgba(0,0,0,.1);
}

h2{
    color:#5b0aa8;
    margin-bottom:18px;
}

label{
    display:block;
    font-weight:bold;
    margin:10px 0 6px;
}

input,select{
    width:100%;
    padding:12px;
    border:1px solid #ccc;
    border-radius:8px;
    font-size:16px;
}

button{
    border:0;
    border-radius:7px;
    padding:10px 14px;
    margin:5px 2px;
    cursor:pointer;
    font-size:14px;
}

.add{
    width:100%;
    background:#5b0aa8;
    color:white;
    margin-top:15px;
}

.present{
    background:#198754;
    color:white;
}

.absent{
    background:#dc3545;
    color:white;
}

.delete{
    background:#555;
    color:white;
}

.clear{
    background:#222;
    color:white;
    width:100%;
    margin-top:15px;
}

.date{
    background:#f8f8f8;
    margin-bottom:15px;
}

.table-container{
    overflow-x:auto;
}

table{
    width:100%;
    border-collapse:collapse;
    min-width:700px;
}

th,td{
    border:1px solid #ddd;
    padding:11px;
    text-align:center;
}

th{
    background:#5b0aa8;
    color:white;
}

.status-present{
    color:#198754;
    font-weight:bold;
}

.status-absent{
    color:#dc3545;
    font-weight:bold;
}

.not-marked{
    color:#777;
    font-weight:bold;
}

.summary{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
}

.box{
    flex:1;
    min-width:130px;
    text-align:center;
    padding:18px;
    background:#f1e8ff;
    border-radius:10px;
}

.box h3{
    font-size:28px;
    color:#5b0aa8;
    margin-bottom:5px;
}

.empty{
    text-align:center;
    padding:20px;
    color:#777;
}

@media(max-width:600px){
    header h1{
        font-size:21px;
    }

    .card{
        padding:15px;
    }
}
</style>
</head>

<body>

<header>
    <h1>🌸 Maa Saraswati Educational Institute</h1>
    <p>📋 Online Attendance System</p>
</header>

<div class="container">

    <!-- Student Add Section -->
    <div class="card">

        <h2>👨‍🎓 Add Student</h2>

        <label>Student Name</label>
        <input
            type="text"
            id="studentName"
            placeholder="Enter student name"
        >

        <label>Class</label>
        <select id="studentClass">
            <option value="">Select Class</option>
            <option>Class 9</option>
            <option>Class 10</option>
            <option>Class 11</option>
            <option>Class 12</option>
        </select>

        <button class="add" onclick="addStudent()">
            ➕ Add Student
        </button>

    </div>


    <!-- Date -->
    <div class="card">

        <h2>📅 Attendance Date</h2>

        <input
            type="date"
            id="attendanceDate"
            class="date"
        >

    </div>


    <!-- Attendance -->
    <div class="card">

        <h2>📋 Mark Attendance</h2>

        <div class="table-container">

            <table>

                <thead>
                    <tr>
                        <th>S.No.</th>
                        <th>Student Name</th>
                        <th>Class</th>
                        <th>Status</
