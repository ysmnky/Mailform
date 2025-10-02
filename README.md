<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<title>Dringende E-Mail senden</title>
<script src="https://cdn.emailjs.com/sdk/3.2/email.min.js"></script>
<script>
   (function(){
       emailjs.init("DEIN_USER_ID"); // hier deine User ID von EmailJS einfügen
   })();

   function sendMail() {
       const templateParams = {
           to_email: "poststelle@auswaertiges-amt.de,johann.wadephul@bundestag.de,poststelle@bk.bund.de,info@ramallah.diplo.de,info@tel-aviv.diplo.de,elefand-hotline@auswaertiges-amt.de,Jacob.Schrot@bk.bund.de",
           subject: "Dringender Appell: Schutz deutscher Staatsbürger nach Festsetzung der Global Sumud Flotilla durch israelische Armee",
           message: `Sehr geehrte Damen und Herren,

wir wenden uns mit größter Dringlichkeit an Sie:

Der deutsche Staatsbürger Hakan Kaya wurde am 2. Oktober 2025 gegen 01:00 Uhr während einer humanitären Hilfsmission in internationalen Gewässern von israelischen Streitkräften gewaltsam festgesetzt und als Geisel genommen.

Herr Kaya war Teil der Global Sumud Flotilla, einer friedlichen, zivilgesellschaftlichen und völkerrechtlich legalen Mission, deren Ziel es ist, humanitäre Hilfsgüter nach Gaza zu bringen und einen humanitären Korridor zu schaffen.

Die Bundesregierung ist verpflichtet, das Leben, die Freiheit und die Würde deutscher Staatsbürger:innen auch im Ausland zu schützen.

Mit Nachdruck und hochachtungsvoll,
Name Nachname`
       };

       emailjs.send("DEIN_SERVICE_ID","DEIN_TEMPLATE_ID", templateParams)
       .then(function(response){
           alert("E-Mail wurde erfolgreich versendet!");
       }, function(error){
           alert("Fehler beim Senden: " + JSON.stringify(error));
       });
   }
</script>
</head>
<body>
<h2>Dringende E-Mail an deutsche Behörden</h2>
<p>Klicke auf den Button, um die Mail an alle Empfänger zu senden:</p>
<button onclick="sendMail()">E-Mail jetzt senden</button>
</body>
</html>
