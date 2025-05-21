# The Great Adventure - Book Landing Page (Old Play Store Android 5 Style)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>The Great Adventure - Old Play Store Style</title>
  <style>
    /* Android 5 Lollipop Play Store style inspired fonts and colors */
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background: #f5f5f5;
      color: #212121;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    a {
      color: #3DDC84;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover, a:focus {
      color: #2ca364;
      text-decoration: underline;
      outline: none;
    }

    /* Container max width */
    .container {
      max-width: 720px;
      margin: 32px auto 64px;
      padding: 0 16px;
    }

    /* Hero Banner */
    .hero {
      position: relative;
      background: url('https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=1300&q=80') center/cover no-repeat;
      height: 280px;
      border-radius: 2px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.26);
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      padding: 24px 32px 32px;
      color: white;
    }
    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(0,0,0,0.6), transparent 70%);
      border-radius: 2px;
      z-index: 0;
    }
    .hero-content {
      position: relative;
      z-index: 1;
    }

    .hero-title {
      font-weight: 500;
      font-size: 2.8rem;
      letter-spacing: 0.02em;
      margin-bottom: 8px;
      text-shadow: 0 1px 2px rgba(0,0,0,0.5);
      user-select: none;
    }
    .hero-subtitle {
      font-weight: 400;
      font-size: 1.1rem;
      color: #cfd8dc;
      margin-bottom: 24px;
      user-select: none;
    }

    /* Buttons container row */
    .button-row {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    /* Material style flat button */
    button, a.button {
      font-size: 1rem;
      font-weight: 500;
      padding: 10px 20px;
      border-radius: 2px;
      border: none;
      cursor: pointer;
      user-select: none;
      text-align: center;
      white-space: nowrap;
      text-decoration: none;
      transition: box-shadow 0.2s ease, background-color 0.2s ease;
      box-shadow: 0 2px 2px rgba(0,0,0,0.14);
      background-color: #3DDC84;
      color: white;
      display: inline-flex;
      align-items: center;
      justify-content: center;
    }
    button:hover, a.button:hover, button:focus, a.button:focus {
      background-color: #2ca364;
      box-shadow: 0 4px 5px rgba(0,0,0,0.26);
      outline: none;
      text-decoration: none;
    }
    button:focus-visible, a.button:focus-visible {
      outline: 2px solid #2ca364;
      outline-offset: 2px;
    }

    /* Small icon button */
    .icon-button {
      background-color: white;
      padding: 0;
      width: 36px;
      height: 36px;
      min-width: 36px;
      box-shadow: 0 2px 2px rgba(0,0,0,0.14);
      border-radius: 2px;
      color: #666;
      justify-content: center;
    }
    .icon-button:hover, .icon-button:focus {
      background-color: #e0f2f1;
      color: #2ca364;
      box-shadow: 0 4px 5px rgba(0,0,0,0.26);
      outline: none;
    }
    .icon-button svg {
      width: 18px;
      height: 18px;
      fill: currentColor;
      user-select: none;
    }

    /* Report button text */
    .report-button {
      background: none;
      box-shadow: none;
      color: #3DDC84;
      font-weight: 500;
      font-size: 1rem;
      padding: 10px 12px;
      border-radius: 2px;
      border: none;
      cursor: pointer;
      user-select: none;
      transition: background-color 0.2s ease;
    }
    .report-button:hover, .report-button:focus {
      background-color: #e0f2f1;
      outline: none;
      text-decoration: none;
      color: #2ca364;
    }
    .report-button:focus-visible {
      outline: 2px solid #2ca364;
      outline-offset: 2px;
    }

    /* Author */
    .author-text {
      color: #90a4ae;
      font-size: 1rem;
      margin-top: 12px;
      user-select: none;
    }

    /* Card sections */
    section {
      background: white;
      border-radius: 2px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.12);
      padding: 24px 32px;
      margin-top: 32px;
    }

    h2 {
      margin-top: 0;
      margin-bottom: 20px;
      font-weight: 500;
      font-size: 1.5rem;
      color: #212121;
      user-select: none;
    }

    /* Preview gallery */
    .preview-gallery {
      display: flex;
      gap: 16px;
      overflow-x: auto;
      padding-bottom: 12px;
    }
    .preview-gallery img {
      height: 220px;
      border-radius: 2px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.2);
      flex-shrink: 0;
      cursor: pointer;
      transition: box-shadow 0.3s ease, transform 0.3s ease;
      user-select: none;
    }
    .preview-gallery img:hover, .preview-gallery img:focus {
      box-shadow: 0 6px 20px rgba(0,0,0,0.3);
      transform: scale(1.05);
      outline: none;
    }

    /* About text */
    .about-text {
      color: #424242;
      font-size: 1.1rem;
      line-height: 1.5;
      user-select: text;
    }

    /* Ratings */
    .ratings {
      display: flex;
      align-items: center;
      gap: 12px;
      user-select: none;
    }
    .stars {
      display: flex;
    }
    svg.star {
      width: 22px;
      height: 22px;
      fill: #f4c20d;
      flex-shrink: 0;
    }
    svg.star.empty {
      fill: #cfd8dc;
    }
    .rating-score {
      font-weight: 500;
      font-size: 1.25rem;
      color: #212121;
    }
    .rating-count {
      font-size: 0.95rem;
      color: #607d8b;
    }

    /* Notes / Support */
    .notes-text {
      font-size: 1rem;
      line-height: 1.45;
      color: #424242;
      user-select: text;
    }
    .notes-link {
      color: #3DDC84;
    }
    .notes-link:hover, .notes-link:focus {
      color: #2ca364;
      text-decoration: underline;
      outline: none;
    }

    /* Responsive */
    @media (max-width: 600px) {
      .hero {
        height: 240px;
        padding: 20px 16px;
      }
      .hero-title {
        font-size: 2rem;
      }
      .hero-subtitle {
        font-size: 0.95rem;
      }
      .button-row {
        flex-wrap: wrap;
        gap: 8px;
      }
      .read-button {
        padding: 8px 16px;
        font-size: 0.95rem;
      }
      .icon-button {
        width: 32px;
        height: 32px;
      }
      .preview-gallery img {
        height: 140px;
      }
      section {
        padding: 20px 20px;
        margin-top: 24px;
      }
    }
  </style>
