<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <link href="styles/js-console.css" rel="stylesheet" />
</head>
<body>
    <div id="js-console"></div>
    <script src="script/js-console.js"></script>
    <script>
        var text = "We are <mixcase>living</mixcase> in a <upcase>yellow submarine</upcase>. We <mixcase>don't</mixcase> have <lowcase>anything</lowcase> else."
        var start = 0;
        var end = 0;
        function toUpCase(text) {
            for (start = text.indexOf("<upcase>", 0) ; start < text.length - 1; start = text.indexOf("<upcase>", end)) {
                if (start != -1) {

                    end = text.indexOf("</upcase>", start);
                    var up = text.substring(start + 8, end);
                    var fixed = up.toUpperCase();
                    text = text.replace(up, fixed);
                }
                else {
                    break;
                }
            }
            text.replace("<upcase>", '');
            text.replace("</upcase>", '');

            return text;
        }
        toUpCase(text);

        function toLowCase(text) {
            for (start = text.indexOf("<lowcase>", 0) ; start < text.length - 1; start = text.indexOf("<lowcase>", end)) {
                if (start != -1) {

                    end = text.indexOf("</lowcase>", start);
                    var low = text.substring(start + 9, end);
                    var fixed = low.toLowerCase();
                    text = text.replace(low, fixed);
                }
                else {
                    break;
                }
            }
            text.replace("<lowcase>", "");
            text.replace("</lowcase>", "");

            return text;
        }
        toLowCase(text);

        function toMixCase(text) {
            for (start = text.indexOf("<mixcase>", 0) ; start < text.length - 1; start = text.indexOf("<mixcase>", end)) {
                if (start != -1) {

                    end = text.indexOf("</mixcase>", start);
                    var temp = text.substring(start + 9, (end - start) - 9);
                    var mix = text;
                    for (var i = 0; i < mix.length ; i++) {
                        if (i % 2 == 0) {
                            mix = mix.replace(mix[i], mix[i].toUpperCase())
                        }
                        else {
                            mix = mix.replace(mix[i], mix[i].toLowerCase())
                        }
                    }
                    text.replace(text, mix);
                }
                else {
                    break;
                }
            }
            text.replace("<mixcase>", "");
            text.replace("</mixcase>", "");

            return text;
        }
        toMixCase(text);

        jsConsole.writeLine(text);
    </script>
</body>
</html>
