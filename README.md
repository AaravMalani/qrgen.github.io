#qrgen.github.io
<!DOCTYPE html>
<html lang="en">
<html>
<head>
    <meta name="viewport" content="width=device=width, initial-scale=1.0">
    <title>QR_CODE_GENERATOR</title>
    <link rel="stylesheet" href="QR.css">
</head>
<body>
<div class="container">
    <p>Enter your text or URL</p>
    <input type="text" placeholder="Text or URL" id="qrText">
    <div id="imgBox">
        <img src="![image](https://user-images.githubusercontent.com/94593299/216765497-b80d15ac-1b7d-4a57-b7d9-8d734d789aae.png)
" id="qrImage">
    </div>
    <button onclick="generateQR()">Generate QR Code</button>
</div>
<script>
    let imgBox = document.getElementById("imgBox");
    let qrImage = document.getElementById("qrImage");
    let qrText = document.getElementById("qrText");

function generateQR(){
    if(qrText.value.length > 0){
        qrImage.src = "https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=" + qrText.value;
    imgBox.classList.add("show-img");
    }
    else{
        qrText.classList.add('error');
        setTimeout(()=>{
            qrText.classList.remove('error');
        },1000)
    }
    }
</script>



</body>
</html>
