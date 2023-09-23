# Tugas1-Grafkom-C

Tujuan: Menggambar tiga huruf pertama dari namamu dengan menggunakan WebGL.

Instruksi:

Menggambar dengan gl.LINES:

Ambil tiga huruf pertama dari namamu. Sebagai contoh, jika namamu "HADZIQ", maka yang akan digambar adalah huruf "HAD".
Gunakan primitif gl.LINES untuk menggambar ketiga huruf tersebut.
Pilihlah warna favoritmu untuk garis-garis yang membentuk huruf. Sebagai contoh, jika warna favoritmu adalah Fuchsia, kode warnanya adalah #FF00FF.
Pastikan warna latar belakang kanvas adalah hitam pekat (#000000).

Menggambar dengan gl.TRIANGLES:

Setelah tiga detik, bersihkan kanvas.
Ubah warna latar belakang kanvas menjadi warna favoritmu.
Gambar kembali tiga huruf pertama dari namamu, tetapi kali ini gunakan primitif gl.TRIANGLES.
Pilihlah warna yang kontras atau komplementer dengan warna favoritmu untuk huruf-huruf ini. Sebagai contoh, warna yang kontras dengan Fuchsia adalah Green dengan kode #00FF00.
Pastikan untuk memeriksa kesesuaian warna yang Anda pilih agar hasil gambar dapat dilihat dengan jelas dan estetik.
Usahakan agar bentuk huruf tetap estetik meskipun menggunakan gl.TRIANGLES.

Animasi:

Setelah tiga detik, ulangi langkah pertama dan seterusnya, sehingga Anda mendapatkan animasi yang bergantian antara gl.LINES dan gl.TRIANGLES.

-----------------------------------------------------------------------------------------------
Jawaban:

Dalam pengerjaannya saya banyak bertanya memalui chatGPT dan ini adalah beberapa detail mengenai pertanyaan saya dengan chatGPT.

- give me a html canvas code to accomplish tjis task Drawing with gl.LINES:

Take the first three letters of your name. For instance, if your name is "NAJMA," you should draw the letters "NAJ."
Use the gl.LINES primitive to illustrate these three letters.
Choose your favorite color for the lines forming the letters. For example, if your favorite color is Fuchsia, its color code is #FF00FF.
Ensure the canvas background color is pitch black (#000000)


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canvas Drawing</title>
</head>
<body style="margin: 0; overflow: hidden;">
    <canvas id="myCanvas" width="800" height="400"></canvas>

    <script>
        // Get a reference to the canvas element and its 2d context
        const canvas = document.getElementById('myCanvas');
        const context = canvas.getContext('2d');

        // Set the background color to pitch black (#000000)
        context.fillStyle = '#000000';
        context.fillRect(0, 0, canvas.width, canvas.height);

        // Set your favorite color for the lines (Fuchsia: #FF00FF)
        context.strokeStyle = '#FF00FF';
        context.lineWidth = 5; // Adjust line width as needed

        // Define the positions of the lines to form the letters "NAJ"
        const lines = [
            // Letter "N"
            { x1: 100, y1: 100, x2: 100, y2: 200 },
            { x1: 100, y1: 200, x2: 150, y2: 100 },
            { x1: 150, y1: 100, x2: 150, y2: 200 },

            // Letter "A"
            { x1: 200, y1: 100, x2: 220, y2: 200 },
            { x1: 220, y1: 200, x2: 240, y2: 100 },
            { x1: 210, y1: 150, x2: 230, y2: 150 },

            // Letter "J"
            { x1: 270, y1: 100, x2: 270, y2: 200 },
            { x1: 270, y1: 200, x2: 320, y2: 200 },
            { x1: 320, y1: 200, x2: 320, y2: 150 },
        ];

        // Draw the lines using the gl.LINES primitive
        for (const line of lines) {
            context.beginPath();
            context.moveTo(line.x1, line.y1);
            context.lineTo(line.x2, line.y2);
            context.stroke();
        }
    </script>
</body>
</html>
```

Karena huruf yang dihasilkan dari kode diatas terbalik, maka saya mengganti beberapa korrdinat pada huruf tersebut. menjadi :

            // Letter "N"
            { x1: 100, y1: 100, x2: 100, y2: 200 },
            { x1: 100, y1: 200, x2: 150, y2: 100 },
            { x1: 150, y1: 100, x2: 150, y2: 200 },

            // Letter "A"
            { x1: 200, y1: 100, x2: 220, y2: 200 },
            { x1: 220, y1: 200, x2: 240, y2: 100 },
            { x1: 210, y1: 150, x2: 230, y2: 150 },

            // Letter "J"
            { x1: 270, y1: 100, x2: 270, y2: 200 },
            { x1: 270, y1: 200, x2: 320, y2: 200 },
            { x1: 320, y1: 200, x2: 320, y2: 150 },
        ];



