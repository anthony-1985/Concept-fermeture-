<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Concept Fermeture</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Montserrat', sans-serif;
      scroll-behavior: smooth;
    }

    /* ----- NAVIGATION ----- */
    nav {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 50px;
      background: rgba(0,0,0,0.5);
      z-index: 10;
      transition: background 0.3s;
    }
    nav.scrolled {
      background: rgba(0,0,0,0.9);
    }
    nav .logo {
      font-size: 1.5rem;
      font-weight: bold;
      text-transform: uppercase;
      color: #c9a646;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 30px;
      margin: 0;
      padding: 0;
    }
    nav ul li a {
      text-decoration: none;
      color: white;
      font-weight: 500;
      transition: 0.3s;
    }
    nav ul li a:hover {
      color: #c9a646;
    }

    /* ----- HERO ----- */
    .hero {
      background: url('https://picsum.photos/1600/900?grayscale') no-repeat center center/cover;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
      color: white;
    }
    .overlay {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.6);
    }
    .content {
      position: relative;
      z-index: 2;
      margin-top: 80px;
    }
    h1 {
      font-size: 3.5rem;
      margin: 0;
      text-transform: uppercase;
      letter-spacing: 3px;
    }
    h2 {
      font-size: 1.5rem;
      font-weight: 300;
      margin: 20px 0 40px 0;
      font-style: italic;
    }
    .buttons {
      display: flex;
      gap: 20px;
      justify-content: center;
    }
    .btn {
      padding: 15px 30px;
      background: #c9a646;
      color: black;
      text-decoration: none;
      border-radius: 5px;
      font-weight: bold;
      transition: 0.3s;
    }
    .btn:hover {
      background: #e0c56d;
      transform: scale(1.05);
    }

    /* ----- SECTIONS ----- */
    section {
      padding: 80px 10%;
      text-align: center;
    }
    section h3 {
      font-size: 2rem;
      color: #c9a646;
      margin-bottom: 20px;
    }
    section p {
      max-width: 800px;
      margin: 0 auto 40px;
      font-size: 1.1rem;
      line-height: 1.6;
      color: #333;
    }

    /* PRODUITS */
    .produits {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }
    .produit {
      background: #f7f7f7;
      border-radius: 8px;
      padding: 20px;
      transition: transform 0.3s;
    }
    .produit img {
      width: 100%;
      border-radius: 8px;
    }
    .produit:hover {
      transform: scale(1.05);
    }

    /* RÉALISATIONS */
    .galerie {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
    }
    .galerie img {
      width: 100%;
      border-radius: 8px;
      transition: 0.3s;
    }
    .galerie img:hover {
      transform: scale(1.05);
    }

    /* CONTACT */
    form {
      max-width: 600px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    input, textarea {
      padding: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
    }
    button {
      padding: 15px;
      background: #c9a646;
      border: none;
      border-radius: 5px;
      color: black;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #e0c56d;
    }

  </style>
</head>
<body>
  <!-- NAVIGATION -->
  <nav id="navbar">
    <div class="logo">Concept Fermeture</div>
    <ul>
      <li><a href="#accueil">Accueil</a></li>
      <li><a href="#about">Qui sommes-nous</a></li>
      <li><a href="#produits">Produits</a></li>
      <li><a href="#realisations">Réalisations</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero" id="accueil">
    <div class="overlay"></div>
    <div class="content">
      <h1>Concept Fermeture</h1>
      <h2>Plus qu’un projet, une relation de confiance</h2>
      <div class="buttons">
        <a href="#realisations" class="btn">Découvrir nos réalisations</a>
        <a href="#contact" class="btn">Demander un devis</a>
      </div>
    </div>
  </section>

  <!-- QUI SOMMES-NOUS -->
  <section id="about">
    <h3>Qui sommes-nous ?</h3>
    <p>Depuis plus de 10 ans, Concept Fermeture accompagne ses clients dans leurs projets de menuiserie extérieure : portails, fenêtres, pergolas, baies vitrées et bien plus. Nous mettons un point d’honneur à offrir un service premium basé sur la qualité, le design et la relation de confiance.</p>
  </section>

  <!-- PRODUITS -->
  <section id="produits">
    <h3>Nos Produits</h3>
    <div class="produits">
      <div class="produit">
        <img src="https://picsum.photos/400/250?random=1" alt="Fenêtres">
        <h4>Fenêtres & Portes</h4>
      </div>
      <div class="produit">
        <img src="https://picsum.photos/400/250?random=2" alt="Portails">
        <h4>Portails & Clôtures</h4>
      </div>
      <div class="produit">
        <img src="https://picsum.photos/400/250?random=3" alt="Pergolas">
        <h4>Pergolas Bioclimatiques</h4>
      </div>
      <div class="produit">
        <img src="https://picsum.photos/400/250?random=4" alt="Baies vitrées">
        <h4>Baies vitrées & Portes-fenêtres</h4>
      </div>
    </div>
  </section>

  <!-- RÉALISATIONS -->
  <section id="realisations">
    <h3>Nos Réalisations</h3>
    <div class="galerie">
      <img src="https://picsum.photos/500/300?random=5" alt="Projet 1">
      <img src="https://picsum.photos/500/300?random=6" alt="Projet 2">
      <img src="https://picsum.photos/500/300?random=7" alt="Projet 3">
      <img src="https://picsum.photos/500/300?random=8" alt="Projet 4">
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h3>Contactez-nous</h3>
    <form>
      <input type="text" placeholder="Nom" required>
      <input type="email" placeholder="Email" required>
      <input type="tel" placeholder="Téléphone" required>
      <textarea rows="5" placeholder="Votre message..."></textarea>
      <button type="submit">Envoyer</button>
    </form>
  </section>

  <script>
    // Effet du menu qui fonce au scroll
    window.addEventListener("scroll", function() {
      const nav = document.getElementById("navbar");
      nav.classList.toggle("scrolled", window.scrollY > 50);
    });
  </script>
</body>
</html>
