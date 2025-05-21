# The Great Adventure - Exciting Book Landing Page

<style>
  /* Container */
  .container {
    max-width: 960px;
    margin: 2rem auto;
    font-family: 'Roboto', Arial, sans-serif;
    color: #202124;
  }
  /* Hero */
  .hero {
    position: relative;
    background: url('https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=1300&q=80') center/cover no-repeat;
    border-radius: 8px;
    height: 280px;
    color: white;
    padding: 2rem 3rem;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    box-shadow: 0 4px 24px rgba(0, 0, 0, 0.5);
    overflow: hidden;
  }
  .hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(180deg, rgba(0,0,0,0.4) 0%, rgba(0,0,0,0.8) 100%);
    border-radius: 8px;
    z-index: 0;
  }
  .hero-content {
    position: relative;
    z-index: 1;
  }
  .hero-title {
    font-size: 2.8rem;
    font-weight: 700;
    margin: 0 0 0.25rem;
    text-shadow: 0 3px 7px rgba(0,0,0,0.7);
  }
  .hero-subtitle {
    font-size: 1.125rem;
    opacity: 0.85;
    margin: 0 0 1.25rem;
    text-shadow: 0 2px 5px rgba(0,0,0,0.6);
  }
  /* Buttons */
  .buttons {
    display: flex;
    gap: 1rem;
    align-items: center;
  }
  .btn {
    background-color: #1a73e8;
    color: white;
    font-weight: 600;
    border-radius: 24px;
    padding: 0.6rem 2.4rem;
    font-size: 1.15rem;
    text-decoration: none;
    border: none;
    cursor: pointer;
    box-shadow: 0 6px 12px rgba(26, 115, 232, 0.6);
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
  }
  .btn:hover, .btn:focus {
    background-color: #145abe;
    box-shadow: 0 8px 20px rgba(20, 90, 190, 0.8);
    outline: none;
  }
  .btn-arrow {
    background-color: white;
    border-radius: 12px;
    width: 44px;
    height: 44px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;
    cursor: pointer;
    box-shadow: 0 3px 8px rgba(0,0,0,0.15);
    border: none;
  }
  .btn-arrow:hover, .btn-arrow:focus {
    background-color: #f1f3f4;
    outline: none;
  }
  .btn-arrow svg {
    width: 24px;
    height: 24px;
    fill: #666;
  }
  .btn-report {
    background-color: transparent;
    color: #1a73e8;
    font-weight: 600;
    border-radius: 24px;
    padding: 0.5rem 1.1rem;
    border: 2px solid #1a73e8;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
  }
  .btn-report:hover, .btn-report:focus {
    background-color: #1a73e8;
    color: white;
    outline: none;
  }
  /* Author */
  .author {
    margin-top: 0.6rem;
    font-weight: 500;
    letter-spacing: 0.02em;
    font-size: 1.05rem;
    opacity: 0.85;
    user-select: none;
  }
  /* Preview */
  .section {
    margin-top: 3.5rem;
    background: white;
    border-radius: 12px;
    padding: 2rem 3rem 3rem;
    box-shadow: 0 6px 15px rgba(0,0,0,0.07);
  }
  .section h2 {
    font-size: 1.95rem;
    margin-bottom: 1rem;
    font-weight: 700;
    color: #1a73e8;
  }
  .preview-gallery {
    display: flex;
    gap: 1rem;
    overflow-x: auto;
    padding-bottom: 1rem;
    scrollbar-width: thin;
    scrollbar-color: #1a73e8 #eee;
  }
  .preview-gallery::-webkit-scrollbar {
    height: 8px;
  }
  .preview-gallery::-webkit-scrollbar-thumb {
    background-color: #1a73e8;
    border-radius: 4px;
  }
  .preview-gallery img {
    flex-shrink: 0;
    height: 180px;
    border-radius: 12px;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 4px 18px rgba(0,0,0,0.1);
  }
  .preview-gallery img:hover,
  .preview-gallery img:focus {
    transform: scale(1.1);
    box-shadow: 0 8px 24px rgba(26, 115, 232, 0.4);
    outline: none;
  }
  /* About */
  .about-text {
    font-size: 1.15rem;
    line-height: 1.6;
    color: #444;
    user-select: text;
  }
  /* Ratings */
  .ratings {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-top: 1.25rem;
    user-select: none;
  }
  .stars svg {
    width: 24px;
    height: 24px;
    fill: #fbbc04;
  }
  .stars svg.empty {
    fill: #ddd;
  }
  .rating-score {
    font-weight: 700;
    font-size: 1.3rem;
    color: #222;
  }
  .rating-count {
    font-size: 1rem;
    opacity: 0.7;
  }
  /* Notes & Support */
  .notes-text {
    margin-top: 2rem;
    font-size: 1rem;
    color: #444;
  }
  .notes-link {
    color: #1a73e8;
    text-decoration: none;
    font-weight: 600;
  }
  .notes-link:hover,
  .notes-link:focus {
    text-decoration: underline;
    outline: none;
  }
