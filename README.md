<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Brice - Ressources et Formations pour les Professionnels du Digital</title>
  <meta name="description" content="Ressources, formations et outils digitaux pour booster votre productivité et vos compétences numériques.">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" />
  <style>
    /* Reset simple */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f4f7fa;
      color: #333;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background-color: #0066b2;
      color: white;
      padding: 12px 40px;
      box-shadow: 0 3px 6px rgba(0,0,0,0.1);
    }

    .header-container {
      max-width: 1400px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      display: flex;
      align-items: center;
      font-size: 1.8rem;
      font-weight: 700;
      text-decoration: none;
      color: white;
    }

    .logo-icon {
      margin-right: 10px;
      font-size: 2rem;
    }

    .nav-container {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    nav {
      display: flex;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 25px;
      font-weight: 600;
      transition: color 0.2s ease;
      padding: 8px 0;
    }

    nav a:hover {
      color: #b3d9ff;
    }

    /* Hero section */
    .hero {
      background: linear-gradient(135deg, #004d8c 0%, #0066b2 100%);
      color: white;
      padding: 60px 40px;
      text-align: center;
    }

    .hero-container {
      max-width: 1000px;
      margin: 0 auto;
    }

    .hero h1 {
      font-size: 2.8rem;
      margin-bottom: 20px;
      line-height: 1.2;
    }

    .hero p {
      font-size: 1.2rem;
      max-width: 700px;
      margin: 0 auto 30px;
      line-height: 1.6;
      opacity: 0.9;
    }

    .hero-buttons {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      margin-top: 30px;
      flex-wrap: wrap;
    }

    .hero-buttons .btn,
    .hero-buttons .btn-secondary {
      background: white;
      color: #0066b2;
      border: none;
      border-radius: 30px;
      padding: 14px 32px;
      font-size: 1.1rem;
      font-weight: 700;
      box-shadow: 0 4px 16px rgba(0,102,178,0.10);
      transition: background 0.2s, color 0.2s, transform 0.2s, box-shadow 0.2s;
      cursor: pointer;
      margin: 0;
      outline: none;
      display: inline-block;
      text-decoration: none;
    }

    .hero-buttons .btn:hover,
    .hero-buttons .btn-secondary:hover {
      background: #3d9bff;
      color: #fff;
      transform: translateY(-2px) scale(1.04);
      box-shadow: 0 8px 24px rgba(0,102,178,0.18);
    }

    .hero-buttons .btn-secondary {
      border: 2px solid #0066b2;
      background: white;
      color: #0066b2;
    }

    .hero-buttons .btn-secondary:hover {
      background: #0066b2;
      color: #fff;
      border-color: #3d9bff;
    }

    .search-container {
      display: flex;
      margin: 30px auto;
      max-width: 800px;
    }

    .search-bar {
      width: 100%;
      padding: 12px 20px;
      border: 2px solid #ddd;
      border-radius: 30px;
      font-size: 1rem;
      outline: none;
      transition: all 0.3s ease;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }

    .search-bar:focus {
      border-color: #0066b2;
      box-shadow: 0 2px 15px rgba(0,102,178,0.1);
    }

    /* Section intro */
    .section-intro {
      text-align: center;
      margin-bottom: 40px;
    }

    .section-intro h2 {
      font-size: 2rem;
      color: #004d8c;
      margin-bottom: 15px;
    }

    .section-intro p {
      max-width: 800px;
      margin: 0 auto;
      color: #555;
      line-height: 1.6;
      font-size: 1.1rem;
    }

    .category-filter {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 30px;
      gap: 10px;
    }

    .filter-btn {
      padding: 8px 15px;
      background-color: white;
      border: 1px solid #ddd;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 500;
      transition: all 0.2s ease;
    }

    .filter-btn:hover {
      background-color: #f0f7ff;
      border-color: #0066b2;
    }

    .filter-btn.active {
      background-color: #0066b2;
      color: white;
      border-color: #0066b2;
    }

    main {
      flex-grow: 1;
      padding: 30px 20px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .grid-products {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 25px;
    }

    @media (max-width: 1200px) {
      .grid-products {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    @media (max-width: 900px) {
      .grid-products {
        grid-template-columns: repeat(2, 1fr);
      }
      
      .hero h1 {
        font-size: 2.2rem;
      }
      
      .hero p {
        font-size: 1.1rem;
      }
    }

    @media (max-width: 600px) {
      .grid-products {
        grid-template-columns: 1fr;
      }
      
      .header-container {
        flex-direction: column;
        gap: 15px;
      }
      
      .nav-container {
        width: 100%;
        justify-content: center;
      }
      
      nav {
        flex-wrap: wrap;
        justify-content: center;
      }
      
      nav a {
        margin: 5px 10px;
      }
      
      .hero-buttons {
        flex-direction: column;
        gap: 15px;
        width: 100%;
      }
      .hero-buttons .btn,
      .hero-buttons .btn-secondary {
        width: 100%;
        min-width: unset;
      }
    }

    .product {
      background-color: #fff;
      border-radius: 12px;
      padding: 25px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: transform 0.3s, box-shadow 0.3s;
      height: 100%;
      align-self: stretch;
      min-height: 420px;
      position: relative;
      overflow: hidden;
    }

    .product-img {
      width: 100%;
      height: 140px;
      object-fit: cover;
      border-radius: 8px;
      margin-bottom: 12px;
      background: #f0f7ff;
      box-shadow: 0 2px 8px rgba(0,102,178,0.06);
    }

    .product-actions {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 12px;
      width: 100%;
    }

    .product-action {
      flex: 1 1 auto;
      min-width: 0;
      padding: 12px 0;
      font-size: 1.08rem;
      border-radius: 28px;
      background: linear-gradient(90deg, #0066b2 0%, #3d9bff 100%);
      color: #fff;
      border: none;
      font-weight: 700;
      box-shadow: 0 4px 16px rgba(0,102,178,0.10);
      transition: background 0.2s, color 0.2s, box-shadow 0.2s, transform 0.2s;
      text-align: center;
      text-decoration: none;
      outline: none;
      cursor: pointer;
      margin-right: 16px;
      letter-spacing: 0.5px;
      position: relative;
      z-index: 1;
      border: 2px solid transparent;
    }

    .product-action:hover, .product-action:focus {
      background: linear-gradient(90deg, #3d9bff 0%, #0066b2 100%);
      color: #fff;
      box-shadow: 0 8px 24px rgba(0,102,178,0.18);
      transform: translateY(-2px) scale(1.04);
      border-color: #3d9bff;
    }

    .product-actions .icon-btn {
      width: 42px;
      height: 42px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-left: 8px;
      font-size: 1.25rem;
      box-shadow: 0 2px 8px rgba(0,102,178,0.15);
      border: 2px solid #f0f7ff;
      background: #f4f7fa;
      color: #0066b2;
      transition: background 0.2s, color 0.2s, box-shadow 0.2s, transform 0.2s;
      text-decoration: none;
      cursor: pointer;
      position: relative;
    }

    .product-actions .icon-btn:focus {
      outline: 2px solid #3d9bff;
      outline-offset: 2px;
    }

    .product-actions .icon-btn:hover::after, .product-actions .icon-btn:focus::after {
      content: attr(title);
      position: absolute;
      top: 110%;
      left: 50%;
      transform: translateX(-50%);
      background: #0066b2;
      color: #fff;
      padding: 4px 10px;
      border-radius: 6px;
      font-size: 0.85rem;
      white-space: nowrap;
      z-index: 10;
      pointer-events: none;
    }

    .product-actions .whatsapp-btn {
      background: #25d366;
      color: #fff;
      border-color: #25d366;
    }
    .product-actions .whatsapp-btn:hover, .product-actions .whatsapp-btn:focus {
      background: #128c7e;
      color: #fff;
      border-color: #128c7e;
    }

    .product-actions .gmail-btn {
      background: #fff;
      color: #ea4335;
      border: 2px solid #eee;
    }
    .product-actions .gmail-btn:hover, .product-actions .gmail-btn:focus {
      background: #ea4335;
      color: #fff;
      border-color: #ea4335;
    }

    /* Animation cascade sur les produits */
    .product {
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.7s cubic-bezier(.4,0,.2,1), transform 0.7s cubic-bezier(.4,0,.2,1);
    }
    .product.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Testimonials */
    .testimonials {
      background-color: #f0f7ff;
      padding: 60px 40px;
      margin: 40px 0;
    }

    .testimonials-container {
      max-width: 1000px;
      margin: 0 auto;
      text-align: center;
    }

    .testimonials h2 {
      font-size: 2rem;
      color: #004d8c;
      margin-bottom: 40px;
    }

    .testimonial-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 30px;
    }

    @media (max-width: 900px) {
      .testimonial-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 600px) {
      .testimonial-grid {
        grid-template-columns: 1fr;
      }
    }

    .testimonial {
      background-color: white;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.08);
      position: relative;
    }

    .testimonial-text {
      font-style: italic;
      color: #555;
      margin-bottom: 20px;
      line-height: 1.6;
    }

    .testimonial-author {
      font-weight: 600;
      color: #004d8c;
    }

    .testimonial-role {
      font-size: 0.9rem;
      color: #666;
      margin-top: 3px;
    }

    .testimonial-quote {
      position: absolute;
      top: -15px;
      left: 20px;
      color: #0066b2;
      font-size: 2rem;
      opacity: 0.2;
    }

    /* Call to action */
    .cta {
      background: linear-gradient(135deg, #0066b2 0%, #004d8c 100%);
      color: white;
      padding: 50px 40px;
      text-align: center;
      margin-top: 40px;
    }

    .cta-container {
      max-width: 800px;
      margin: 0 auto;
    }

    .cta h2 {
      font-size: 2rem;
      margin-bottom: 20px;
    }

    .cta p {
      font-size: 1.1rem;
      margin-bottom: 30px;
      opacity: 0.9;
      line-height: 1.6;
    }

    .cta .btn {
      background-color: white;
      color: #0066b2;
      font-size: 1.1rem;
      padding: 14px 30px;
    }

    .cta .btn:hover {
      background-color: #f0f7ff;
    }

    footer {
      background-color: #004d8c;
      color: white;
      padding: 50px 40px 20px;
      box-shadow: 0 -3px 6px rgba(0,0,0,0.1);
    }

    .footer-container {
      max-width: 1400px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 40px;
    }

    @media (max-width: 900px) {
      .footer-container {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 600px) {
      .footer-container {
        grid-template-columns: 1fr;
      }
    }

    .footer-section h3 {
      font-size: 1.2rem;
      margin-bottom: 20px;
      position: relative;
      padding-bottom: 10px;
    }

    .footer-section h3:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 50px;
      height: 2px;
      background-color: #3d9bff;
    }

    .footer-section ul {
      list-style: none;
    }

    .footer-section li {
      margin-bottom: 10px;
    }

    .footer-section a {
      color: #b3d9ff;
      text-decoration: none;
      transition: color 0.2s ease;
    }

    .footer-section a:hover {
      color: white;
      text-decoration: underline;
    }

    .footer-newsletter input {
      background-color: rgba(255,255,255,0.1);
      border: none;
      padding: 12px 15px;
      border-radius: 4px;
      color: white;
      width: 100%;
      margin-bottom: 10px;
    }

    .footer-newsletter input::placeholder {
      color: rgba(255,255,255,0.6);
    }

    .social-icons {
      display: flex;
      gap: 15px;
      margin-top: 15px;
    }

    .social-icons a {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 36px;
      height: 36px;
      background-color: rgba(255,255,255,0.1);
      border-radius: 50%;
      transition: all 0.3s ease;
    }

    .social-icons a:hover {
      background-color: rgba(255,255,255,0.2);
      transform: translateY(-3px);
    }

    /* Barre de progression pour lecture */
    .progress-container {
      width: 100%;
      height: 5px;
      background: transparent;
      position: fixed;
      top: 0;
      left: 0;
      z-index: 1000;
    }
    
    .progress-bar {
      height: 5px;
      background: #3d9bff;
      width: 0%;
    }
    
    /* Badge promo */
    .promo-badge {
      position: absolute;
      top: -12px;
      right: -12px;
      background: #ff6b6b;
      color: white;
      padding: 5px 10px;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: 700;
      box-shadow: 0 2px 5px rgba(0,0,0,0.15);
      z-index: 2;
    }
    
    /* Badge nouveauté */
    .new-badge {
      position: absolute;
      top: -12px;
      right: -12px;
      background: #6bc86f;
      color: white;
      padding: 5px 10px;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: 700;
      box-shadow: 0 2px 5px rgba(0,0,0,0.15);
      z-index: 2;
    }

    /* Floating button */
    .floating-btn {
      position: fixed;
      bottom: 30px;
      right: 30px;
      width: 60px;
      height: 60px;
      background-color: #0066b2;
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      cursor: pointer;
      z-index: 99;
      transition: all 0.3s ease;
    }
    
    .floating-btn:hover {
      background-color: #004d8c;
      transform: translateY(-5px);
    }
    
    .floating-btn i {
      font-size: 1.5rem;
    }

    /* Amélioration de l'affichage des boutons d'action produit */
.product-actions {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 12px;
  gap: 0;
  width: 100%;
}

.product-action {
  flex: 1 1 auto;
  min-width: 0;
  padding: 12px 0;
  font-size: 1.08rem;
  border-radius: 28px;
  background: linear-gradient(90deg, #0066b2 0%, #3d9bff 100%);
  color: #fff;
  border: none;
  font-weight: 700;
  box-shadow: 0 4px 16px rgba(0,102,178,0.10);
  transition: background 0.2s, color 0.2s, box-shadow 0.2s, transform 0.2s;
  text-align: center;
  text-decoration: none;
  outline: none;
  cursor: pointer;
  margin-right: 16px;
  letter-spacing: 0.5px;
  position: relative;
  z-index: 1;
}

.product-action:hover {
  background: linear-gradient(90deg, #3d9bff 0%, #0066b2 100%);
  color: #fff;
  box-shadow: 0 8px 24px rgba(0,102,178,0.18);
  transform: translateY(-2px) scale(1.04);
}

.product-actions .icon-btn {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-left: 8px;
  margin-right: 0;
  font-size: 1.25rem;
  box-shadow: 0 2px 8px rgba(0,102,178,0.08);
  transition: background 0.2s, color 0.2s, box-shadow 0.2s, transform 0.2s;
  text-decoration: none;
  cursor: pointer;
}

.product-actions .whatsapp-btn {
  background: #25d366;
  color: #fff;
}

.product-actions .whatsapp-btn:hover {
  background: #128c7e;
  color: #fff;
}

.product-actions .gmail-btn {
  background: #fff;
  color: #ea4335;
  border: 1.5px solid #eee;
}

.product-actions .gmail-btn:hover {
  background: #ea4335;
  color: #fff;
  border-color: #ea4335;
}

/* Responsive : sur mobile, les boutons passent en colonne */
@media (max-width: 600px) {
  .product-actions {
    flex-direction: column;
    align-items: stretch;
    gap: 10px;
  }
  .product-action {
    margin-right: 0;
    margin-bottom: 6px;
  }
  .product-actions .icon-btn {
    margin-left: 0;
  }
  .product-img {
    height: 110px;
  }
}
  </style>
</head>
<body>
  <!-- Barre de progression -->
  <div class="progress-container">
    <div class="progress-bar" id="progressBar"></div>
  </div>

  <header>
    <div class="header-container">
      <a href="#" class="logo">
        <div class="logo-icon"><i class="fas fa-bold"></i></div>
        <span>Brice</span>
      </a>
      <div class="nav-container">
        <nav>
          <a href="#produits">Tous les produits</a>
          <a href="#templates">Templates</a>
          <a href="#formations">Formations</a>
          <a href="#ebooks">E-Books</a>
          <a href="#blog">Blog</a>
          <a href="#contact">Contact</a>
        </nav>
      </div>
    </div>
  </header>

  <!-- Nouvelle section hero avec phrase d'accroche -->
  <section class="hero">
    <div class="hero-container">
      <h1>Transformez vos compétences digitales avec nos ressources premium</h1>
      <p>Des guides experts, des formations adaptées et des templates professionnels pour vous aider à réussir dans l'univers numérique d'aujourd'hui et de demain.</p>
      <div class="hero-buttons">
        <a href="#produits" class="btn">Découvrir nos produits</a>
        <a href="#contact" class="btn-secondary">Nous contacter</a>
      </div>
    </div>
  </section>

  <main>
    <div class="search-container">
      <input type="text" class="search-bar" placeholder="Rechercher un produit, une formation ou un template...">
    </div>

    <!-- Section d'introduction avec phrase d'accroche -->
    <div class="section-intro">
      <h2>Des ressources soigneusement conçues pour votre réussite</h2>
      <p>Que vous soyez débutant ou expert, notre catalogue complet vous offre les outils nécessaires pour développer vos compétences et optimiser votre productivité au quotidien.</p>
    </div>

    <div class="category-filter">
      <button class="filter-btn active">Tous</button>
      <button class="filter-btn">Templates</button>
      <button class="filter-btn">Formations</button>
      <button class="filter-btn">E-Books</button>
      <button class="filter-btn">Scripts</button>
      <button class="filter-btn">Tutoriels</button>
    </div>

    <section id="produits" class="grid-products">
      <article class="product">
        <span class="product-tag">Guide</span>
        <span class="promo-badge">-20%</span>
        <img src="images/guide-nettoyage-windows.jpg" alt="Guide Nettoyage Windows 10 & 11" class="product-img" loading="lazy" />
        <h2>📘 Guide Nettoyage Windows 10 & 11</h2>
        <p>Optimisez et accélérez votre PC avec ce guide complet et facile à suivre. Supprimez les logiciels indésirables et optimisez les performances système.</p>
        <span class="product-price">12,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit1" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Guide%20Nettoyage%20Windows%2010%20%26%2011" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Guide%20Nettoyage%20Windows%2010%20%26%2011" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Formation</span>
        <img src="images/formation-video.jpg" alt="Production Vidéo Professionnelle" class="product-img" loading="lazy" />
        <h2>🎬 Production Vidéo Professionnelle</h2>
        <p>Apprenez à créer des vidéos de qualité professionnelle pour vos projets marketing et votre présence en ligne.</p>
        <span class="product-price">49,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit20" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Production%20Vidéo%20Professionnelle" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Production%20Vidéo%20Professionnelle" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Tutoriel</span>
        <img src="images/tutoriel-installation-n8n.jpg" alt="Installation n8n sous Linux Mint" class="product-img" loading="lazy" />
        <h2>⚙️ Installation n8n sous Linux Mint</h2>
        <p>Apprenez à installer n8n, un outil d'automatisation puissant, étape par étape. Configuration complète et exemples pratiques inclus.</p>
        <span class="product-price">9,99 €</span>
        <div class="product-actions">
          <a href="https://payhip.com/b/ton-produit2" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Installation%20n8n%20sous%20Linux%20Mint" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Installation%20n8n%20sous%20Linux%20Mint" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Template</span>
        <img src="images/template-notion-productivite.jpg" alt="Template Notion Productivité" class="product-img" loading="lazy" />
        <h2>📝 Template Notion Productivité</h2>
        <p>Boostez votre organisation avec ce template prêt à l'emploi pour Notion. Gestion des tâches, projets et objectifs en un seul endroit.</p>
        <span class="product-price">14,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit3" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Template%20Notion%20Productivité" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Template%20Notion%20Productivité" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Dashboard</span>
        <img src="images/dashboard-automatisation.jpg" alt="Dashboard Automatisation" class="product-img" loading="lazy" />
        <h2>📊 Dashboard Automatisation</h2>
        <p>Un dashboard prêt à l'emploi pour suivre et automatiser vos tâches quotidiennes. Visualisez votre progression et optimisez votre workflow.</p>
        <span class="product-price">24,99 €</span>
        <div class="product-actions">
          <a href="https://payhip.com/b/ton-produit4" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Dashboard%20Automatisation" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Dashboard%20Automatisation" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Formation</span>
        <span class="new-badge">Nouveau</span>
        <img src="images/formation-bases-ia.jpg" alt="Formation Bases de l'IA" class="product-img" loading="lazy" />
        <h2>📚 Formation Bases de l'IA</h2>
        <p>Découvrez les fondamentaux de l'intelligence artificielle et ses applications. Formation en ligne complète avec exercices pratiques.</p>
        <span class="product-price">49,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit5" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Formation%20Bases%20de%20l'IA" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Formation%20Bases%20de%20l'IA" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Scripts</span>
        <img src="images/scripts-automatisation.jpg" alt="Scripts d'Automatisation" class="product-img" loading="lazy" />
        <h2>🔧 Scripts d'Automatisation</h2>
        <p>Collection de scripts pour automatiser vos workflows répétitifs facilement. Compatible avec Windows, Mac et Linux pour tous vos besoins.</p>
        <span class="product-price">19,99 €</span>
        <div class="product-actions">
          <a href="https://payhip.com/b/ton-produit6" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Scripts%20d'Automatisation" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Scripts%20d'Automatisation" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">E-Book</span>
        <img src="images/ebook-strategies-digitales.jpg" alt="E-book Stratégies Digitales" class="product-img" loading="lazy" />
        <h2>💡 E-book Stratégies Digitales</h2>
        <p>Guide complet pour développer votre présence en ligne et votre business digital. Stratégies testées et approuvées pour tous les secteurs.</p>
        <span class="product-price">17,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit7" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20E-book%20Stratégies%20Digitales" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20E-book%20Stratégies%20Digitales" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Design</span>
        <img src="images/pack-templates-design.jpg" alt="Pack Templates Design" class="product-img" loading="lazy" />
        <h2>🖼 Pack Templates Design</h2>
        <p>Des modèles graphiques modernes et personnalisables pour vos projets digitaux. Inclut fichiers sources pour Photoshop et Figma.</p>
        <span class="product-price">29,99 €</span>
        <div class="product-actions">
          <a href="https://payhip.com/b/ton-produit8" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Pack%20Templates%20Design" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Pack%20Templates%20Design" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Tutoriel</span>
        <img src="images/tutoriel-video-automatisation.jpg" alt="Tutoriel Vidéo Automatisation" class="product-img" loading="lazy" />
        <h2>🎥 Tutoriel Vidéo Automatisation</h2>
        <p>Apprenez à créer des automatisations avancées en vidéo, pas à pas. Plus de 3 heures de formation approfondie avec exemples pratiques.</p>
        <span class="product-price">34,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit9" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Tutoriel%20Vidéo%20Automatisation" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Tutoriel%20Vidéo%20Automatisation" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Guide</span>
        <img src="images/guide-marketing-mobile.jpg" alt="Guide Marketing Mobile" class="product-img" loading="lazy" />
        <h2>📱 Guide Marketing Mobile</h2>
        <p>Techniques et astuces pour promouvoir efficacement vos produits sur mobile. Apprenez à créer des campagnes ciblées à fort impact.</p>
        <span class="product-price">15,99 €</span>
        <div class="product-actions">
          <a href="https://payhip.com/b/ton-produit10" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Guide%20Marketing%20Mobile" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Guide%20Marketing%20Mobile" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
      <article class="product">
        <span class="product-tag">Template</span>
        <img src="images/template-analytics-dashboard.jpg" alt="Template Analytics Dashboard" class="product-img" loading="lazy" />
        <h2>📊 Template Analytics Dashboard</h2>
        <p>Dashboard interactif pour suivre et analyser les performances de votre site web ou application. Compatible avec Google Analytics.</p>
        <span class="product-price">22,99 €</span>
        <div class="product-actions">
          <a href="https://gumroad.com/l/ton-produit11" target="_blank" class="btn product-action" rel="noopener">Plus d'info</a>
          <a href="https://wa.me/?text=Je%20souhaite%20plus%20d'informations%20sur%20ce%20produit%20:%20Template%20Analytics%20Dashboard" target="_blank" class="icon-btn whatsapp-btn" title="Contacter sur WhatsApp" rel="noopener" aria-label="WhatsApp">
            <i class="fab fa-whatsapp"></i>
          </a>
          <a href="mailto:?subject=Demande%20d'information%20sur%20le%20produit%20Template%20Analytics%20Dashboard" class="icon-btn gmail-btn" title="Contacter par Gmail" rel="noopener" aria-label="Gmail">
            <i class="far fa-envelope"></i>
          </a>
        </div>
      </article>
    </section>
    
    <!-- Section témoignages -->
    <section class="testimonials">
      <div class="testimonials-container">
        <h2>Ce que nos clients disent</h2>
        <div class="testimonial-grid">
          <div class="testimonial">
            <div class="testimonial-quote"><i class="fas fa-quote-left"></i></div>
            <p class="testimonial-text">Le guide Windows m'a permis d'optimiser mon ordinateur en moins d'une heure. Je n'ai jamais vu mon PC être aussi rapide !</p>
            <p class="testimonial-author">Marie D.</p>
            <p class="testimonial-role">Entrepreneure</p>
          </div>
          <div class="testimonial">
            <div class="testimonial-quote"><i class="fas fa-quote-left"></i></div>
            <p class="testimonial-text">Les templates Notion ont complètement changé ma façon de travailler. Un gain de temps incroyable et une organisation impeccable.</p>
            <p class="testimonial-author">Thomas L.</p>
            <p class="testimonial-role">Chef de projet</p>
          </div>
          <div class="testimonial">
            <div class="testimonial-quote"><i class="fas fa-quote-left"></i></div>
            <p class="testimonial-text">La formation sur l'IA est la plus complète que j'ai suivie. Très pédagogique même pour les débutants comme moi.</p>
            <p class="testimonial-author">Sophie M.</p>
            <p class="testimonial-role">Consultante Marketing</p>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Call to action -->
    <section class="cta">
      <div class="cta-container">
        <h2>Prêt à faire passer vos compétences au niveau supérieur ?</h2>
        <p>Rejoignez plus de 15 000 professionnels qui ont déjà transformé leur workflow grâce à nos ressources et formations.</p>
        <a href="#produits" class="btn">Découvrir notre catalogue</a>
      </div>
    </section>
  </main>

  <!-- Footer complet -->
  <footer>
    <div class="footer-container">
      <div class="footer-section">
        <h3>À propos de Brice</h3>
        <p style="color: #b3d9ff; line-height: 1.6; margin-bottom: 15px;">Expert en productivité et outils digitaux, je partage mes connaissances pour vous aider à optimiser votre travail et améliorer vos compétences numériques.</p>
        <div class="social-icons">
          <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
          <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
          <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
          <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
        </div>
      </div>
      <div class="footer-section">
        <h3>Liens rapides</h3>
        <ul>
          <li><a href="#produits">Tous les produits</a></li>
          <li><a href="#templates">Templates</a></li>
          <li><a href="#formations">Formations</a></li>
          <li><a href="#ebooks">E-Books</a></li>
          <li><a href="#blog">Blog</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
      <div class="footer-section">
        <h3>Informations légales</h3>
        <ul>
          <li><a href="#">Mentions légales</a></li>
          <li><a href="#">Politique de confidentialité</a></li>
          <li><a href="#">Conditions générales de vente</a></li>
          <li><a href="#">Politique de remboursement</a></li>
          <li><a href="#">Politique des cookies</a></li>
        </ul>
      </div>
      <div class="footer-section footer-newsletter">
        <h3>Newsletter</h3>
        <p style="color: #b3d9ff; line-height: 1.6; margin-bottom: 15px;">Inscrivez-vous pour recevoir mes derniers conseils, tutoriels et offres exclusives.</p>
        <form>
          <input type="email" placeholder="Votre adresse email" aria-label="Email pour la newsletter">
          <button type="submit" class="btn">S'inscrire</button>
        </form>
        <p style="color: #b3d9ff; font-size: 0.8rem; margin-top: 10px;">En vous inscrivant, vous acceptez notre politique de confidentialité.</p>
      </div>
    </div>
    <div class="copyright">
      <p>&copy; 2025 Brice - Tous droits réservés. Conçu avec <i class="fas fa-heart" style="color: #ff6b6b;"></i> en France.</p>
    </div>
  </footer>

    <script>
document.addEventListener('DOMContentLoaded', function() {
  const filterButtons = document.querySelectorAll('.filter-btn');
  const searchBar = document.querySelector('.search-bar');
  const products = document.querySelectorAll('.product');

  let activeCategory = 'Tous';

  // Fonction de filtrage combinée
  function filterProducts() {
    const searchTerm = searchBar.value.toLowerCase().trim();

    products.forEach(product => {
      const title = product.querySelector('h2').textContent.toLowerCase();
      const description = product.querySelector('p').textContent.toLowerCase();
      const tag = product.querySelector('.product-tag').textContent.toLowerCase();

      // Vérifie la catégorie
      const matchesCategory = (activeCategory === 'Tous') ||
        tag === activeCategory.toLowerCase() ||
        (activeCategory === 'Scripts' && tag === 'scripts') ||
        (activeCategory === 'E-Books' && (tag === 'e-book' || tag === 'ebook')) ||
        (activeCategory === 'Tutoriels' && tag === 'tutoriel') ||
        (activeCategory === 'Templates' && tag === 'template') ||
        (activeCategory === 'Formations' && tag === 'formation');

      // Vérifie la recherche texte
      const matchesSearch = title.includes(searchTerm) || description.includes(searchTerm) || tag.includes(searchTerm);

      if (matchesCategory && matchesSearch) {
        product.style.display = ''; // Affiche normalement dans la grille
      } else {
        product.style.display = 'none';
      }
    });
  }

  // Gestion des boutons de filtre
  filterButtons.forEach(button => {
    button.addEventListener('click', function() {
      filterButtons.forEach(btn => btn.classList.remove('active'));
      this.classList.add('active');
      activeCategory = this.textContent.trim();
      filterProducts();
    });
  });

  // Recherche texte
  searchBar.addEventListener('input', filterProducts);

  // Rendre tous les produits et témoignages visibles immédiatement
  function showAllElements() {
    const elements = document.querySelectorAll('.product, .testimonial');
    elements.forEach((element, index) => {
      element.style.opacity = '1';
      element.style.transform = 'translateY(0)';
      element.classList.add('visible');
      element.style.transitionDelay = (index * 0.05) + 's';
    });
  }

  // Barre de progression
  window.onscroll = function() {
    let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
    let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
    let scrolled = (winScroll / height) * 100;
    document.getElementById("progressBar").style.width = scrolled + "%";
  };

  // Lancer le filtrage au chargement
  filterProducts();

  // Forcer l'affichage de tous les éléments au chargement
  showAllElements();
});
</script>

<script>
document.querySelector('.footer-newsletter form').addEventListener('submit', function(e) {
  e.preventDefault();
  const input = this.querySelector('input[type="email"]');
  const email = input.value.trim();
  let msg = document.createElement('div');
  msg.style.marginTop = "10px";
  msg.style.fontSize = "0.95rem";
  msg.style.color = "#6bc86f";
  msg.textContent = "Merci pour votre inscription !";
  if (email && /\S+@\S+\.\S+/.test(email)) {
    this.appendChild(msg);
    input.value = '';
    setTimeout(() => msg.remove(), 4000);
  } else {
    msg.textContent = "Veuillez entrer un email valide.";
    msg.style.color = "#ff6b6b";
    this.appendChild(msg);
    setTimeout(() => msg.remove(), 4000);
  }
});
</script>
</body>
</html>
