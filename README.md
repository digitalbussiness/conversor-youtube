<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Baixar Vídeo do YouTube</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
      margin: 0;
      padding: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
    }
    .container {
      background: #fff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      width: 100%;
      max-width: 500px;
      margin: 20px;
      text-align: center;
    }
    h1 {
      font-size: 1.8rem;
      margin-bottom: 10px;
    }
    p {
      font-size: 1rem;
      margin-bottom: 20px;
    }
    input, select, button {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
    }
    button {
      background-color: #28a745;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    button:hover {
      background-color: #218838;
    }
    iframe {
      margin-top: 20px;
      width: 100%;
      height: 300px;
      border: none;
    }
    .ads {
      margin: 20px 0;
    }
    .compartilhar {
      margin-top: 20px;
    }
    .compartilhar button {
      background-color: #25D366;
      border: none;
    }
    @media screen and (max-width: 480px) {
      h1 {
        font-size: 1.4rem;
      }
      p, input, select, button {
        font-size: 0.95rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🎵 Conversor YouTube para MP3/MP4 🎥</h1>
    <p>Cole o link do vídeo e baixe grátis!</p>

    <div class="ads">
      <!-- Aqui vai o bloco de anúncio -->
      <ins class="adsbygoogle"
           style="display:block"
           data-ad-client="ca-pub-XXXXXXXXXXXXXXX"
           data-ad-slot="1234567890"
           data-ad-format="auto"
           data-full-width-responsive="true"></ins>
      <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
      <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
    </div>

    <input id="url" type="text" placeholder="Cole o link do YouTube aqui">
    <select id="formato">
      <option value="mp3">MP3 (Áudio)</option>
      <option value="mp4">MP4 (Vídeo)</option>
    </select>
    <button onclick="baixar()">Converter e Baixar</button>

    <div id="resultado"></div>

    <div class="compartilhar">
      <button onclick="compartilhar()">📲 Compartilhar no WhatsApp</button>
    </div>
  </div>

  <script>
    function baixar() {
      const url = document.getElementById('url').value;
      const formato = document.getElementById('formato').value;
      const apiURL = `https://api.vevioz.com/api/button/${formato}?url=${encodeURIComponent(url)}`;
      document.getElementById('resultado').innerHTML = `<iframe src="${apiURL}"></iframe>`;
    }

    function compartilhar() {
      const siteURL = window.location.href;
      const texto = encodeURIComponent("Olha esse site pra baixar vídeos do YouTube: " + siteURL);
      const link = `https://wa.me/?text=${texto}`;
      window.open(link, '_blank');
    }
  </script>
</body>
</html>

