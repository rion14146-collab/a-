<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <style>
        body { margin: 0; background: #000; overflow: hidden; font-family: sans-serif; }
        main { height: 100vh; overflow-y: scroll; scroll-snap-type: y mandatory; scrollbar-width: none; }
        main::-webkit-scrollbar { display: none; }
        section { height: 100vh; width: 100vw; scroll-snap-align: start; display: flex; justify-content: center; alignItems: center; position: relative; }
        video { width: 100%; height: 100%; object-fit: contain; }
    </style>
</head>
<body>
    <main id="player">
        <section><video src="https://filetoh-b6a9a1cfb5ff.herokuapp.com//dl/91480?code=6f810db865eae4eded5e46d3eaa5ee997e61bca45ef5cee6" loop playsinline></video></section>
        <section><video src="https://filetoh-b6a9a1cfb5ff.herokuapp.com//dl/91457?code=73292da25cbc9c39eb456ea58f113fef3e35ba2bf964dd90" loop playsinline></video></section>
        <section><video src="https://filetoh-b6a9a1cfb5ff.herokuapp.com//dl/91481?code=f1730ab759862776ab48443754a8db2c2cbb369430b03523" loop playsinline></video></section>
        <section><video src="https://filetoh-b6a9a1cfb5ff.herokuapp.com//dl/91482?code=ed48a437accca96d31b589df4aa7b22229707f4211240c04" loop playsinline></video></section>
    </main>

    <script>
        const videos = document.querySelectorAll('video');
        
        // التشغيل عند الظهور (تيك توك)
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.play();
                else { entry.target.pause(); entry.target.currentTime = 0; }
            });
        }, { threshold: 0.6 });

        videos.forEach(v => {
            observer.observe(v);
            // تسريع 2x عند الضغط المطول
            v.onpointerdown = () => v.playbackRate = 2;
            v.onpointerup = () => v.playbackRate = 1;
        });
    </script>
</body>
</html>