</style>

<div class="container">

  <header class="hero" role="banner" aria-label="Book title and cover background">
    <div class="hero-content">
      <h1 class="hero-title">The Great Adventure</h1>
      <p class="hero-subtitle">By Geeks for Geeks</p>
      <div class="buttons" role="group" aria-label="Actions">
        <a href="https://example.com/read-the-great-adventure" class="btn" target="_blank" rel="noopener" role="button" aria-label="Read The Great Adventure book">Read</a>
        <button class="btn-arrow" aria-label="More options">
          <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
            <path d="M7 10l5 5 5-5H7z"/>
          </svg>
        </button>
        <button class="btn-report" type="button" aria-label="Report this book">Report</button>
      </div>
      <p class="author">Author: Geeks for Geeks</p>
    </div>
  </header>

  <section class="section" aria-label="Preview images of the book">
    <h2>Preview</h2>
    <div class="preview-gallery" tabindex="0">
      <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=400&q=80" alt="Preview page 1 of The Great Adventure" />
      <img src="https://images.unsplash.com/photo-1544716278-fd38580f106e?auto=format&fit=crop&w=400&q=80" alt="Preview page 2 of The Great Adventure" />
      <img src="https://images.unsplash.com/photo-1590608897129-79d0b03ecbde?auto=format&fit=crop&w=400&q=80" alt="Preview page 3 of The Great Adventure" />
      <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?auto=format&fit=crop&w=400&q=80" alt="Preview page 4 of The Great Adventure" />
    </div>
  </section>

  <section class="section" aria-label="About the book The Great Adventure">
    <h2>About this book</h2>
    <p class="about-text">
      "The Great Adventure" is an enthralling journey that explores themes of courage, friendship, and self-discovery. Written by the Geeks for Geeks team, this book weaves a tale that pulls readers into a vivid world full of memorable characters and unexpected twists. Perfect for fans of gripping storytelling and emotional depth.
    </p>
  </section>

  <section class="section" aria-label="Book ratings and reviews">
    <h2>Ratings and reviews</h2>
    <div class="ratings" aria-live="polite" aria-atomic="true">
      <div class="stars" aria-hidden="true" role="img" aria-label="4 out of 5 stars rating">
        <svg><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
        <svg><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
        <svg><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
        <svg><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
        <svg class="empty"><path d="M12 15.4l-3.76 2.27 1-4.28-3.32-2.87 4.38-.38L12 6.1l1.71 4.04 4.38.38-3.32 2.87 1 4.28z"/></svg>
      </div>
      <div class="rating-score" aria-label="Rating score">4.0</div>
      <div class="rating-count" aria-label="Total number of ratings">(1,234 ratings)</div>
    </div>
  </section>

  <section class="section" aria-label="Notes and support information for The Great Adventure">
    <h2>Notes &amp; Support</h2>
    <p class="notes-text">
      If you experience any issues with this book or its content, please visit our 
      <a href="https://example.com/support" target="_blank" rel="noopener" class="notes-link">Support Page</a> for assistance and further information.
    </p>
    <p class="notes-text">We appreciate your feedback to help us improve.</p>
  </section>

</div>
