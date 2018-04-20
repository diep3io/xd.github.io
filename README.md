<!doctype html>
<html lang="en" id="mainBody">
<head>
    <!-- Meta Properties -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=no">
    <title>xd.io</title>
    <!-- CSS -->
    <link href="https://fonts.googleapis.com/css?family=Ubuntu:400,700" rel="stylesheet"> 
    <link rel="stylesheet" href="css/main.css" />
    <!-- Version Control -
    <script>
        var VERSION = localStorage.getItem('versionHash');
        (function versionControl() {
            let request = new XMLHttpRequest();
            let url = window.location.href + "/api/vhash";
            console.log("Checking version...");
            return new Promise((resolve, reject) => {
                request.open('GET', url);
                request.onload = () => { resolve(request.response); console.log('Version check successful.'); };
                request.onerror = () => { reject(request.statusText); console.log('Version check failed.'); console.log(request.statusText); };
                request.send();
            });
        })().then(function resolveVersion(data) {
            localStorage.setItem('versionHash', data);
            if (VERSION !== data) {
                console.log("Updating!");   
                localStorage.setItem('updated', 'datgudshit');
                location.reload(true);
            }
        });
    </script>
    -->
    <!-- Favicons -->
    <link rel="apple-touch-icon" sizes="57x57" href="/favicons/apple-icon-57x57.png">
    <link rel="apple-touch-icon" sizes="60x60" href="/favicons/apple-icon-60x60.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/favicons/apple-icon-72x72.png">
    <link rel="apple-touch-icon" sizes="76x76" href="/favicons/apple-icon-76x76.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/favicons/apple-icon-114x114.png">
    <link rel="apple-touch-icon" sizes="120x120" href="/favicons/apple-icon-120x120.png">
    <link rel="apple-touch-icon" sizes="144x144" href="/favicons/apple-icon-144x144.png">
    <link rel="apple-touch-icon" sizes="152x152" href="/favicons/apple-icon-152x152.png">
    <link rel="apple-touch-icon" sizes="180x180" href="/favicons/apple-icon-180x180.png">
    <link rel="icon" type="image/png" sizes="192x192"  href="/favicons/android-icon-192x192.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicons/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="96x96" href="/favicons/favicon-96x96.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicons/favicon-16x16.png">
    <link rel="manifest" href="/favicons/manifest.json">
    <meta name="msapplication-TileColor" content="#ffffff">
    <meta name="msapplication-TileImage" content="/favicons/ms-icon-144x144.png">
    <meta name="theme-color" content="#ffffff">
