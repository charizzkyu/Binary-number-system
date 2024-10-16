# Binary-number-system ---{group winners}---

Program to convert Binary Number System

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

  
    <meta name="title" content="Number System Converter">
    <meta name="description"
        content="Convert number system like (Decimal, Binary, Octal, Hexadecimal)">


    <title>Number System Converter</title>

    <style>
        body {
            background-color: #324efd;
            box-sizing: border-box;
            color: #ffffff;
            font-family: Arial, Helvetica, sans-serif;
            height: 100%;
            margin: 0;
            text-align: center;
            width: 100%;
        }

        #container {
            display: flex;
            margin: 50px auto;
            text-align: center;
            flex-flow: column;
            justify-content: center;
        }

        h1 {
            font-size: 3rem;
        }

        label {
            font-size: 1.5rem;
            font-weight: bold;
        }

        input {
            background-color: transparent;
            border-radius: 5px;
            border: 3px solid #ffffff;
            color: #ffffff;
            display: block;
            font-size: 30px;
            font-weight: bold;
            height: 50px;
            margin: 10px auto;
            outline: 1px solid transparent;
            text-align: center;
            text-transform: uppercase;
            transition: .3s ease;
            width: 40%;
        }

        input:focus {
            border: 3px solid #ffffff;
            width: 50%;
        }

        ::placeholder {
            color: #ffffff80;
            font-weight: normal;
        }

        footer {
            padding: 10px;
        }

        @media (max-width: 767px) {
            body {
                height: 100%;
            }

            h1 {
                font-size: 2rem;
            }

            input {
                width: 80%;
            }

            input:focus {
                width: 90%;
            }
        }
    </style>
</head>

<body>
    <div id="container">
        <h1>Convert Any Number</h1>
        <label for="input1">Decimal:</label>
        <input type="number" name="" id="input1" placeholder="Decimal Number">

        <label for="input2">Binary:</label>
        <input type="number" name="" id="input2" placeholder="Binary Number">

        <label for="input3">Octal:</label>
        <input type="number" name="" id="input3" placeholder="Octal Number">

        <label for="input4">Hexadecimal:</label>
        <input type="text" name="" id="input4" placeholder="Hexadecimal Number">
    </div>

    <footer><b>group Winners</b></footer><br>
    
    
    <footer>group Winners</footer>

    <script>
       
        let input1 = document.getElementById("input1"),
            input2 = document.getElementById("input2"),
            input3 = document.getElementById("input3"),
            input4 = document.getElementById("input4");
             function deciToAll() {
            let valInput1 = parseInt(input1.value, 10),
                valInput2 = parseInt(input2.value, 2),
                valInput3 = parseInt(input3.value, 8),
                valInput4 = parseInt(input4.value, 16);

            // Generate result
            input2.value = valInput1.toString(2).toUpperCase();
            input3.value = valInput1.toString(8).toUpperCase();
            input4.value = valInput1.toString(16).toUpperCase();
        }

        function octToAll() {
            // Local Variables for the value of input fields
            let valInput1 = parseInt(input1.value, 10),
                valInput2 = parseInt(input2.value, 2),
                valInput3 = parseInt(input3.value, 8),
                valInput4 = parseInt(input4.value, 16);

            // Generate result
            input1.value = valInput3.toString(10).toUpperCase();
            input2.value = valInput3.toString(2).toUpperCase();
            input4.value = valInput3.toString(16).toUpperCase();
        }

        function hexaToAll() {
            
            let valInput1 = parseInt(input1.value, 10),
                valInput2 = parseInt(input2.value, 2),
                valInput3 = parseInt(input3.value, 8),
                valInput4 = parseInt(input4.value, 16);

            input1.value = valInput4.toString(10).toUpperCase();
            input2.value = valInput4.toString(2).toUpperCase();
            input3.value = valInput4.toString(8).toUpperCase();
        }
        
        input1.addEventListener("keyup", function () {
            deciToAll();
        });
        
        input1.addEventListener("change", function () {
            deciToAll();
        });

        input2.addEventListener("keyup", function () {
            
            let valInput1 = parseInt(input1.value, 10),
                valInput2 = parseInt(input2.value, 2),
                valInput3 = parseInt(input3.value, 8),
                valInput4 = parseInt(input4.value, 16);

            
            input1.value = valInput2.toString(10).toUpperCase();
            input3.value = valInput2.toString(8).toUpperCase();
            input4.value = valInput2.toString(16).toUpperCase();
        });

        input3.addEventListener("keyup", function () {
            octToAll()
        });

        
        input3.addEventListener("change", function () {
            octToAll()
        });

         input4.addEventListener("keyup", function () {
            hexaToAll();
        });

        
        input4.addEventListener("change", function () {
            hexaToAll();
        });
    </script>
</body>

</html>