#calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, intial-scale=1.0">
    <link rel="stylsheet" href="style.css">
    <title>calcutor</title>
</head>
<body>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body{
    width: 90%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(45deg,
     #0a0a0a, #3a4452);
}

.calculator{
    width: 85%;
    border: 1px solid #717377;
    padding: 20px;
    border-radius: 16px;
    background: transparent;
    box-shadow: 0px 3px 15px rgba(113, 115, 
    119, 0.5);
}

input{
    width: 80%;
    border: none;
    padding: 24px;
    margin: 10px;
    background: transparent;
    box-shadow: 0px 3px 15px rgbs(84, 84, 84,
    0.1);
    font-size: 40px;
    text-align: right;
    cursor: pointer;
    color: #ffffff;
}

input::placeholder{
    color: #ffffff;
}

button{
    border: none;
    width: 60px;
    height: 60px;
    margin: 10px;
    border-radius: 50%;
    background: transparent;
    color: #ffffff;
    font-size: 10px;
    box-shadow: -8px -8px 15px rgba(255, 
    255, 255, 0.1);
    cursor: pointer;
    color: #ffffff;
}

.equalBTn{
    background-color: #fb7c14;
}

.operator{
    color: #6dee0a;

}
</style> 
<body>
    <div id="calculator">
        <input types="text" placeholder="0">
        <div>
            <button class="operator">AC</button>
            <button class="operator">DEL</button>
            <button class="operator">%</button>
            <button class="operator">/</button>
        </div>
        <div>
            <button>7</button>
            <button>8</button>
            <button>9</button>
            <button class="operator">*</button>
        </div>
        <div>
            <button>4</button>
            <button>5</button>
            <button>6</button>
            <button class="operator">-</button>
        </div>
        <div>
            <button>1</button>
            <button>2</button>
            <button>3</button>
            <button class="operator">+</button>
        </div>
        <div>
            <button>00</button>
            <button>0</button>
            <button>.</button>
            <button class="equalBTn">=</button>
        </div>   
    </div>
     <script>
      let input = document.getElementById('inputBox');
      let buttons = document.querySelectorAll
      ('button')

      let string = "";
      let arr = Array.from(buttons);
      arr.forEach(button => {
      button.addEventListener( 'click', (e) => {
        if(e.target.innerHTML == '='){
            string = eval(string);
            input.value = sting;
        }
        else if(e.target.innerHTML == 'AC'){
            string = ""
            input.value = string;
        }
        else if(e.target.innerHTML == 'DEL'){
            string = string.substring(0,string.
            length-1);
            input.value = string;
        }
        else{
            string += e.target.innerHTML;
            input.value = string;    
        } 
    })
})
</script>
</body>
</html> 
