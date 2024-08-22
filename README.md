<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>❤N❤</title>
    <link rel="stylesheet" href="styles.css">
</head>

<audio controls src="dontstayaway.mp3"></audio>
<body align="center" >

<div class="image-container">
    <img id="qualityImage"  alt="Địa C" style="color: aliceblue;">
</div>
<h1></h1>
<select id="qualitySelect" onchange="changeImage()">
    <option></option>       
    <option value="144p">144p</option>
    <option value="240p">240p</option>
    <option value="480p">480p</option>
    <option value="720p">720p</option>
    <option value="1080p">1080p</option>
    
</div>

<script src="script.js"></script>

</body>
</html>
body {
    background-color: black;
    
}

.container {
    text-align: center;
    background: #1e1e1e; /* Nền container màu xám tối */
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

h1 {
    color: #fff; /* Chữ màu trắng */
    margin-bottom: 20px;
}

select {
    padding: 10px;
    font-size: 16px;
    margin-bottom: 20px;
    background-color: #333; /* Nền select màu xám đậm */
    color: #fff; /* Chữ màu trắng */
    border: 1px solid #444; /* Viền select màu xám nhạt */
    border-radius: 4px;
}

.image-container {
    margin-top: 20px;
}

img {
    max-width: 100%;
    height: auto;
    border: 1px solid #444; /* Viền ảnh màu xám nhạt */
    border-radius: 4px;}
 function changeImage() {
    const qualitySelect = document.getElementById('qualitySelect');
    const qualityImage = document.getElementById('qualityImage');
    const selectedQuality = qualitySelect.value;

    // Mapping between quality and image file name
    const qualityImageMap = {
        '144p': 'images/144p (1).png',
        '240p': 'images/240p.png',
        '480p': 'images/480p.png',
        '720p': 'images/720p.png',
        '1080p': 'images/1080p.png'
    };

    // Change image source based on selected quality
    qualityImage.src = qualityImageMap[selectedQuality];
}
