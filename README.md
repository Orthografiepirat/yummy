# Progressive Web Apps - Complete Guide
This source code is part of Maximilian Schwarzmüller's "Progressive Web Apps - Complete Guide" course on udemy.com.

# How to Use
You need [Node.js](https://nodejs.org) installed on your machine. Simply download the installer from [nodejs.org](https://nodejs.org) and go through the installation steps.

Once Node.js is installed, open your command prompt or terminal and **navigate into this project folder**. There, run `npm install` to install all required dependencies.

Finally, run `npm start` to start the development server and visit [localhost:8080](http://localhost:8080) to see the running application.


# App Manifest
- ermöglicht es die PWA zu installieren (z. B. Icon auf Smartphone speichern)
- datei die im root folder angelegt wird (hier public), der Name sollte 'manifest.json' sein
    - properties sind:
    - name -> Name der App, erscheint z. B. auf Splashscreen)
    - short_name -> Kurzname z. B. unter Icon -> immer wenn begrenzter Platz
    - start_url -> Seite die beim Startup geladen wird, bei Icon-Start auf Smartphone
    - scope -> "." heißt alle Folder werden inkludiert, falls was exkludiert wird, dann werden die Werte auf Manifest.json nicht dafür verwendet
    - display -> Wie die App angezeigt werden soll, z. B. standalone verbirgt browserpfeile und adresszeile etc.
    - background_color -> auf Splashscreen und Ladeanzeigen
    - theme_color -> Farbe der Toolbar/taskbar
    - description -> wird z. B. angezeigt in Browserfavoriten
    - dir -> ltr/rtl
    - lang -> standardsprache (de-de)
    - orientation -> default orientation oder zwangsorientierung
    - icons -> Array mit Iconsets, wobei das beste passende gewählt wird z. B. via "sizes": 96x96 ... 48x48 / 128 / 512
    - related_applications -> array, z. B. falls Nativeapp vorhanden
- wird via neuer link in jeder html datei hinterlegt   <link rel="manifest" href="/manifest.json">