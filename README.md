# Leno
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>เสือหนังฟรี</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(120deg, #89f7fe, #66a6ff); /* พื้นหลังแบบไล่เฉดสี */
            background-attachment: fixed;
            color: #333;
        }
        header {
            background-color: rgba(0, 120, 215, 0.9);
            color: white;
            padding: 20px;
            text-align: center;
            position: relative;
        }
        header .menu {
            position: absolute;
            top: 20px;
            right: 20px;
        }
        header .menu button {
            background-color: white;
            color: #0078d7;
            border: none;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
        }
        header .menu button:hover {
            background-color: #005bb5;
            color: white;
        }
        .contact-info {
            margin-top: 10px;
            font-size: 14px;
        }
        .container {
            margin: 20px auto;
            max-width: 1200px;
            text-align: center;
        }
        .movie-list {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }
        .movie-card {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 8px;
            width: 200px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        .movie-card img {
            width: 100%;
            border-top-left-radius: 8px;
            border-top-right-radius: 8px;
        }
        .movie-card h3 {
            font-size: 18px;
            margin: 10px 0;
        }
        .movie-card button {
            margin-bottom: 10px;
            padding: 10px;
            background-color: #0078d7;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .movie-card button:hover {
            background-color: #005bb5;
        }
    </style>
</head>
<body>
    <header>
        <h1>เลือกหนังที่คุณต้องการ</h1>
        <p>หนังฟรีชนโรงต้องที่นี่ เสือหนังฟรีสามารถดูได้ทันที</p>
        <p class="contact-info">สามารถติดต่อสอบถามได้ที่ไลน์ @gzodhf123</p>
        <div class="menu">
            <button onclick="alert('เอาไว้หลอกคนโง่')">เมนู</button>
        </div>
    </header>
    <div class="container">
        <div class="movie-list">
            <!-- Loop for 12 movies -->
            <script>
                const movies = [
                    { title: "ธี่หยด 2", image: "https://s.isanook.com/mv/0/ui/34/173699/gal-173699-20240914095416-9ea9a10.jpeg" },
                    { title: "โซนิค 3", image: "https://lh3.googleusercontent.com/oyRKadXnbFaDJyVGWkHvjrHxHVOVLlpoS5Li9jKDkiq3kjFOxBdCawGVIY9SPukqxmTrNSKOUZPIJlOriKMrOJBp0ue4QRWLPw=s0" },
                    { title: "Avenger INFINITY WAY", image: "https://s.isanook.com/mv/0/ud/17/86249/avengersinfinitywar.jpg?ip/resize/w728/q80/jpg" },
                    { title: "โดราเอม่อน เดอะมูฟวี่", image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQu-9I-oYq5ObSIt-YESLBwsM5JypUcSL6jTQ&s" },
                    { title: "คาคุเรนเจอร์ 30ปี", image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7Yg4lJk9VYY91mhPIyme0IOGsPc093U-VhA&s" },
                    { title: "รถทัวร์ วีไอผี", image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQRoEpACbHU_Neb36XROj1sV71q8tYaaPHEGg&s" },
                    { title: "จอมขมังเวทย์", image: "https://favforward.com/app/uploads/2019/11/%E0%B8%AB%E0%B8%99%E0%B8%B1%E0%B8%87%E0%B9%83%E0%B8%AB%E0%B8%A1%E0%B9%88%E0%B8%99%E0%B9%88%E0%B8%B2%E0%B8%94%E0%B8%B9%E0%B9%80%E0%B8%94%E0%B8%B7%E0%B8%AD%E0%B8%99%E0%B8%9E%E0%B8%A4%E0%B8%A8%E0%B8%88%E0%B8%B4%E0%B8%81%E0%B8%B2%E0%B8%A2%E0%B8%99-03.jpg" },
                    { title: "โคตรคนชนเอเลี่ยน", image: "https://s359.kapook.com/rq/500/auto/50/pagebuilder/9309e475-8de6-4f92-b675-340ae4c8cbf6.jpg" },
                    { title: "Spider-Man No Way Homes", image: "https://us-fbcloud.net/wb/data/1422/1422876-img.vnc69k.y2ma.jpg" },
                    { title: "Venom Let Theke Carnage", image: "https://th-images.hellomagazine.com/wp-content/uploads/2021/11/18145317/movie.jpg" },
                    { title: "The OUTPOST", image: "https://cdni-hw.bugaboo.tv/dm/sz-sm/i/images/2023/04/21/pic_the_outpost_1682049520_4460.jpg" },
                    { title: "ปราณี", image: "https://static.thairath.co.th/media/Dtbezn3nNUxytg04ajY6CCMU1rS7vlGobKVG7TarjVmVX2.webp" }
                ];
                movies.forEach((movie) => {
                    document.write(`
                        <div class="movie-card">
                            <img src="${movie.image}" alt="${movie.title}">
                            <h3>${movie.title}</h3>
                            <button onclick="alert('คุณเลือกดู ${movie.title}')">เลือกหนัง</button>
                        </div>
                    `);
                });
            </script>
            
        </div>
    </div>
</body>
</html>
