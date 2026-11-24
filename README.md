# book
<!DOCTYPE html>
<!--
  Azure Bay Hotel &amp; Resort — Stay Above the Ordinary - student HTML & CSS project
  This ONE file contains both the HTML structure and the full CSS (<style> block).
  Photos are loaded from the "images" folder next to this file - keep the images
  folder in the same directory (and you may rename this file to index.html).
-->

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Azure Bay Hotel &amp; Resort — Stay Above the Ordinary</title>
<meta name="description" content="Azure Bay Hotel & Resort offers luxury rooms, bay-view suites, a rooftop infinity pool and warm hospitality — book your perfect stay.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@600;700&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ============================================================
   Azure Bay Hotel & Resort
   Pure HTML + CSS student project · Responsive (desktop / tablet / mobile)
   ============================================================ */
:root {
  --bg: #f6f9fb;
  --surface: #ffffff;
  --ink: #13293d;
  --ink-soft: #5b7083;
  --navy: #123a5c;
  --teal: #1f8a8a;
  --gold: #c9a24b;
  --gold-dark: #b18c3a;
  --line: #dbe6ee;
  --shadow: 0 12px 32px rgba(18, 57, 92, .12);
  --radius: 14px;
  --font-head: "Cormorant Garamond", Georgia, serif;
  --font-body: "Jost", "Segoe UI", system-ui, sans-serif;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { font-family: var(--font-body); background: var(--bg); color: var(--ink); line-height: 1.65; }
img { max-width: 100%; display: block; }
.container { width: min(1160px, 92%); margin-inline: auto; }
h1, h2, h3 { font-family: var(--font-head); line-height: 1.2; }
h2 { font-size: clamp(1.8rem, 3vw, 2.5rem); }

/* ---------- buttons ---------- */
.btn {
  display: inline-block; padding: .8rem 1.7rem; border-radius: 999px;
  font-weight: 600; font-size: .95rem; text-decoration: none; border: 2px solid transparent;
  cursor: pointer; transition: transform .18s ease, box-shadow .18s ease, background .18s ease;
}
.btn-gold { background: var(--gold); color: #1d1508; }
.btn-gold:hover { background: var(--gold-dark); transform: translateY(-2px); box-shadow: var(--shadow); }
.btn-navy { background: var(--navy); color: #fff; }
.btn-navy:hover { background: #0c2a44; transform: translateY(-2px); box-shadow: var(--shadow); }
.btn-sm { padding: .5rem 1.2rem; font-size: .85rem; }
.btn-block { width: 100%; text-align: center; }

/* ---------- navbar ---------- */
.navbar {
  position: sticky; top: 0; z-index: 50;
  background: rgba(246, 249, 251, .94); backdrop-filter: blur(8px);
  border-bottom: 1px solid var(--line);
}
.nav-inner { display: flex; align-items: center; justify-content: space-between; min-height: 70px; }
.brand { font-family: var(--font-head); font-size: 1.6rem; font-weight: 700; color: var(--navy); text-decoration: none; letter-spacing: 1px; }
.brand span { color: var(--gold); }
.nav-links { display: flex; align-items: center; gap: 1.4rem; }
.nav-links a { color: var(--ink); text-decoration: none; font-weight: 500; font-size: .95rem; }
.nav-links a:hover { color: var(--teal); }
.nav-toggle { display: none; }
.nav-burger { display: none; cursor: pointer; width: 30px; height: 24px; position: relative; }
.nav-burger span, .nav-burger span::before, .nav-burger span::after {
  content: ""; position: absolute; left: 0; width: 100%; height: 3px;
  background: var(--navy); border-radius: 2px; transition: .25s;
}
.nav-burger span { top: 10px; }
.nav-burger span::before { top: -8px; }
.nav-burger span::after { top: 8px; }

/* ---------- hero ---------- */
.hero { min-height: 88vh; display: flex; align-items: flex-end; background: url("images/hero.jpg") center/cover no-repeat; }
.hero-overlay { width: 100%; background: linear-gradient(180deg, rgba(9, 28, 45, .55), rgba(9, 28, 45, .82)); }
.hero-content { padding: 4.5rem 0 5rem; color: #fff; max-width: 860px; }
.hero-kicker { color: var(--gold); letter-spacing: 3px; font-size: .8rem; text-transform: uppercase; margin-bottom: .9rem; }
.hero h1 { font-size: clamp(2.4rem, 5vw, 3.8rem); margin-bottom: .9rem; }
.hero-sub { color: #e3edf5; font-weight: 300; margin-bottom: 2.2rem; max-width: 560px; }

/* booking search bar */
.search-bar {
  background: rgba(255, 255, 255, .96); border-radius: 14px; padding: 1.1rem;
  display: grid; grid-template-columns: repeat(4, 1fr) auto; gap: .9rem; align-items: end;
  box-shadow: var(--shadow);
}
.search-bar label { font-size: .72rem; text-transform: uppercase; letter-spacing: 1px; color: var(--ink-soft); font-weight: 600; }
.search-bar input, .search-bar select {
  width: 100%; margin-top: .3rem; padding: .65rem .7rem; border: 1px solid var(--line);
  border-radius: 9px; font-family: inherit; font-size: .88rem; color: var(--ink); background: var(--bg);
}
.search-bar input:focus, .search-bar select:focus { outline: none; border-color: var(--teal); }
.search-bar .btn { white-space: nowrap; }

/* ---------- welcome strip ---------- */
.section-sm { padding: 2.5rem 0; background: var(--surface); border-bottom: 1px solid var(--line); }
.welcome-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 1rem; text-align: center; }
.welcome-stat strong { display: block; font-family: var(--font-head); font-size: 1.7rem; color: var(--teal); }
.welcome-stat span { font-size: .8rem; color: var(--ink-soft); text-transform: uppercase; letter-spacing: 1px; }

/* ---------- sections ---------- */
.section { padding: 5.5rem 0; }
.section-head { text-align: center; max-width: 620px; margin: 0 auto 3rem; }
.kicker { color: var(--teal); font-weight: 600; letter-spacing: 2px; text-transform: uppercase; font-size: .8rem; margin-bottom: .5rem; }
.section-sub { color: var(--ink-soft); margin-top: .8rem; }

/* ---------- rooms ---------- */
.rooms-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.8rem; }
.room-card {
  background: var(--surface); border: 1px solid var(--line); border-radius: var(--radius);
  overflow: hidden; box-shadow: 0 6px 18px rgba(18, 57, 92, .07);
  transition: transform .2s ease, box-shadow .2s ease; position: relative;
}
.room-card:hover { transform: translateY(-6px); box-shadow: var(--shadow); }
.room-card img { height: 230px; width: 100%; object-fit: cover; }
.room-body { padding: 1.3rem 1.4rem 1.5rem; }
.room-top { display: flex; justify-content: space-between; align-items: baseline; gap: .6rem; margin-bottom: .5rem; }
.room-top h3 { font-size: 1.35rem; }
.price { color: var(--teal); font-weight: 700; font-size: 1.05rem; white-space: nowrap; }
.price span { font-size: .72rem; color: var(--ink-soft); font-weight: 400; }
.room-body p { font-size: .88rem; color: var(--ink-soft); margin-bottom: 1rem; }
.amenities { list-style: none; display: flex; flex-wrap: wrap; gap: .4rem; margin-bottom: 1.2rem; }
.amenities li {
  font-size: .72rem; background: var(--bg); border: 1px solid var(--line);
  color: var(--ink-soft); padding: .22rem .65rem; border-radius: 999px;
}
.featured { border: 2px solid var(--gold); }
.ribbon {
  position: absolute; top: 16px; left: 16px; z-index: 2; background: var(--gold);
  color: #1d1508; font-size: .72rem; font-weight: 700; letter-spacing: 1px;
  text-transform: uppercase; padding: .3rem .8rem; border-radius: 999px;
}

/* ---------- facilities ---------- */
.facilities { background: var(--navy); color: #fff; }
.facilities .kicker { color: var(--gold); }
.facility-gallery { display: grid; grid-template-columns: repeat(4, 1fr); grid-auto-rows: 180px; gap: 1rem; margin-bottom: 2.5rem; }
.fg-item { position: relative; border-radius: var(--radius); overflow: hidden; }
.fg-item.tall { grid-row: span 2; }
.fg-item img { width: 100%; height: 100%; object-fit: cover; transition: transform .35s ease; }
.fg-item:hover img { transform: scale(1.06); }
.fg-item figcaption {
  position: absolute; left: 0; right: 0; bottom: 0; padding: 1.6rem 1rem .8rem;
  background: linear-gradient(180deg, transparent, rgba(9, 28, 45, .85));
  font-size: .85rem; font-weight: 500; letter-spacing: .5px;
}
.facility-list {
  list-style: none; display: grid; grid-template-columns: repeat(4, 1fr); gap: .8rem 1.6rem;
}
.facility-list li {
  background: rgba(255, 255, 255, .07); border: 1px solid rgba(255, 255, 255, .16);
  border-radius: 10px; padding: .7rem 1rem; font-size: .9rem; text-align: center;
}
.facility-list li::before { content: "— "; color: var(--gold); }

/* ---------- reviews ---------- */
.reviews-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.6rem; }
.review-card { background: var(--surface); border: 1px solid var(--line); border-radius: var(--radius); padding: 1.7rem; box-shadow: 0 6px 18px rgba(18, 57, 92, .07); }
.stars { color: var(--gold); letter-spacing: 3px; margin-bottom: .8rem; }
.review-card blockquote { font-size: .92rem; color: var(--ink-soft); font-style: italic; }
.review-card figcaption { display: flex; align-items: center; gap: .9rem; margin-top: 1.3rem; font-size: .85rem; }
.review-card small { color: var(--ink-soft); }
.avatar { width: 46px; height: 46px; border-radius: 50%; display: inline-flex; flex-shrink: 0; align-items: center; justify-content: center; color: #fff; font-weight: 700; }
.av-1 { background: var(--teal); }
.av-2 { background: var(--navy); }
.av-3 { background: var(--gold); }

/* ---------- booking ---------- */
.booking { background: var(--surface); }
.booking-grid { display: grid; grid-template-columns: .9fr 1.1fr; gap: 3rem; align-items: stretch; }
.booking-media { display: flex; flex-direction: column; gap: 1.4rem; }
.booking-media img { border-radius: var(--radius); box-shadow: var(--shadow); height: 300px; width: 100%; object-fit: cover; }
.booking-assurance { background: var(--bg); border: 1px solid var(--line); border-radius: var(--radius); padding: 1.5rem; flex: 1; }
.booking-assurance h3 { margin-bottom: .5rem; }
.booking-assurance p { font-size: .88rem; color: var(--ink-soft); margin-bottom: 1rem; }
.booking-assurance ul { list-style: none; display: grid; gap: .4rem; }
.booking-assurance li { font-size: .86rem; }
.booking-assurance li::before { content: "✓ "; color: var(--teal); font-weight: 700; }
.booking-form { background: var(--bg); border: 1px solid var(--line); border-radius: var(--radius); padding: 2.2rem; box-shadow: var(--shadow); }
.booking-form h2 { margin-bottom: 1.5rem; }
.booking-form label { display: block; font-size: .85rem; font-weight: 500; margin-bottom: 1rem; }
.booking-form input, .booking-form select, .booking-form textarea {
  width: 100%; margin-top: .35rem; padding: .7rem .9rem; border: 1px solid var(--line);
  border-radius: 10px; background: #fff; font-family: inherit; font-size: .9rem; color: var(--ink);
}
.booking-form input:focus, .booking-form select:focus, .booking-form textarea:focus {
  outline: none; border-color: var(--teal); box-shadow: 0 0 0 3px rgba(31, 138, 138, .12);
}
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
.form-row label { margin-bottom: 0; }
.form-row + label, .form-row + .form-row { margin-top: 1rem; }
.booking-form textarea { margin-top: 1rem; }
.booking-form .btn { margin-top: .5rem; }
.form-note { font-size: .78rem; color: var(--ink-soft); margin-top: .8rem; text-align: center; }

/* ---------- footer ---------- */
.footer { background: #0c2236; color: #c8d8e5; padding: 3.5rem 0 0; }
.footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 2.5rem; padding-bottom: 2.5rem; }
.footer-brand { font-size: 1.5rem; color: #fff; margin-bottom: .7rem; }
.footer-brand span { color: var(--gold); }
.footer h4 { color: #fff; margin-bottom: .9rem; font-family: var(--font-body); font-weight: 600; font-size: .95rem; }
.footer-grid a { display: block; color: #c8d8e5; text-decoration: none; font-size: .88rem; margin-bottom: .5rem; }
.footer-grid a:hover { color: var(--gold); }
.footer-grid p { font-size: .88rem; }
.footer-bottom { border-top: 1px solid rgba(255, 255, 255, .12); padding: 1.2rem 0; }
.footer-bottom p { font-size: .78rem; color: #8aa2b5; text-align: center; }

/* ---------- responsive ---------- */
@media (max-width: 980px) {
  .rooms-grid { grid-template-columns: repeat(2, 1fr); }
  .reviews-grid { grid-template-columns: 1fr; }
  .facility-gallery { grid-template-columns: repeat(2, 1fr); grid-auto-rows: 170px; }
  .facility-list { grid-template-columns: repeat(2, 1fr); }
  .welcome-grid { grid-template-columns: repeat(3, 1fr); gap: 1.5rem; }
  .booking-grid { grid-template-columns: 1fr; }
  .search-bar { grid-template-columns: 1fr 1fr; }
  .search-bar .btn { grid-column: 1 / -1; }
}
@media (max-width: 640px) {
  .section { padding: 3.5rem 0; }
  .rooms-grid, .facility-gallery, .facility-list, .welcome-grid { grid-template-columns: 1fr; }
  .facility-gallery { grid-auto-rows: 200px; }
  .fg-item.tall { grid-row: span 1; }
  .footer-grid { grid-template-columns: 1fr; }
  .form-row { grid-template-columns: 1fr; }
  .hero { min-height: 74vh; }

  .nav-burger { display: block; }
  .nav-links {
    display: none; position: absolute; top: 70px; left: 0; right: 0;
    background: #fff; flex-direction: column; align-items: stretch; gap: 0;
    border-bottom: 1px solid var(--line); box-shadow: var(--shadow); padding: .6rem 4%;
  }
  .nav-links a { padding: .85rem .4rem; border-bottom: 1px solid var(--line); }
  .nav-links a:last-child { border-bottom: none; margin-top: .5rem; text-align: center; }
  .nav-toggle:checked ~ .nav-links { display: flex; }
  .nav-toggle:checked + .nav-burger span { background: transparent; }
  .nav-toggle:checked + .nav-burger span::before { transform: rotate(45deg); top: 0; }
  .nav-toggle:checked + .nav-burger span::after { transform: rotate(-45deg); top: 0; }
}

</style>
</head>
<body>

<!-- ===== Navigation ===== -->
<header class="navbar">
  <div class="container nav-inner">
    <a href="#home" class="brand">Azure <span>Bay</span></a>
    <input type="checkbox" id="nav-toggle" class="nav-toggle">
    <label for="nav-toggle" class="nav-burger" aria-label="Toggle menu"><span></span></label>
    <nav class="nav-links">
      <a href="#home">Home</a>
      <a href="#rooms">Rooms &amp; Suites</a>
      <a href="#facilities">Facilities</a>
      <a href="#reviews">Reviews</a>
      <a href="#booking">Book Now</a>
      <a href="#booking" class="btn btn-gold btn-sm">Reserve</a>
    </nav>
  </div>
</header>

<!-- ===== Hero with booking search ===== -->
<section id="home" class="hero">
  <div class="hero-overlay">
    <div class="container hero-content">
      <p class="hero-kicker">★ ★ ★ ★ ★ &nbsp;Luxury Beachfront Resort</p>
      <h1>Stay Above the Ordinary</h1>
      <p class="hero-sub">Wake up to endless bay views, unwind at the rooftop infinity pool
        and let our team take care of every detail of your holiday.</p>

      <form class="search-bar" action="#booking" method="get">
        <label>Check In <input type="date" name="in"></label>
        <label>Check Out <input type="date" name="out"></label>
        <label>Guests
          <select name="guests">
            <option>1 Adult</option><option selected>2 Adults</option>
            <option>2 Adults, 1 Child</option><option>Family (4+)</option>
          </select>
        </label>
        <label>Room Type
          <select name="room">
            <option selected>Any room</option><option>Classic Queen</option>
            <option>Deluxe Garden</option><option>Executive City</option>
            <option>Bayview Suite</option><option>Family Retreat</option>
          </select>
        </label>
        <button type="submit" class="btn btn-gold">Check Availability</button>
      </form>
    </div>
  </div>
</section>

<!-- ===== Welcome strip ===== -->
<section class="welcome section-sm">
  <div class="container welcome-grid">
    <div class="welcome-stat"><strong>4.9★</strong><span>Guest rating</span></div>
    <div class="welcome-stat"><strong>210</strong><span>Rooms &amp; suites</span></div>
    <div class="welcome-stat"><strong>3</strong><span>Outdoor pools</span></div>
    <div class="welcome-stat"><strong>24/7</strong><span>Room service</span></div>
    <div class="welcome-stat"><strong>150m</strong><span>Private beach</span></div>
  </div>
</section>

<!-- ===== Rooms ===== -->
<section id="rooms" class="section rooms">
  <div class="container">
    <div class="section-head">
      <p class="kicker">Rooms &amp; Suites</p>
      <h2>Find Your Perfect Room</h2>
      <p class="section-sub">Every room includes free Wi-Fi, breakfast buffet, air
        conditioning and a daily housekeeping service.</p>
    </div>
    <div class="rooms-grid">
      <article class="room-card">
        <img src="images/room-standard.jpg" alt="Classic Queen room with canopy bed">
        <div class="room-body">
          <div class="room-top"><h3>Classic Queen</h3><span class="price">₹3,999<span>/night</span></span></div>
          <p>A calm, light-filled retreat with a queen canopy bed and garden views.</p>
          <ul class="amenities"><li>28 m²</li><li>Queen bed</li><li>Free Wi-Fi</li><li>Breakfast</li></ul>
          <a href="#booking" class="btn btn-navy btn-sm btn-block">Book This Room</a>
        </div>
      </article>

      <article class="room-card">
        <img src="images/room-deluxe.jpg" alt="Deluxe Garden room with cosy window seating">
        <div class="room-body">
          <div class="room-top"><h3>Deluxe Garden</h3><span class="price">₹5,499<span>/night</span></span></div>
          <p>Spacious room opening onto the palm gardens, with a cosy reading nook.</p>
          <ul class="amenities"><li>36 m²</li><li>King bed</li><li>Garden view</li><li>Breakfast</li></ul>
          <a href="#booking" class="btn btn-navy btn-sm btn-block">Book This Room</a>
        </div>
      </article>

      <article class="room-card">
        <img src="images/room-executive.jpg" alt="Executive City room in dark elegant tones">
        <div class="room-body">
          <div class="room-top"><h3>Executive City</h3><span class="price">₹6,999<span>/night</span></span></div>
          <p>Sleek, dark-wood elegance on the top floors with skyline and bay views.</p>
          <ul class="amenities"><li>42 m²</li><li>King bed</li><li>Lounge access</li><li>Airport pickup</li></ul>
          <a href="#booking" class="btn btn-navy btn-sm btn-block">Book This Room</a>
        </div>
      </article>

      <article class="room-card featured">
        <span class="ribbon">Guest Favourite</span>
        <img src="images/room-suite.jpg" alt="Bayview Suite with soft beige luxury interior">
        <div class="room-body">
          <div class="room-top"><h3>Bayview Suite</h3><span class="price">₹9,499<span>/night</span></span></div>
          <p>A generous suite with a separate living area and a private balcony over the bay.</p>
          <ul class="amenities"><li>58 m²</li><li>King bed</li><li>Balcony</li><li>Free spa session</li></ul>
          <a href="#booking" class="btn btn-gold btn-sm btn-block">Book This Room</a>
        </div>
      </article>

      <article class="room-card">
        <img src="images/room-family.jpg" alt="Family Retreat with classic four poster bed">
        <div class="room-body">
          <div class="room-top"><h3>Family Retreat</h3><span class="price">₹7,999<span>/night</span></span></div>
          <p>Two connected bedrooms, a lounge corner and extra beds for the kids.</p>
          <ul class="amenities"><li>64 m²</li><li>Sleeps 5</li><li>Kids amenity kit</li><li>Breakfast</li></ul>
          <a href="#booking" class="btn btn-navy btn-sm btn-block">Book This Room</a>
        </div>
      </article>
    </div>
  </div>
</section>

<!-- ===== Facilities ===== -->
<section id="facilities" class="section facilities">
  <div class="container">
    <div class="section-head">
      <p class="kicker">Facilities</p>
      <h2>Everything You Need, and More</h2>
    </div>
    <div class="facility-gallery">
      <figure class="fg-item tall"><img src="images/facility-cliffpool.jpg" alt="Cliffside infinity pool over the sea"><figcaption>Cliffside Infinity Pool</figcaption></figure>
      <figure class="fg-item"><img src="images/pool-sunset.jpg" alt="Sunset lap pool lined with palm trees"><figcaption>Sunset Lap Pool</figcaption></figure>
      <figure class="fg-item"><img src="images/pool-garden.jpg" alt="Garden pool with shaded cabanas"><figcaption>Garden Cabana Pool</figcaption></figure>
      <figure class="fg-item"><img src="images/villa-pool.jpg" alt="Private villa pool at dusk"><figcaption>Private Villa Pools</figcaption></figure>
    </div>
    <ul class="facility-list">
      <li>Rooftop Bar &amp; Grill</li>
      <li>Full-Service Spa</li>
      <li>Fitness Studio</li>
      <li>3 Outdoor Pools</li>
      <li>Private Beach Access</li>
      <li>Kids Club</li>
      <li>Conference Rooms</li>
      <li>Free Valet Parking</li>
    </ul>
  </div>
</section>

<!-- ===== Reviews ===== -->
<section id="reviews" class="section reviews">
  <div class="container">
    <div class="section-head">
      <p class="kicker">Guest Reviews</p>
      <h2>Loved by Guests Worldwide</h2>
    </div>
    <div class="reviews-grid">
      <figure class="review-card">
        <div class="stars">★★★★★</div>
        <blockquote>"The bayview suite was worth every rupee. Watching the sunset from
          the private balcony with room service was the highlight of our trip."</blockquote>
        <figcaption><span class="avatar av-1">SK</span>
          <span><strong>Sneha Kapoor</strong><br><small>Family holiday · Pune</small></span></figcaption>
      </figure>
      <figure class="review-card">
        <div class="stars">★★★★★</div>
        <blockquote>"Impeccable service. The team remembered our names, arranged a
          surprise cake for my mother's birthday and the breakfast spread is huge."</blockquote>
        <figcaption><span class="avatar av-2">AV</span>
          <span><strong>Arjun Verma</strong><br><small>Business traveller · Delhi</small></span></figcaption>
      </figure>
      <figure class="review-card">
        <div class="stars">★★★★☆</div>
        <blockquote>"Beautiful property and the cliff pool is stunning. Only tip —
          book spa slots early because evenings fill up fast."</blockquote>
        <figcaption><span class="avatar av-3">MT</span>
          <span><strong>Meera Iyer</strong><br><small>Couple getaway · Chennai</small></span></figcaption>
      </figure>
    </div>
  </div>
</section>

<!-- ===== Booking ===== -->
<section id="booking" class="section booking">
  <div class="container booking-grid">
    <div class="booking-media">
      <img src="images/room-deluxe.jpg" alt="Deluxe garden room ready for check-in">
      <div class="booking-assurance">
        <h3>Best Rate Promise</h3>
        <p>Book directly with us and enjoy free cancellation up to 48 hours before
          check-in, plus a complimentary welcome drink for every guest.</p>
        <ul><li>Free cancellation*</li><li>No prepayment needed</li><li>Welcome drink included</li></ul>
      </div>
    </div>
    <form class="booking-form" action="#" method="post">
      <p class="kicker">Reservations</p>
      <h2>Book Your Stay</h2>
      <div class="form-row">
        <label>Full Name <input type="text" name="name" placeholder="e.g. Ishita Rao" required></label>
        <label>Email <input type="email" name="email" placeholder="you@example.com" required></label>
      </div>
      <div class="form-row">
        <label>Check In <input type="date" name="in" required></label>
        <label>Check Out <input type="date" name="out" required></label>
      </div>
      <div class="form-row">
        <label>Room Type
          <select name="room">
            <option>Classic Queen</option><option>Deluxe Garden</option>
            <option>Executive City</option><option selected>Bayview Suite</option>
            <option>Family Retreat</option>
          </select>
        </label>
        <label>Guests
          <select name="guests"><option>1</option><option selected>2</option><option>3</option><option>4+</option></select>
        </label>
      </div>
      <label>Special Requests
        <textarea name="note" rows="3" placeholder="Airport pickup, high floor, honeymoon setup…"></textarea>
      </label>
      <button type="submit" class="btn btn-gold btn-block">Request Booking</button>
      <p class="form-note">Our reservation desk will confirm availability by email within one hour.</p>
    </form>
  </div>
</section>

<!-- ===== Footer ===== -->
<footer class="footer">
  <div class="container footer-grid">
    <div>
      <p class="brand footer-brand">Azure <span>Bay</span></p>
      <p>Bayfront Road, Sunny Shores,<br>Kerala 682001, India<br>+91 98470 11223 · stay@azurebay.example</p>
    </div>
    <div>
      <h4>Explore</h4>
      <a href="#rooms">Rooms &amp; Suites</a>
      <a href="#facilities">Facilities</a>
      <a href="#reviews">Guest Reviews</a>
    </div>
    <div>
      <h4>Plan</h4>
      <a href="#booking">Book Your Stay</a>
      <a href="#booking">Offers &amp; Packages</a>
      <a href="#home">Back to Top</a>
    </div>
  </div>
  <div class="container footer-bottom">
    <p>© 2026 Azure Bay Hotel &amp; Resort · Student HTML &amp; CSS Project · Images for educational use</p>
  </div>
</footer>

</body>
</html>
