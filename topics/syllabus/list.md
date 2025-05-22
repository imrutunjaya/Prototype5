# The Great Adventure - Professional Line-Themed Landing Page

<style>
  /* Base resets */
  *, *::before, *::after {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    font-family: 'Roboto', sans-serif;
    background: #fafafa;
    color: #222;
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
  a {
    text-decoration: none;
    color: inherit;
    transition: color 0.3s ease;
  }
  a:hover, a:focus {
    color: #0057ff;
    outline: none;
    text-decoration: underline;
  }
  /* Container */
  .container {
    max-width: 960px;
    margin: 2rem auto 4rem;
    padding: 0 2rem;
    user-select: text;
  }
  /* Hero section */
  .hero {
    position: relative;
    background: url('https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=1300&q=80') center / cover no-repeat;
    padding: 4rem 3rem 5rem;
    border-radius: 14px;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    box-shadow: inset 0 0 120px 40px rgba(0, 0, 0, 0.6);
  }
  .hero-content {
    position: relative;
    z-index: 1;
  }
  .hero-title {
    font-size: 3rem;
    font-weight: 800;
    margin: 0 0 0.5rem 0;
    letter-spacing: 0.03em;
    text-shadow: 0 3px 7px rgba(0,0,0,0.7);
  }
  .hero-subtitle {
    font-weight: 500;
    font-size: 1.25rem;
    margin: 0 0 2.2rem 0;
    opacity: 0.85;
    text-shadow: 0 2px 5px rgba(0,0,0,0.5);
  }
  /* Buttons container */
  .buttons {
    display: flex;
    gap: 1.5rem;
    flex-wrap: wrap;
    align-items: center;
  }
  /* General button styles */
  .btn, button {
    cursor: pointer;
    padding: 0.6rem 2.8rem;
    font-size: 1.15rem;
    font-weight: 700;
    border-radius: 32px;
    border: 2.5px solid #0057ff;
    background: transparent;
    color: #0057ff;
    display: inline-flex;
    align-items: center;
    gap: 0.7rem;
    transition: background-color 0.3s ease, color 0.3s ease, box-shadow 0.3s ease;
    user-select: none;
  }
  .btn svg, button svg {
    stroke: currentColor;
    stroke-width: 2.8;
    fill: none;
    width: 22px;
    height: 22px;
  }
  .btn:hover, .btn:focus,
  button:hover, button:focus {
    color: #fff;
    background-color: #0057ff;
    outline-offset: 2px;
    outline: 3px solid #0047d5;
    box-shadow: 0 0 20px #0070ff88;
    text-decoration: none;
  }
  .btn:focus-visible, button:focus-visible {
    outline-offset: 2px;
    outline: 3px solid #003db0;
  }
  /* Author text */
  .author {
    margin-top: 1.8rem;
    font-weight: 500;
    font-size: 1.1rem;
    opacity: 0.8;
    letter-spacing: 0.02em;
    user-select: text;
  }
  /* Sections styles */
  section {
    background: white;
    border-radius: 14px;
    margin-top: 3.5rem;
    padding: 3rem 3rem 4rem;
    box-shadow: 0 10px 28px rgba(0, 0, 0, 0.07);
  }
  section h2 {
    font-size: 2rem;
    font-weight: 800;
    margin-bottom: 1.8rem;
    color: #0057ff;
    letter-spacing: 0.01em;
  }
  /* Preview gallery */
  .preview-gallery {
    display: flex;
    gap: 1.3rem;
    overflow-x: auto;
    padding-bottom: 1rem;
    scrollbar-width: thin;
    scrollbar-color: #0057ff #e8e8e8;
  }
  .preview-gallery::-webkit-scrollbar {
    height: 9px;
  }
  .preview-gallery::-webkit-scrollbar-track {
    background: #e8e8e8;
    border-radius: 6px;
  }
  .preview-gallery::-webkit-scrollbar-thumb {
    background-color: #0057ff;
    border-radius: 6px;
  }
  .preview-gallery img {
    height: 190px;
    border-radius: 16px;
    flex-shrink: 0;
    object-fit: cover;
    box-shadow: 0 7px 26px rgb(0 87 255 / 0.2);
    cursor: pointer;
    transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1),
      box-shadow 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .preview-gallery img:hover, .preview-gallery img:focus {
    transform: scale(1.13);
    box-shadow: 0 18px 52px rgb(0 87 255 / 0.58);
    outline: none;
  }
  /* About text */
  .about-text {
    font-size: 1.22rem;
    color: #333;
    line-height: 1.68;
    max-width: 900px;
    user-select: text;
  }
  /* Ratings */
  .ratings {
    display: flex;
    align-items: center;
    gap: 1.6rem;
    margin-top: 2.6rem;
    user-select: none;
  }
  .stars {
    display: flex;
    gap: 8px;
  }
  .stars svg {
    width: 28px;
    height: 28px;
    stroke: #fbbc04;
    stroke-width: 2.8;
    fill: none;
  }
  .stars svg.filled {
    fill: #fbbc04;
  }
  .rating-score {
    font-weight: 800;
    font-size: 1.5rem;
    color: #222;
    user-select: text;
  }
  .rating-count {
    font-size: 1.15rem;
    color: #666;
    opacity: 0.87;
  }
  /* Notes & Support */
  .notes-text {
    font-size: 1.07rem;
    color: #444;
    max-width: 900px;
    margin-top: 2.9rem;
    user-select: text;
  }
  .notes-link {
    color: #0057ff;
    font-weight: 600;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  .notes-link:hover,
  .notes-link:focus {
    color: #003e99;
    text-decoration: underline;
    outline: none;
  }
  /* Responsive */
  @media (max-width: 768px) {
    .container {
      max-width: 90vw;
      padding: 0 1.5rem 3rem;
    }
    .hero {
      padding: 3rem 2rem 3rem;
      height: 280px;
    }
    .hero-title {
      font-size: 2.35rem;
    }
    .hero-subtitle {
      font-size: 1.18rem;
    }
    .btn,
    button {
      font-size: 1rem;
      padding: 0.5rem 2.4rem;
    }
    .preview-gallery img {
      height: 150px;
    }
    section {
      padding: 2.4rem 2.3rem 3rem;
    }
  }
  @media (max-width: 440px) {
    .buttons {
      flex-wrap: wrap;
      justify-content: center;
    }
    .hero-title {
      font-size: 2rem;
    }
    .preview-gallery img {
      height: 120px;
    }
    .btn,
    button {
      padding: 0.48rem 1.7rem;
      font-size: 0.95rem;
    }
    section h2 {
      font-size: 1.7rem;
    }
  }
</style>

<div class="container">

  <header class="hero" aria-label="Hero section with book cover and title">
    <div class="hero-content">
      <h1 class="hero-title">The Great Adventure</h1>
      <p class="hero-subtitle">By Geeks for Geeks</p>
      <div class="buttons" role="group" aria-label="Action buttons">
        <a href="https://example.com/read-the-great-adventure" target="_blank" rel="noopener" class="btn" role="button" aria-label="Read The Great Adventure book">
          Read
          <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
            <path d="M5 12h14M13 5l7 7-7 7" stroke-linecap="round" stroke-linejoin="round" />
          </svg>
        </a>

        <button class="btn" aria-label="More options">
          <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
            <circle cx="12" cy="5" r="2" />
            <circle cx="12" cy="12" r="2" />
            <circle cx="12" cy="19" r="2" />
          </svg>
          More
        </button>

        <button class="btn" aria-label="Report this book">
          <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false" stroke="currentColor" stroke-width="2" stroke-linejoin="round" stroke-linecap="round" fill="none">
            <path d="M3 6h18M9 6V4a3 3 0 0 1 6 0v2M10.29 11H13.7l.79 7H9.5z" />
          </svg>
          Report
        </button>
      </div>
      <p class="author" aria-label="Author name">Author: Geeks for Geeks</p>
    </div>
  </header>

  <section aria-label="Preview images of the book The Great Adventure">
    <h2>Preview</h2>
    <div class="preview-gallery" tabindex="0">
      <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=400&q=80" alt="Preview page 1" />
      <img src="https://images.unsplash.com/photo-1544716278-fd38580f106e?auto=format&fit=crop&w=400&q=80" alt="Preview page 2" />
      <img src="https://images.unsplash.com/photo-1590608897129-79d0b03ecbde?auto=format&fit=crop&w=400&q=80" alt="Preview page 3" />
      <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?auto=format&fit=crop&w=400&q=80" alt="Preview page 4" />
    </div>
  </section>

  <section aria-label="About the book The Great Adventure">
    <h2>About This Book</h2>
    <p class="about-text">
      "The Great Adventure" is an enthralling journey that explores themes of courage, friendship, and self-discovery. Written by the Geeks for Geeks team, this book weaves a tale that pulls readers into a vivid world full of memorable characters and unexpected twists. Perfect for fans of gripping storytelling and emotional depth.
    </p>
  </section>

  <section aria-label="Book ratings and reviews">
    <h2>Ratings & Reviews</h2>
    <div class="ratings" aria-live="polite" aria-atomic="true">
      <div class="stars" aria-hidden="true" role="img" aria-label="4 out of 5 stars rating">
        <svg class="filled"><circle cx="12" cy="12" r="10" /></svg>
        <svg class="filled"><circle cx="12" cy="12" r="10" /></svg>
        <svg class="filled"><circle cx="12" cy="12" r="10" /></svg>
        <svg class="filled"><circle cx="12" cy="12" r="10" /></svg>
        <svg class="empty"><circle cx="12" cy="12" r="10" /></svg>
      </div>
      <div class="rating-score" aria-label="Rating score">4.0</div>
      <div class="rating-count" aria-label="Total number of ratings">(1,234 ratings)</div>
    </div>
  </section>

  <section aria-label="Notes and support for The Great Adventure">
    <h2>Notes & Support</h2>
    <p class="notes-text">
      If you experience any issues with this book or its content, please visit our
      <a href="https://example.com/support" target="_blank" rel="noopener" class="notes-link">Support Page</a> for assistance and further information.
    </p>
    <p class="notes-text">We appreciate your feedback to help us improve.</p>
  </section>

</div>
