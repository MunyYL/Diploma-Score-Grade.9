![Doc2_Page_1](https://github.com/user-attachments/assets/91c77027-46c1-420b-adea-6c204c921114)
<!DOCTYPE html>
<html lang="en">
<head>
   
    <body>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diploma Score</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <img src="folder/Doc2_Page_1.png" alt="Description of photo" width="230">
        <h1>គណនាពិន្ទុប្រឡងសញ្ញាបត្រមធ្យមសិក្សាបឋមភូមិ 
        <input type="text" placeholder="ភាសាខ្មែរ" id="K">
        <input type="text" placeholder="គណិតវិទ្យា" id="M">
        <input type="text" placeholder="រូបវិទ្យា" id="P">
        <input type="text" placeholder="គីមីវិទ្យា" id="C">
        <input type="text" placeholder="ជីវៈវិទ្យា" id="B">
        <input type="text" placeholder="ប្រវត្តិវិទ្យា" id="H">
                <input type="text" placeholder="ផែនដី និងបរិស្ថានវិទ្យា" id="ES"> 
        <input type="text" placeholder="ភូមិវិទ្យា" id="G">
                <input type="text" placeholder="សីលធម៍ និងពលរដ្ឋវិជ្ជា" id=" Ma">
               <input type="text" placeholder="ភាសាបរទេស" id="E">
        <button type="button" onclick="show_result()">បង្ហាញលទ្ធផល</button>
        <div id="result">
            <h2>ពិន្ទុសរុប :<span id="total"></span></h2>
            <h2>និទ្ទេស :<span id="mention"></span></h2>
            <h2>លទ្ធផល :<span id="final_result"></span></h2>
        </div>
    </div>
    <script src="script.js"></script>
    <body>
        <script type="text/javascript" src="folder/ResuitDexam.js"></script>
    </body>
    <link rel="stylesheet"type="text/css" href="folder/ResuitDExam.css">
</head>
           function show_result() {
    let K = parseFloat(document.getElementById('K').value) || 0;
    let M = parseFloat(document.getElementById('M').value) || 0;
    let P = parseFloat(document.getElementById('P').value) || 0;
    let C = parseFloat(document.getElementById('C').value) || 0;
    let B = parseFloat(document.getElementById('B').value) || 0;
    let H = parseFloat(document.getElementById('H').value) || 0;
    let E = parseFloat(document.getElementById('E').value) || 0;
    let ES = parseFloat(document.getElementById('ES').value) || 0;
    let G = parseFloat(document.getElementById('G').value) || 0;
    let Ma = parseFloat(document.getElementById('Ma').value) || 0;

    let total = K + M + P + C + B + H + (E - 25) + ES + G + Ma ;

    document.getElementById('total').innerText = total;

    let mention;
    if (total >= 416 && total <= 470) {
        mention = 'ល្អ';
    } else if (total >= 338 && total <= 415) {
        mention = 'ល្អបង្គួរ';
    } else if (total >= 260 && total <= 337) {
        mention = 'មធ្យម';
   } else if (total < 259) {
        mention = 'ខ្សោយ';
    }

    document.getElementById('mention').innerText = mention;

    let result = total >= 259 ? 'ជាប់' : 'ធ្លាក់';
    document.getElementById('final_result').innerText = result;
}


   </html>
