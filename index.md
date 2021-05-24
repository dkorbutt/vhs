<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VHS</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="shortcut icon" href="fav.png" type="image/x-icon">
    <link href="https://fonts.googleapis.com/css2?family=Nunito&display=swap" rel="stylesheet">
</head>
<body>
    <div id="burger">
        <div class="bg-pas" id="bg1"></div>
        <div class="bg-pas" id="bg2"></div>
        <div class="bg-pas" id="bg3"></div>
    </div>
    <div id="burgerbar">
        <div id="bars">
            <div class="bar" id="bg-bar1">HOME</div>
            <div class="bar" id="bg-bar2">SAMPLE TEXT</div>
            <div class="bar" id="bg-bar3">SAMPLE TEXT</div>
            <div class="bar" id="bg-bar4">VHS</div>
        </div>
        <div id="burgerfooter">
            <ul>
                <li>
                    <svg width="24" height="15" viewBox="0 0 24 24"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/></svg>
                </li>
                <li>
                    dkorbutt
                </li>
            </ul>
            
        </div>
    </div>
    <div id="main">
        <div id="napis" class="show" data-text="vhs">vhs</div>
        <div id="vhs" class="hidden">
            <img src="vhs.gif" alt="">
        </div>
    </div>
    
    <script>
        var button = document.getElementById("burger");
        var slider = document.getElementById("burgerbar");
        var paski = document.getElementsByClassName("bg-pas");
        var main = document.getElementById("main");
        var vhs = document.getElementById("bg-bar4");
        var napis = document.getElementById("napis");
        var home = document.getElementById("bg-bar1");

        button.addEventListener("click", () => {
            slider.classList.toggle("bg-active");
            button.classList.toggle("change");
            main.classList.toggle("move");

            if(slider.classList.contains("bg-active")) {
            main.addEventListener("click", ()=> {
                slider.classList.remove("bg-active");
                main.classList.remove("move");
                button.classList.remove("change");
            })
        }
            
        })

        vhs.addEventListener("click", ()=> {
            napis.classList.remove("show");
            napis.classList.add("hidden");
            document.getElementById("vhs").classList.add("show");
            document.getElementById("vhs").classList.remove("hidden");

        })

        home.addEventListener("click", ()=> {
            napis.classList.add("show");
            napis.classList.remove("hidden");
            document.getElementById("vhs").classList.remove("show");
            document.getElementById("vhs").classList.add("hidden");
        })
        
    </script>
</body>
</html>