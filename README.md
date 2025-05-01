<!DOCTYPE html>
<html>
<head>
    <title>Котики</title>
    <style>
        body {
            font-family: Arial;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            text-align: center;
        }
        .cat {
            border: 1px solid #ddd;
            padding: 15px;
            margin-bottom: 20px;
            border-radius: 5px;
        }
        .cat img {
            width: 100%;
            max-height: 200px;
            object-fit: cover;
        }
        .cat h2 {
            margin-top: 10px;
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <h1>Наши котики</h1>
    
    <div id="cats"></div>

    <script>
        const cats = [
            {
                "name": "Лара",
                "img_link": "https://www.friendforpet.ru/api/sites/default/files/2021-09/167200DD-A44F-4845-8D4D-ACCFC180165A.jpeg",
                "age": 8,
                "description": "Лара – шотландская вислоухая, у нее остеохондродисплазия. Лара спокойная, очень ласковая и контактная."
            },
            {
                "name": "Базиль",
                "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/064AEBCB-45EC-4CE7-AB13-C65F10F00B7B.jpeg",
                "age": 2,
                "description": "Внимательный, активный и ласковый. Любит играть, катать мяч, и мурчать на пледе рядом с людьми!"
            },
            {
                "name": "Риш",
                "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/_DM34706.JPG",
                "age": 1,
                "description": "Риш любит лесенки, канаты. Очень активный и дружелюбный кот."
            }
        ];

        const catsContainer = document.getElementById('cats');
        
        cats.forEach(cat => {
            catsContainer.innerHTML += `
                <div class="cat">
                    <img src="${cat.img_link}" alt="${cat.name}">
                    <h2>${cat.name}, ${cat.age} ${cat.age === 1 ? 'год' : cat.age < 5 ? 'года' : 'лет'}</h2>
                    <p>${cat.description}</p>
                </div>
            `;
        });
    </script>
</body>
</html>
