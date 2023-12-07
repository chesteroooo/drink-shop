<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>飲料店菜單</title>
    <!-- Include jQuery -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #F3EEEA; /* Light beige background */
        }

        header {
            background-color: #333;
            color: white;
            padding: 1em;
            text-align: center;
        }

        section {
            padding: 20px;
            background-color: #EBE3D5; /* Light gray background for sections */
        }

        .menu-item {
            border-bottom: 1px solid #ddd;
            padding: 10px 0;
            display: flex;
            justify-content: space-between;
            cursor: pointer; /* Add cursor pointer to indicate interactivity */
            background-color: #fff; /* White background for menu items */
            color: #333; /* Dark gray text color */
            transition: background-color 0.3s, color 0.3s, box-shadow 0.3s; /* Smooth transition effect */
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Subtle box shadow */
        }

        .menu-item:hover {
            background-color: #B0A695; /* Light brown color on hover */
            color: #333; /* Dark gray text color on hover */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Slightly larger box shadow on hover */
        }


    </style>
    <script>
        // jQuery code
        $(document).ready(function () {
            // Add a simple fade effect on menu items
            $('.menu-item').hover(function () {
                $(this).fadeTo('fast', 0.7);
            }, function () {
                $(this).fadeTo('fast', 1);
            });
        });
    </script>
</head>

<body>

    <header>
        <h1>妖洞八茶鋪</h1>
        <p>讓你找回最初的感動</p>
    </header>

    <section>
        <h2>菜單</h2>

        
        <div class="menu-item">
            <span>珍珠奶茶</span>
            <span>NT$50</span>
        </div>

        <div class="menu-item">
            <span>多多綠</span>
            <span>NT$45</span>
        </div>

        <div class="menu-item">
            <span>極品水果茶</span>
            <span>NT$55</span>
        </div>

        <div class="menu-item">
            <span>貴妃荔枝紅茶</span>
            <span>NT$40</span>
        </div>

        <div class="menu-item">
            <span>琥珀烏龍茶</span>
            <span>NT$45</span>
        </div>

        <div class="menu-item">
            <span>阿里山奶茶</span>
            <span>NT$50</span>
        </div>

        <div class="menu-item">
            <span>金桔檸檬</span>
            <span>NT$40</span>
        </div>

        <div class="menu-item">
            <span>哈尼檸檬</span>
            <span>NT$45</span>
        </div>

        <div class="menu-item">
            <span>冬瓜內內</span>
            <span>NT$35</span>
        </div>




    </section>

    <section>
        

        <h2>飲料圖片</h2>
        <img src="https://www.sunnysyrup.com/proimages/recipe/03Milk_Tea/01%20Tapioca%20Pearl%20Milk%20Tea.jpg" alt="珍珠奶茶" style="width: 100px; height: 100px;">
        <img src="https://www.woo-oh.com/archive/image/edcontent3/yufruit3.jpg" alt="多多綠" style="width: 100px; height: 100px;">
        <img src="https://www.sweet-dumpling.com/media/content/6eb5de29eeb6fa0fc1cfe686a25f3252/taiwanese-style-iced-fruit-tea-cover.jpg" alt="極品水果茶" style="width: 100px; height: 100px;">
        <img src="https://www.sunnysyrup.com/proimages/pb/products/04Tea/03/03-5/Lychee-Black-Tea-(Extract)-2.jpg" alt="貴妃荔枝紅茶" style="width: 100px; height: 100px;">
        <img src="https://d5ttlem47o98b.cloudfront.net/s3fs-public/styles/banner/public/news_cover/1589710273_u3.jpg?itok=9LeEWDy4" alt="琥珀烏龍茶" style="width: 100px; height: 100px;">
        <img src="https://www.dicos.com.tw/upload/products/2021122812294163u8c.jpg" alt="阿里山奶茶" style="width: 100px; height: 100px;">
        <img src="https://marketbuy.cto.moea.gov.tw/assets/uploads/600x600/%EF%BC%92_20220507110404989606.jpg" alt="金桔檸檬" style="width: 100px; height: 100px;">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRdxMD_DdgRG496Lw9WBk8VnJPm7BYIMspOog&usqp=CAU" alt="哈尼檸檬" style="width: 100px; height: 100px;">
        <img src="https://tb-static.uber.com/prod/image-proc/processed_images/c511cf0f499446a610389aa0e69dcaab/4218ca1d09174218364162cd0b1a8cc1.jpeg" alt="冬瓜內內" style="width: 100px; height: 100px;">
        

    </section>

    <section id="introduction">
        <h2>飲料介紹</h2>
        <p id="drinkIntroduction">請選擇一款飲料查看介紹。</p>
    </section>

    <script>
        // jQuery code
        $(document).ready(function () {
            // Add a simple fade effect on menu items
            $('.menu-item').hover(function () {
                $(this).fadeTo('fast', 0.7);
            }, function () {
                $(this).fadeTo('fast', 1);
            });

            // Handle click event on menu items
            $('.menu-item').click(function () {
                // Get the text of the clicked menu item
                var drinkName = $(this).find('span:first').text();

                // Display introduction based on the clicked menu item
                displayIntroduction(drinkName);
            });

            // Function to display introduction based on the selected drink
            function displayIntroduction(drinkName) {
                var introduction = getDrinkIntroduction(drinkName);
                $('#drinkIntroduction').text(introduction);
            }

            // Function to get the introduction based on the selected drink
            function getDrinkIntroduction(drinkName) {
                // Add your drink introductions here
                switch (drinkName) {
                    case '珍珠奶茶':
                        return '珍珠奶茶是一種受歡迎的台灣飲料，特色是搭配Q彈的珍珠和香濃的奶茶。';
                    case '多多綠':
                        return '多多綠是一款清新的綠茶飲料，搭配豐富的多多果肉，是夏日消暑的好選擇。';
                    case '極品水果茶':
                    return '極品水果茶以新鮮水果製作而成，口感清爽，綜合多種水果的風味，是果迷的最愛。';
                    case '貴妃荔枝紅茶':
                        return '貴妃荔枝紅茶是一種充滿芳香的茶飲，荔枝的甜美與紅茶的香氣完美結合。';
                    case '琥珀烏龍茶':
                        return '琥珀烏龍茶具有獨特的烏龍香氣，口感滑順，是喜愛烏龍茶的人士的首選。';
                    case '阿里山奶茶':
                        return '阿里山奶茶以高山茶葉製成，搭配濃郁的奶香，是一種帶有山林風味的茶飲。';
                    case '金桔檸檬':
                        return '金桔檸檬是一款清新酸爽的檸檬飲料，加入金桔的風味，更顯獨特。';
                    case '哈尼檸檬':
                        return '哈尼檸檬是以哈密瓜和檸檬製作而成的飲料，結合了兩種水果的風味，清新怡人。';
                    case '冬瓜內內':
                        return '冬瓜內內是一種利用冬瓜製成的甜品飲料，清涼解渴，適合喜歡清淡口味的人士。';

                    default:
                        return '暫無介紹。';
                }
            }
        });
    </script>

</body>

</html>
