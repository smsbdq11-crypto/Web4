# Web4

<!DOCTYPE html>
<html>

<head>

    <title>Sarah's Age Calculator</title>

    <style>

        body {
            background-color: #ffe6ef;
            font-family: Arial;
            text-align: center;
            padding-top: 100px;
        }

        .box {
            background-color: white;
            width: 350px;
            margin: auto;
            padding: 30px;
            border-radius: 25px;
        }

        h1 {
            color: #d94f7d;
        }

        p {
            color: #777;
            font-size: 18px;
        }

        input {
            padding: 12px;
            border: 2px solid #f3a6bd;
            border-radius: 10px;
            font-size: 16px;
        }

        button {
            background-color: #e8789d;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 15px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #d94f7d;
        }

        #result {
            color: #d94f7d;
            margin-top: 25px;
        }

    </style>

</head>


<body>


    <div class="box">

        <h1>🎀 Sarah's Age Calculator 🎀</h1>

        <p>Enter your date of birth</p>

        <input type="date" id="birthDate">

        <br><br>

        <button onclick="calculateAge()">
            Calculate My Age
        </button>

        <h2 id="result"></h2>

    </div>


    <script>

        function calculateAge() {

            let birthDate =
                document.getElementById("birthDate").value;

            let birth =
                new Date(birthDate);

            let today =
                new Date();

            let age =
                today.getFullYear() -
                birth.getFullYear();


            if (
                today.getMonth() < birth.getMonth() ||
                (
                    today.getMonth() == birth.getMonth() &&
                    today.getDate() < birth.getDate()
                )
            ) {

                age--;

            }


            document.getElementById("result").innerHTML =
                "You are " + age + " years old 🎂💕";

        }

    </script>


</body>

</html>
