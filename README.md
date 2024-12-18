<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Solar System Exploration</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background: radial-gradient(circle at center, #000814, #001d3d, #003566);
            color: white;
            overflow-x: hidden;
        }
        header {
            text-align: center;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }
        header h1 {
            font-size: 3rem;
            margin: 0;
        }
        .solar-system {
            margin: 50px auto;
            display: flex;
            flex-direction: column;
            gap: 150px;
            align-items: center;
        }
        .row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            max-width: 800px;
        }
        .row:nth-child(even) {
            flex-direction: row-reverse;
        }
        .celestial-body {
            position: relative;
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background-size: cover;
            background-position: center;
            cursor: pointer;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
            animation: spin 20s linear infinite;
        }
        .celestial-body:hover {
            transform: scale(1.2);
            box-shadow: 0 0 30px rgba(255, 255, 255, 0.8);
            animation-play-state: paused;
        }
        .sun {
            width: 200px;
            height: 200px;
            animation: glow 2s infinite alternate;
        }
        @keyframes spin {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }
        @keyframes glow {
            0% {
                box-shadow: 0 0 30px rgba(255, 200, 0, 0.8);
            }
            100% {
                box-shadow: 0 0 60px rgba(255, 255, 0, 1);
            }
        }
        .info-box {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(0, 0, 0, 0.95);
            color: white;
            padding: 30px;
            border-radius: 15px;
            max-width: 600px;
            text-align: center;
            z-index: 1000;
            box-shadow: 0 0 30px rgba(255, 255, 255, 0.5);
        }
        .info-box h2 {
            margin-top: 0;
            font-size: 2rem;
        }
        .info-box button {
            background: crimson;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 1rem;
            margin-top: 20px;
            cursor: pointer;
        }
        .info-box button:hover {
            background: darkred;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            margin-top: 40px;
        }
        footer p {
            margin: 0;
            font-size: 0.9rem;
        }
        #back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 10px 15px;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            display: none;
        }
        #back-to-top:hover {
            background: rgba(0, 0, 0, 0.9);
        }
    </style>
</head>
<body>
    <header>
        <h1>Solar System Exploration</h1>
    </header>
    <main>
        <div class="solar-system">
            <div class="row">
                <div class="celestial-body sun" style="background-image: url('https://www.flexiprep.com/NCERT-Exercise-Solutions/Science/Class-6/posts/Ch-11-Light-Shadows-And-Reflections-Part-1/luminous-objects.png');" onclick="showInfo('Sun', 'The Sun is the center of our solar system and contains about 99.86% of the mass of the entire solar system. It is a giant ball of hot, glowing gases, primarily hydrogen and helium, undergoing nuclear fusion, which powers the Sun and provides energy to all the planets. The Sun’s surface temperature is around 5,500°C (9,932°F), but its core reaches a scorching 15 million°C (27 million°F). It also produces solar winds, which are streams of charged particles that affect the entire solar system. It accounts for 99.86% of the solar system\'s mass.')"></div>
            </div>
            <div class="row">
    <div class="celestial-body" style="background-image: url('https://www.pngall.com/wp-content/uploads/2/Mercury-Planet-Transparent.png');" onclick="showInfo('Mercury', 'Mercury is the closest planet to the Sun, but it\'s not the hottest! Even though it\'s closer to the Sun than Venus, it lacks a thick atmosphere to trap heat, meaning temperatures on its surface can drop drastically at night.')"></div>
</div>
            <div class="row">
                <div class="celestial-body" style="background-image: url('https://www.nicepng.com/png/full/218-2180092_venus-png.png');" onclick="showInfo('Venus', 'Venus is the hottest planet in our Solar System, with surface temperatures that can reach up to 900°F (475°C). This extreme heat is caused by its thick atmosphere made mostly of carbon dioxide, which traps heat through the greenhouse effect.')"></div>
            </div>
           <div class="row">
    <div class="celestial-body" style="background-image: url('https://th.bing.com/th/id/OIP.BuJsmAGQhAZVy3dSaSYNDAHaHa?w=720&h=720&rs=1&pid=ImgDetMain');" onclick="showInfo('Earth', 'Earth is the only planet known to support life. It has the perfect combination of atmosphere, temperature, and water that supports a wide variety of life forms. Earth is also the only planet where liquid water exists on the surface in large quantities. Earth is the only known planet to have wood, which is a vital resource for many living organisms. Wood comes from trees and is an essential part of Earth\'s ecosystems, providing shelter, oxygen, and nutrients. This unique feature of our planet is one of the many things that make Earth special.')"></div>
