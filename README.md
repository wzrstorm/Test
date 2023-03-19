<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>信息收集表单</title>
    <style>
        /* 页面样式 */
        body {
            font-family: Arial, sans-serif;
            background-color: #f8f9fa;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 600px;
            margin: 30px auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            font-size: 24px;
        }
        form {
            display: flex;
            flex-direction: column;
        }
        label {
            font-weight: bold;
            margin-top: 15px;
        }
        input, textarea, select {
            margin-top: 5px;
            font-size: 14px;
            padding: 5px;
            border: 1px solid #ccc;
        }
        input[type="submit"] {
            margin-top: 20px;
            background-color: #007bff;
            color: #fff;
            font-size: 16px;
            font-weight: bold;
            border: none;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>学生测评信息收集</h1>
        <!-- 将您的Formspree电子邮件地址替换为实际的地址 -->
        <form action="https://formspree.io/f/mrgvazpd" method="POST" enctype="multipart/form-data">
            <label for="class">班级</label>
            <input type="text" id="class" name="class" required>

            <label for="name">姓名</label>
            <input type="text" id="name" name="name" required>

            <label for="student_id">学号</label>
            <input type="text" id="student_id" name="student_id" required>

            <label for="score">测评成绩</label>
            <input type="text" id="score" name="score" required>
            
            <input type="submit" value="提交">
        </form>
    </div>
<script>
    document.querySelector("form").addEventListener("submit", function (event) {
        // 确保所有字段都已填写
        if (
            !document.getElementById("class").value ||
            !document.getElementById("name").value ||
            !document.getElementById("student_id").value ||
            !document.getElementById("score").value ||
        ) {
            event.preventDefault(); // 阻止表单提交
            alert("请填写完整信息！"); // 显示提示信息
            return;
        }

        // 如果所有字段都已填写，则显示“提交成功”信息
        event.target.addEventListener("submit", function () {
            alert("提交成功");
        });
    });
</script>
</body>
</html>
