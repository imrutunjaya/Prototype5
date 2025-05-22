<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>The Great Adventure - Minimal Line Theme</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

  /* Reset */
  *, *::before, *::after {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    font-family: 'Roboto', sans-serif;
    background: #fafafa;
    color: #222;
    line-height: 1.5;
  }
  a {
    color: inherit;
    text-decoration: none;
  }
  a:hover, a:focus {
    text-decoration: underline;
  }

  /* Container */
  .container {
    max-width: 720px;
    margin: 0 auto 3rem;
    padding: 1.5rem;
  }

  /* Hero Section */
  .hero {
    position: relative;
    background: linear-gradient(135deg, #e0e0e0 0%, #f9f9f9 100%);
    border-radius: 8px;
    padding: 3rem 2rem 4rem;
    text-align: center;
  }
  .hero img {
    max-width: 160px;
    width: 100%;
    height: auto;
    margin-bottom: 1.5rem;
    filter: grayscale(40%);
  }
  .hero-title {
    font-weight: 700;
    font-size: 2.8rem;
    margin-bottom: 0.5rem;
    color: #222;
  }
  .hero-subtitle {
    font-weight: 500;
    font-size: 1.25rem;
    color: #555;
    margin-bottom: 1.75rem;
  }

  /* Buttons row */
  .buttons {
    display: inline-flex;
    gap: 1rem;
  }
  button, a.button {
    font-family: inherit;
    font-weight: 600;
    font-size: 1rem;
    padding: 0.5rem 1.75rem;
    border-radius: 22px;
    background: transparent;
    border: 2px solid #555;
    color: #555;
    cursor: pointer;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  button:hover, a.button:hover,
  button:focus, a.button:focus {
    border-color: #007acc;
    color: #007acc;
    outline: none;
    text-decoration: none;
  }
  button svg, a.button svg {
    stroke: currentColor;
    stroke-width: 2;
    fill: none;
    width: 18px;
    height: 18px;
  }

  /* Author text */
  .author {
    margin-top: 1.5rem;
    font-size: 1rem;
    color: #888;
  }

  /* Section default style */
  section {
    margin-top: 3rem;
    padding-top: 1rem;
    border-top: 1px solid #ddd;
  }
  section:first-of-type {
    margin-top: 2rem;
    border-top: none;
    padding-top: 0;
  }
  h2 {
    font-weight: 700;
    font-size: 1.8rem;
    margin-bottom: 1rem;
    color: #007acc;
  }

  /* Preview gallery */
  .preview-gallery {
    display: flex;
    gap: 1rem;
    overflow-x: auto;
    padding-bottom: 0.5rem;
  }
  .preview-gallery img {
    border-radius: 8px;
    height: 160px;
    flex-shrink: 0;
    box-shadow: none;
    transition: box-shadow 0.3s ease, transform 0.3s ease;
    cursor: pointer;
  }
  .preview-gallery img:hover, .preview-gallery img:focus {
    box-shadow: 0 4px 12px rgba(0, 120, 212, 0.3);
    transform: scale(1.05);
    outline: none;
  }

  /* About text */
  .about-text {
    font-size: 1.1rem;
    color: #333;
  }

  /* Ratings */
  .ratings {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  .stars {
    display: flex;
    gap: 4px;
  }
  .stars svg {
    width: 22px;
    height: 22px;
    stroke: #f2b01e; /* golden stroke */
    fill: none;
  }
  .stars svg.filled {
    fill: #f2b01e;
  }
  .rating-score {
    font-weight: 700;
    font-size: 1.25rem;
    color: #222;
  }
  .rating-count {
    font-size: 0.95rem;
    color: #666;
  }

  /* Notes & Support */
  .notes-text {
    font-size: 1rem;
    color: #444;
  }
  .notes-link {
    color: #007acc;
    text-decoration: none;
  }
  .notes-link:hover, .notes-link:focus {
    text-decoration: underline;
  }

  /* Scrollbar styling for preview */
  .preview-gallery::-webkit-scrollbar {
    height: 6px;
  }
  .preview-gallery::-webkit-scrollbar-track {
    background: #eee;
    border-radius: 3px;
  }
  .preview-gallery::-webkit-scrollbar-thumb {
    background: #007acc;
    border-radius: 3px;
  }

  /* Responsive */
  @media (max-width: 600px) {
    .hero {
      padding: 2rem 1rem 3rem;
    }
    .hero-title {
      font-size: 2.25rem;
    }
    .buttons {
      flex-wrap: wrap;
      justify-content: center;
    }
    .preview-gallery img {
      height: 120px;
    }
  }
</style>
</head>
<body>
  <div class="container" role="main" aria-label="Book landing page The Great Adventure">

    <header class="hero" aria-label="Book cover and title">
      <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=160&q=80"
        alt="Book cover image of The Great Adventure" loading="lazy" />
      <h1 class="hero-title">The Great Adventure</h1>
      <p class="hero-subtitle">By Geeks for Geeks</p>
      <div class="buttons" role="group" aria-label="Page actions">
        <a href="https://example.com/read-the-great-adventure" target="_blank" rel="noopener" class="button btn" role="button" aria-label="Read The Great Adventure">Read
          <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
            <path d="M5 12h14M13 5l7 7-7 7" stroke-linecap="round" stroke-linejoin="round"/>
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
            <path d="M3 6h18M9 6V4a3 3 0 0 1 6 0v2M10.29 11H13.7l.79 7H9.5z"/>
          </svg>
          Report
        </button>
      </div>
      <p class="author" aria-label="Author name">Author: Geeks for Geeks</p>
    </header>

    <section aria-label="Book preview images">
      <h2>Preview</h2>
      <div class="preview-gallery" tabindex="0">
        <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=400&q=80" alt="Preview page 1" />
        <img src="https://images.unsplash.com/photo-1544716278-fd38580f106e?auto=format&fit=crop&w=400&q=80" alt="Preview page 2" />
        <img src="https://images.unsplash.com/photo-1590608897129-79d0b03ecbde?auto=format&fit=crop&w=400&q=80" alt="Preview page 3" />
        <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?auto=format&fit=crop&w=400&q=80" alt="Preview page 4" />
      </div>
    </section>

    <section aria-label="About the book The Great Adventure">
      <h2>About this Book</h2>
      <p class="about-text">
        "The Great Adventure" is an enthralling journey that explores themes of courage, friendship, and self-discovery. Written by the Geeks for Geeks team, this book weaves a tale that pulls readers into a vivid world full of memorable characters and unexpected twists. Perfect for fans of gripping storytelling and emotional depth.
      </p>
    </section>

    <section aria-label="Book ratings and reviews">
      <h2>Ratings & Reviews</h2>
      <div class="ratings" aria-live="polite" aria-atomic="true">
        <div class="stars" aria-hidden="true" role="img" aria-label="4 out of 5 stars">
          <svg class="filled"><circle cx="12" cy="12" r="10"/></svg>
          <svg class="filled"><circle cx="12" cy="12" r="10"/></svg>
          <svg class="filled"><circle cx="12" cy="12" r="10"/></svg>
          <svg class="filled"><circle cx="12" cy="12" r="10"/></svg>
          <svg class="empty"><circle cx="12" cy="12" r="10"/></svg>
        </div>
        <div class="rating-score" aria-label="Rating score">4.0</div>
        <div class="rating-count" aria-label="Total ratings">(1,234 ratings)</div>
      </div>
    </section>

    <section aria-label="Notes and support for The Great Adventure">
      <h2>Notes & Support</h2>
      <p class="notes-text">
        If you experience any issues with this book or its content, please visit our <a href="https://example.com/support" class="notes-link" target="_blank" rel="noopener">Support Page</a> for assistance and further information.
      </p>
      <p class="notes-text">We appreciate your feedback to help us improve.</p>
    </section>

  </div>
</body>
</html>