</head>
<body>
  <div class="container" role="main" aria-label="Book landing page - The Great Adventure">

    <header class="hero" aria-label="Book cover image and title">
      <div class="hero-content">
        <h1 class="hero-title">The Great Adventure</h1>
        <p class="hero-subtitle">By Geeks for Geeks</p>
        <div class="button-row">
          <a href="https://example.com/read-the-great-adventure" target="_blank" rel="noopener" class="button read-button" aria-label="Read The Great Adventure book">Read</a>
          <button class="icon-button" aria-label="More options">
            <svg viewBox="0 0 24 24" focusable="false" aria-hidden="true">
              <path d="M7 10l5 5 5-5H7z"/>
            </svg>
          </button>
          <button class="report-button" type="button" aria-label="Report this book">Report</button>
        </div>
        <p class="author-text">Author: Geeks for Geeks</p>
      </div>
    </header>

    <section aria-label="Preview images of the book">
      <h2>Preview</h2>
      <div class="preview-gallery" tabindex="0">
        <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=400&q=80" alt="Preview page 1 of The Great Adventure" />
        <img src="https://images.unsplash.com/photo-1544716278-fd38580f106e?auto=format&fit=crop&w=400&q=80" alt="Preview page 2 of The Great Adventure" />
        <img src="https://images.unsplash.com/photo-1590608897129-79d0b03ecbde?auto=format&fit=crop&w=400&q=80" alt="Preview page 3 of The Great Adventure" />
        <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?auto=format&fit=crop&w=400&q=80" alt="Preview page 4 of The Great Adventure" />
      </div>
    </section>

    <section aria-label="About the book The Great Adventure">
      <h2>About this book</h2>
      <p class="about-text">
        "The Great Adventure" is an enthralling journey that explores themes of courage, friendship, and self-discovery. Written by the Geeks for Geeks team, this book weaves a tale that pulls readers into a vivid world full of memorable characters and unexpected twists. Perfect for fans of gripping storytelling and emotional depth.
      </p>
    </section>

    <section aria-label="Book ratings and reviews">
      <h2>Ratings and reviews</h2>
      <div class="ratings" aria-live="polite" aria-atomic="true">
        <div class="stars" aria-hidden="true" role="img" aria-label="4 out of 5 stars rating">
          <svg class="star" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
          <svg class="star" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
          <svg class="star" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
          <svg class="star" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21 16.54 13.97 22 9.24l-7.19-.62L12 2 9.19 8.62 2 9.24l5.46 4.73L5.82 21z"/></svg>
          <svg class="star empty" viewBox="0 0 24 24"><path d="M12 15.4l-3.76 2.27 1-4.28-3.32-2.87 4.38-.38L12 6.1l1.71 4.04 4.38.38-3.32 2.87 1 4.28z"/></svg>
        </div>
        <div class="rating-score" aria-label="Rating score">4.0</div>
        <div class="rating-count" aria-label="Total number of ratings">(1,234 ratings)</div>
      </div>
    </section>

    <section aria-label="Notes and support information for The Great Adventure">
      <h2>Notes &amp; Support</h2>
      <p class="notes-text">
        If you experience any issues with this book or its content, please visit our 
        <a href="https://example.com/support" target="_blank" rel="noopener" class="notes-link">Support Page</a> for assistance and further information.
      </p>
      <p class="notes-text">We appreciate your feedback to help us improve.</p>
    </section>

  </div>
</body>
</html>