</head>
<body oncontextmenu="return false;" id="mainBody">
    <div id="gameAreaWrapper">
        <canvas id="gameCanvas" tabindex="1" id="cvs" tabindex="1"></canvas>
    </div>
    <div id="mainWrapper">
        <div id="startMenuWrapper">
            <div id="startMenu">
                <div id="twitterHolder" class="startMenuHolder" style="height:100%">
                    <a class="twitter-timeline" data-width="350" data-height="295" data-theme="light" data-link-color="#B9E87E" href="https://twitter.com/arras_dev?ref_src=twsrc%5Etfw">Tweets by arras_dev</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
                </div>
                <div class="startMenuHolder">
                    <div class="sliderHolder">
                        <div class="slider" id="startMenuSlidingContent">
                            <center><img src="/favicons/favicon-96x96.png" /></center>
                            <h1>xd.io</h1>
                            <div id="serverName"><h4 class="nopadding">Connecting...</h4></div>
                            <input type="text" autofocus tabindex="1" spellcheck="false" placeholder="This is the tale of:" id="playerNameInput" maxlength="28" />
                        </div>
                        <div class="slider" id="startMenuSlidingTrigger"><h3 class="nopadding"><span id="viewOptionText">view options</span>&nbsp;&nbsp;<i class="arrow" id="optionArrow" style="transform:rotate(-45deg);-webkit-transform:rotate(-45deg)"></i></h3></div>
                        <div class="slider" id="startMenuSlidingContent"> 
                            <br>
                            <optionsHeader>Advanced Controls:</optionsHeader><br>
                            <table>
                                <tr>
                                    <td><b>E</b>: auto-fire</td>
                                    <td><b>D</b>: auto-spin</td>
                                </tr>
                                <tr>
                                    <td><b>R</b>: disable auto-weapons</td>
                                    <td><b>N</b>: level up (sandbox)</td>
                                </tr>
                                <tr>
                                    <td><b>B</b>: reverse mouse buttons</td>
                                    <td><b>V</b>: reverse tank</td>
                                </tr>
                            </table>
                            <optionsHeader>Options:</optionsHeader>
                            <select id="optColors" tabindex="-1">
                                <option value="normal">Light Colors</option>
                                <option value="dark">Dark Colors</option>
                                <option value="natural">Natural</option>
                                <option value="classic">Classic</option>
                                <option value="forest">Forest (Fan-made)</option>
                                <option value="midnight">Midnight (Fan-made)</option>
                                <option value="pastel">Snow (Fan-made)</option>
                                <option value="ocean">Coral Reef (Fan-made)</option>
                                <option value="badlands">Badlands (Fan-made)</option>
                                <option value="bleach">Bleach (Fan-made)</option>
                            </select>
                            <select id="optBorders" tabindex="-1">
                                <option value="normal">Soft Borders</option>
                                <option value="dark">Dark Borders</option>
                                <option value="neon">Neon Mode</option>
                                <option value="glass">Glass Mode</option>
                            </select>
                            <table>
                                <tr>
                                    <td><div>
                                        <label class="container"><input id="optScreenshotMode" tabindex="-1" class="checkbox" type="checkbox"><span class="checkmark"></span>Screenshot Mode</label>
                                    </div></td>
                                    <td><div>
                                        <label class="container"><input id="optNoPointy" tabindex="-1" class="checkbox" type="checkbox"><span class="checkmark"></span>Classic Traps</label>
                                    </div></td>
                                </tr><tr>
                                    <td><div>
                                        <label class="container"><input id="optFancy" tabindex="-1" class="checkbox" type="checkbox"><span class="checkmark"></span>Low Graphics</label>
                                    </div></td>
                                    <td><div>
                                        <label class="container"><input id="optPredictive" tabindex="-1" class="checkbox" type="checkbox"><span class="checkmark"></span>Disable Hyperactivity</label>
                                    </div></td>
                                </tr><tr>
                                </tr>
                            </table>
                        </div>    
                   
                    <div style="position: relative; bottom: -10px;">
                        <button id="startButton" tabindex="2">Play</button>
                    </div>
                </div>          
                <div class="startMenuHolder" allowtransparency="false">
                    <iframe id="patchNotesIFrame" src="changelog.html" seamless='seamless' frameBorder="0">Patch notes go here!</iframe>
                </div>
                <div id="bottomHolder">
                    <a style="background:#7289DB" href="http://discord.gg/J5h8Hfe">Discord</a>     
                    <a style="background:#E0D571" href="https://discord.gg/k8ZFMUz">Dev Discord</a>
                    <a style="background:#F74501" href="https://www.reddit.com/r/Diep2io/">Reddit</a>
                    <a style="background:#9974E8;float:right" href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=YJ42X4KU6ETPA">Paypal</a>   
                    <a style="background:#E27061;float:right" href="https://www.patreon.com/diep2dev">Patreon</a>
                    <h5 class="nopadding" style="margin:9px;float:right;display:inline">Donate to the original developer:</h5>
                </div>  
            </div>
        </div>
    </div>
    <!-- JS -->
    <script>
    (function() {
        if (window !== window.top || window.location.hostname !== "arras.surge.sh") {
            try {
                window.top.location = "http://http://diep3io.github.io/xd.github.io"
            } catch(e) {
                document.body.addEventListener('click', function() {
                    window.top.location = "http://diep3io.github.io/xd.github.io"
                })
            }
        } else {
            var gameScript = document.createElement('script')
            gameScript.src = "/bundle.js"
            document.body.appendChild(gameScript)
        }
        var clicked = 0
        var trigger = document.getElementById("startMenuSlidingTrigger")
        var optionArrow = document.getElementById("optionArrow")
        var viewOptionText = document.getElementById("viewOptionText")
        var sliders = document.getElementsByClassName("slider")
        trigger.onclick = function() {
            clicked = 1 - clicked
            optionArrow.style.transform = optionArrow.style.webkitTransform = clicked ? 'rotate(45deg)' : 'rotate(-45deg)'
            viewOptionText.innerText = clicked ? 'close options' : 'view options'
            for (var i = 0; i < sliders.length; i++)
                sliders[i].style.top = clicked ? '-225px' : '0'
            sliders[0].style.opacity = 1 - clicked
            sliders[2].style.opacity = clicked
        }
        window.onerror = function(message, source, lineno, colno, error) {
            window.onerror = null
            if (error) error = error.toString()
            console.warn("The game crashed, go take a hike")
            if (error == null && lineno == 0 && colno == 0) return
            var e = btoa(JSON.stringify({
                message: message,
                source: source,
                lineno: lineno,
                colno: colno,
                error: error
            }))
            console.log("Uncaught error, base 64 dump below")
            console.log(e)
            console.log("Uncaught error, base 64 dump above")
            /*var xhr = new XMLHttpRequest();
            xhr.open("POST", "//", true);
            xhr.send(e);*/
        }
    })()
    </script>
</body>
</html>