</div>
            <div class="row">
                <div class="celestial-body" style="background-image: url('https://www.picng.com/upload/mars_planet/png_mars_planet_6494.png');" onclick="showInfo('Mars', 'Mars is known as the Red Planet because of its reddish appearance, caused by iron oxide, or rust, on its surface. It is also located in the habitable zone of the Sun, meaning it has the potential to support liquid water under the right conditions. Mars has the largest volcano in the solar system, Olympus Mons, and the longest canyon, Valles Marineris, both of which are larger than any feature on Earth.')"></div>
            </div>
            <div class="row">
                <div class="celestial-body" style="background-image: url('https://solarsystem.nasa.gov/system/feature_items/images/16_jupiter_new.png');" onclick="showInfo('Jupiter', 'Jupiter is the largest planet in our solar system, with a diameter of about 142,984 km. It has a massive storm, the Great Red Spot, which has been raging for at least 400 years. Jupiter is primarily made of hydrogen and helium and has a strong magnetic field, making it a gas giant with over 70 moons, including its largest moon, Ganymede, which is the biggest moon in the entire solar system.')"></div>
            </div>
            <div class="row">
                <div class="celestial-body" style="background-image: url('https://www.pngarts.com/files/4/Saturn-Free-PNG-Image.png');" onclick="showInfo('Saturn', 'Saturn is known for its stunning ring system, which is made up of billions of ice particles and rocks. The rings are divided into several sections, and some of them are even thin enough to see through. Saturn is a gas giant, like Jupiter, and is primarily composed of hydrogen and helium. It has more than 80 moons, with Titan being the largest. Titan is unique because it has a thick atmosphere and is the only moon in the solar system known to have liquid lakes and rivers on its surface.')"></div>
            </div>
            <div class="row">
                <div class="celestial-body" style="background-image: url('https://static.vecteezy.com/system/resources/previews/016/778/851/non_2x/planet-galaxy-space-free-png.png');" onclick="showInfo('Uranus', 'Uranus is unique because it rotates on its side, making it the only planet in our solar system that has an extreme tilt of about 98 degrees. This unusual tilt causes its seasons to be much more extreme than those of other planets. Uranus is an ice giant, composed mainly of hydrogen, helium, and water, ammonia, and methane ices. It has a faint ring system and 27 known moons, with Titania being the largest.')"></div>
            </div>
<div class="row">
    <div class="celestial-body" style="background-image: url('https://png.pngtree.com/png-vector/20230918/ourmid/pngtree-beautiful-planet-neptune-png-image_10119972.png');" onclick="showInfo('Neptune', 'Neptune is the farthest planet from the Sun, and is often called the Windiest planet in the solar system, with winds reaching speeds of up to 2,100 km/h (1,300 mph). This ice giant is composed primarily of hydrogen, helium, and water ice, and has a vivid blue color due to methane in its atmosphere. Neptune also has a Great Dark Spot, similar to Jupiter’s Great Red Spot, which is a massive storm system. Neptune has 14 known moons, with Triton being its largest and most intriguing moon, as it has geysers that erupt nitrogen gas into space.')"></div>
</div>
        </div>
    </main>
    <div class="info-box" id="infoBox">
        <h2 id="planetTitle"></h2>
        <p id="planetDescription"></p>
        <button onclick="closeInfo()">Close</button>
    </div>
    <button id="back-to-top" onclick="scrollToTop()">Back to Top</button>
    <footer>
        <p>&copy; 2024 Solar System Exploration. All Rights Reserved.</p>
    </footer>

    <script>
        function showInfo(title, description) {
            document.getElementById('planetTitle').innerText = title;
            document.getElementById('planetDescription').innerText = description;
            document.getElementById('infoBox').style.display = 'block';
        }

        function closeInfo() {
            document.getElementById('infoBox').style.display = 'none';
        }

        window.onscroll = function () {
            const backToTop = document.getElementById('back-to-top');
            if (document.documentElement.scrollTop > 200) {
                backToTop.style.display = 'block';
            } else {
                backToTop.style.display = 'none';
            }
        };

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    </script>
</body>
</html> 


