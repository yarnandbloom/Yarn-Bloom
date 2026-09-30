<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Yarn & Bloom - Handmade Crochet</title>
  <style>
    :root {
      --bg: #faf7f2;
      --card-bg: #ffffff;
      --text: #4a3b32;
      --accent-sage: #87a990;
      --accent-rose: #d88373;
      --accent-yellow: #f4c468;
      --border: #e6dfd3;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
    body { background-color: var(--bg); color: var(--text); padding-bottom: 50px; }

    header {
      background: var(--card-bg);
      border-bottom: 2px dashed var(--accent-sage);
      text-align: center;
      padding: 2rem 1rem;
      position: relative;
    }

    .edit-toggle {
      position: absolute;
      top: 15px;
      right: 15px;
      background: var(--accent-sage);
      color: white;
      border: none;
      padding: 8px 16px;
      border-radius: 20px;
      cursor: pointer;
      font-weight: bold;
    }

    h1 { color: var(--accent-rose); font-size: 2.8rem; margin-bottom: 5px; }
    .tagline { font-style: italic; color: #6b5b52; margin-bottom: 15px; }

    .banner {
      background: var(--accent-yellow);
      padding: 10px;
      font-weight: bold;
      border-radius: 8px;
      display: inline-block;
      margin-top: 10px;
    }

    .container { max-width: 1000px; margin: 30px auto; padding: 0 20px; }

    .pitch-box {
      background: #f1ebd9;
      border: 2px solid #d4c8ad;
      padding: 20px;
      border-radius: 12px;
      margin-bottom: 30px;
      text-align: center;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
    }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 10px rgba(0,0,0,0.04);
      display: flex;
      flex-direction: column;
    }

    .card img {
      width: 100%;
      height: 220px;
      object-fit: cover;
    }

    .card-content { padding: 18px; flex-grow: 1; display: flex; flex-direction: column; justify-content: space-between; }
    .card-title { font-size: 1.3rem; color: var(--accent-rose); margin-bottom: 8px; }
    .card-desc { font-size: 0.95rem; color: #555; margin-bottom: 15px; line-height: 1.4; }
    .card-price { font-weight: bold; color: var(--accent-sage); font-size: 1.1rem; }

    .custom-form {
      background: white;
      border: 2px solid var(--accent-sage);
      padding: 25px;
      border-radius: 12px;
      margin-top: 40px;
    }

    .form-group { margin-bottom: 15px; }
    label { display: block; margin-bottom: 5px; font-weight: bold; }
    input, textarea { width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 6px; }

    button.submit-btn {
      background: var(--accent-rose);
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 6px;
      cursor: pointer;
      font-size: 1rem;
      font-weight: bold;
    }

    [contenteditable="true"] {
      outline: 2px dashed var(--accent-rose);
      background-color: #fff9f8;
    }
  </style>
</head>
<body>

  <header>
    <button class="edit-toggle" onclick="toggleEdit()">Owner Edit Mode: OFF</button>
    <h1 class="editable">🌸 Yarn & Bloom 🌸</h1>
    <p class="tagline editable">Handmade Crochet Apparel, Bags, Accessories & Plushies</p>
    <div class="banner editable">✨ Special Requests Always Welcome! ✨</div>
  </header>

  <div class="container">

    <div class="pitch-box">
      <h3 style="margin-bottom:8px;">Welcome to My Shop!</h3>
      <p class="editable">
        Hi everyone! Welcome to Yarn & Bloom, where everything is 100% handmade with love! 
        I create super cozy beanies, stylish cardigans, durable tote bags, and the cutest plushies and keychains. 
        If you have a specific color or custom idea in mind, I take special requests!
      </p>
    </div>

    <h2 style="margin-bottom: 20px; color: var(--accent-rose);">Our Handmade Collection</h2>
    <div class="gallery">

      <!-- Item 1 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1576871337632-b9aef4c17ab9?auto=format&fit=crop&w=600&q=80" alt="Crochet Beanie">
        <div class="card-content">
          <div>
            <div class="card-title editable">Cozy Ribbed Beanie</div>
            <div class="card-desc editable">Warm, stretchable, hand-stitched beanies made with soft premium yarn.</div>
          </div>
          <div class="card-price editable">$20.00</div>
        </div>
      </div>

      <!-- Item 2 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1434389677669-e08b4cac3105?auto=format&fit=crop&w=600&q=80" alt="Crochet Cardigan">
        <div class="card-content">
          <div>
            <div class="card-title editable">Granny Square Cardigan</div>
            <div class="card-desc editable">Colorful, trendy handmade cardigan sweaters perfect for layering.</div>
          </div>
          <div class="card-price editable">$65.00</div>
        </div>
      </div>

      <!-- Item 3 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=600&q=80" alt="Crochet Tote Bag">
        <div class="card-content">
          <div>
            <div class="card-title editable">Floral Crochet Tote & Shoulder Bag</div>
            <div class="card-desc editable">Durable straps with cute flower square details for everyday wear.</div>
          </div>
          <div class="card-price editable">$32.00</div>
        </div>
      </div>

      <!-- Item 4 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1558679908-541bcf1249ff?auto=format&fit=crop&w=600&q=80" alt="Crochet Plushie">
        <div class="card-content">
          <div>
            <div class="card-title editable">Cutie Bee Plushie</div>
            <div class="card-desc editable">Adorable, squishy amigurumi plushies made with soft chenille yarn.</div>
          </div>
          <div class="card-price editable">$18.00</div>
        </div>
      </div>

      <!-- Item 5 -->
      <div class="card">
        <img src="https://images.unsplash.com/photo-1607604276583-eef5d076aa5f?auto=format&fit=crop&w=600&q=80" alt="Crochet Keychain">
        <div class="card-content">
          <div>
            <div class="card-title editable">Flower Charm Keychain</div>
            <div class="card-desc editable">Mini handcrafted crochet flower charms to attach to bags or keys.</div>
          </div>
          <div class="card-price editable">$8.00</div>
        </div>
      </div>

    </div>

    <!-- Special Request Form -->
    <div class="custom-form">
      <h2 style="color: var(--accent-rose); margin-bottom: 10px;">Request a Custom Order!</h2>
      <p style="margin-bottom: 15px;">Have a specific color, size, or design in mind? Let me know below!</p>
      <form onsubmit="alert('Thank you! Your custom request has been submitted.'); return false;">
        <div class="form-group">
          <label>Your Name</label>
          <input type="text" required placeholder="Jane Doe">
        </div>
        <div class="form-group">
          <label>What item would you like? (Beanie, Cardigan, Tote Bag, Plushie, Keychain)</label>
          <input type="text" required placeholder="e.g. Custom Bee Plushie with pink wings">
        </div>
        <div class="form-group">
          <label>Special Requests / Color Preferences</label>
          <textarea rows="4" placeholder="Tell me about colors, sizing, or special ideas..."></textarea>
        </div>
        <button type="submit" class="submit-btn">Send Custom Request</button>
      </form>
    </div>

  </div>

  <script>
    let editMode = false;
    function toggleEdit() {
      editMode = !editMode;
      const editables = document.querySelectorAll('.editable');
      const btn = document.querySelector('.edit-toggle');
      
      editables.forEach(el => {
        el.contentEditable = editMode;
      });

      if (editMode) {
        btn.innerText = "Owner Edit Mode: ON";
        btn.style.background = "var(--accent-rose)";
      } else {
        btn.innerText = "Owner Edit Mode: OFF";
        btn.style.background = "var(--accent-sage)";
      }
    }
  </script>
</body>
</html>
