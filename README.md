adicionando Index_html
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>RelaxPrime — Massageador Cervical Inteligente</title>
  <meta name="description" content="RelaxPrime — Diga adeus à dor cervical em 15 minutos. Massageador portátil, recarregável, 6 modos e 16 intensidades." />
  <style>
    :root{
      --bg:#faf8ff; --card:#ffffff; --accent:#b28cff; --accent-2:#8e63c9; --muted:#666; --success:#1fa67a;
      --maxw:1100px; --radius:14px; font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:linear-gradient(180deg,var(--bg),#fff);color:#222;-webkit-font-smoothing:antialiased}
    .container{max-width:var(--maxw);margin:28px auto;padding:0 20px}

    header{display:flex;align-items:center;justify-content:space-between;padding:18px 0}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:52px;height:52px;border-radius:12px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:white;font-weight:700;font-size:18px}
    .brand h1{margin:0;font-size:18px}
    .nav{display:flex;gap:14px;align-items:center}
    .btn{background:var(--accent);color:white;padding:10px 16px;border-radius:10px;border:0;cursor:pointer;font-weight:600}
    .ghost{background:transparent;border:1px solid rgba(0,0,0,0.06);padding:10px 12px;border-radius:10px}

    .hero{display:grid;grid-template-columns:1fr 460px;gap:28px;align-items:center;margin-top:12px}
    .hero-left h2{font-size:28px;margin:0 0 10px}
    .lead{color:var(--muted);margin-bottom:18px}
    .features{display:flex;gap:12px;flex-wrap:wrap}
    .feature{background:var(--card);padding:12px;border-radius:10px;box-shadow:0 4px 14px rgba(18,18,18,0.03);min-width:160px}

    .card{background:var(--card);border-radius:18px;padding:18px;box-shadow:0 10px 30px rgba(17,12,32,0.04)}

    /* Product card */
    .product{display:flex;flex-direction:column;gap:14px}
    .product-media{background:linear-gradient(180deg,#fff,#f8f6ff);border-radius:12px;height:320px;display:flex;align-items:center;justify-content:center}
    .product-media img{max-width:90%;max-height:90%;border-radius:10px}
    .price{font-size:20px;font-weight:700;color:var(--accent-2)}
    .oldprice{color:var(--muted);text-decoration:line-through;margin-left:8px;font-weight:600}
    .cta-row{display:flex;gap:12px}

    /* Sections */
    section{margin-top:22px}
    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}

    /* Testimonials */
    .testi{display:flex;gap:12px;align-items:flex-start}
    .avatar{width:56px;height:56px;border-radius:12px;background:linear-gradient(180deg,#fff,#f2ecff);display:flex;align-items:center;justify-content:center;font-weight:700;color:var(--accent-2)}

    /* FAQ */
    .faq-item{border-top:1px solid #f0eef8;padding:14px 0}
    .muted{color:var(--muted)}

    footer{margin-top:32px;padding:18px 0;color:var(--muted);font-size:14px}

    /* Modal */
    .modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(12,12,18,0.45);padding:24px}
    .modal.show{display:flex}
    .modal-card{width:480px;max-width:96%;background:var(--card);padding:18px;border-radius:12px}

    /* responsive */
    @media (max-width:980px){.hero{grid-template-columns:1fr;}.grid-3{grid-template-columns:1fr}.product-media{height:240px}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">RP</div>
        <div>
          <h1>RelaxPrime</h1>
          <div class="muted" style="font-size:13px">Seu corpo merece esse descanso</div>
        </div>
      </div>
      <nav class="nav">
        <a href="#features" class="muted">Benefícios</a>
        <a href="#testimonials" class="muted">Depoimentos</a>
        <a href="#faq" class="muted">FAQ</a>
        <button id="openBuy" class="btn">Quero alívio</button>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-left">
          <h2>Diga adeus à dor cervical em 15 minutos</h2>
          <p class="lead">Massageador Cervical Inteligente — pulsos terapêuticos que imitam massagem profissional. Leve, portátil e recarregável.</p>

          <div class="features">
            <div class="feature">✔ 6 modos + 16 intensidades</div>
            <div class="feature">✔ Design anatômico</div>
            <div class="feature">✔ Recarregável USB</div>
            <div class="feature">✔ Uso discreto e silencioso</div>
          </div>

          <div style="margin-top:18px" class="card">
            <div style="display:flex;align-items:center;justify-content:space-between">
              <div>
                <div style="font-size:13px;color:var(--muted)">Oferta especial</div>
                <div class="price">R$ 149,90 <span class="oldprice">R$ 249,90</span></div>
                <div class="muted" style="font-size:13px">Frete grátis • Garantia de 7 dias</div>
              </div>
              <div style="display:flex;flex-direction:column;gap:8px">
                <button id="buyTop" class="btn">Comprar agora</button>
                <button class="ghost" onclick="scrollToSection('faq')">Veja o FAQ</button>
              </div>
            </div>
          </div>

        </div>

        <div class="product card">
          <div class="product-media">
            <!-- simple svg product illustration -->
            <svg width="320" height="220" viewBox="0 0 320 220" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Massageador">
              <defs>
                <linearGradient id="g1" x1="0" x2="1"><stop offset="0" stop-color="#b28cff"/><stop offset="1" stop-color="#8e63c9"/></linearGradient>
              </defs>
              <rect x="10" y="30" rx="18" ry="18" width="300" height="160" fill="#fff" stroke="#efe9ff" />
              <ellipse cx="160" cy="110" rx="110" ry="70" fill="url(#g1)" opacity="0.12"/>
              <g transform="translate(80,65)">
                <rect x="0" y="0" rx="12" width="160" height="90" fill="#fff" stroke="#efe9ff" />
                <circle cx="30" cy="45" r="20" fill="#f6f0ff" stroke="#efe9ff" />
                <circle cx="130" cy="45" r="20" fill="#f6f0ff" stroke="#efe9ff" />
                <rect x="60" y="14" rx="8" width="40" height="12" fill="#f6f0ff"/>
              </g>
            </svg>
          </div>

          <div>
            <h3>Massageador Cervical Inteligente — RelaxPrime™</h3>
            <div class="muted">Alívio em minutos • Portátil • Recarregável</div>
            <div style="margin-top:12px" class="price">R$ 149,90 <span class="oldprice">R$ 249,90</span></div>
            <p class="muted" style="margin-top:8px">Frete grátis • Parcelas no cartão • Envio rastreado</p>

            <div style="margin-top:12px" class="cta-row">
              <button id="addToCart" class="btn">Adicionar ao carrinho</button>
              <button id="buyNow" class="ghost">Comprar com WhatsApp</button>
            </div>

            <ul style="margin-top:16px;color:var(--muted);font-size:14px">
              <li>6 modos de massagem</li>
              <li>16 níveis de intensidade</li>
              <li>Bateria de longa duração</li>
            </ul>
          </div>
        </div>
      </section>

      <section id="features" class="card">
        <h3>Como funciona</h3>
        <div style="display:flex;gap:14px;flex-wrap:wrap;margin-top:12px">
          <div style="flex:1;min-width:220px">
            <strong>Pulsos terapêuticos</strong>
            <p class="muted">Estimulação profunda que relaxa o músculo e melhora a circulação.</p>
          </div>
          <div style="flex:1;min-width:220px">
            <strong>Design anatômico</strong>
            <p class="muted">Adapta-se ao pescoço para maior conforto e eficiência.</p>
          </div>
          <div style="flex:1;min-width:220px">
            <strong>Uso discreto</strong>
            <p class="muted">Som baixo e formato compacto — use em casa, escritório ou viagem.</p>
          </div>
        </div>
      </section>

      <section id="testimonials" class="card">
        <h3>Depoimentos</h3>
        <div style="display:flex;gap:12px;flex-direction:column;margin-top:12px">
          <div class="testi">
            <div class="avatar">AL</div>
            <div>
              <strong>Ana L.</strong>
              <div class="muted">"Senti alívio já na primeira noite. Recomendo!"</div>
            </div>
          </div>

          <div class="testi">
            <div class="avatar">PM</div>
            <div>
              <strong>Pedro M.</strong>
              <div class="muted">"Perfeito para quem passa horas no computador."</div>
            </div>
          </div>

          <div class="testi">
            <div class="avatar">CM</div>
            <div>
              <strong>Carla M.</strong>
              <div class="muted">"Entrega rápida e produto de ótima qualidade."</div>
            </div>
          </div>
        </div>
      </section>

      <section id="faq" class="card">
        <h3>Perguntas Frequentes</h3>
        <div style="margin-top:8px">
          <div class="faq-item"><strong>Em quanto tempo vejo resultado?</strong><div class="muted">A maioria sente alívio ainda nos primeiros 10–15 minutos.</div></div>
          <div class="faq-item"><strong>Tem garantia?</strong><div class="muted">7 dias de garantia a partir do recebimento.</div></div>
          <div class="faq-item"><strong>Qual o prazo de entrega?</strong><div class="muted">7 a 15 dias úteis (depende da região).</div></div>
          <div class="faq-item"><strong>Como faço a devolução?</strong><div class="muted">Entre em contato no WhatsApp e nossa equipe orientará o processo.</div></div>
        </div>
      </section>

    </main>

    <footer>
      <div style="display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:12px">
        <div>© <strong>RelaxPrime</strong> — Seu corpo merece esse descanso</div>
        <div style="display:flex;gap:12px;align-items:center">
          <a href="#" class="muted">Política de Troca</a>
          <a href="#" class="muted">Privacidade</a>
        </div>
      </div>
    </footer>
  </div>

  <!-- Modal: Checkout / Order -->
  <div id="modal" class="modal" role="dialog" aria-hidden="true">
    <div class="modal-card">
      <div style="display:flex;align-items:center;justify-content:space-between">
        <strong>Confirmar pedido</strong>
        <button onclick="closeModal()" style="background:none;border:0;font-size:18px;cursor:pointer">✕</button>
      </div>

      <div style="margin-top:12px">
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:72px;height:72px;border-radius:10px;background:#f7f4ff;display:flex;align-items:center;justify-content:center">RP</div>
          <div>
            <div style="font-weight:700">Massageador Cervical Inteligente</div>
            <div class="muted">R$ 149,90 • Frete grátis</div>
          </div>
        </div>

        <form id="orderForm" style="margin-top:12px;display:flex;flex-direction:column;gap:10px">
          <input name="name" placeholder="Seu nome" required style="padding:10px;border-radius:8px;border:1px solid #eee" />
          <input name="phone" placeholder="Telefone (ex: 11999999-9999)" required style="padding:10px;border-radius:8px;border:1px solid #eee" />
          <input name="address" placeholder="Endereço completo para entrega" required style="padding:10px;border-radius:8px;border:1px solid #eee" />

          <div style="display:flex;gap:8px;align-items:center">
            <input type="checkbox" id="agree" required /> <label for="agree" class="muted">Confirmo que os dados estão corretos</label>
          </div>

          <div style="display:flex;gap:8px;justify-content:flex-end;margin-top:8px">
            <button type="button" onclick="submitOrder(true)" class="ghost">Pagar com cartão</button>
            <button type="button" onclick="submitOrder(false)" class="btn">Pagar via WhatsApp</button>
          </div>
        </form>

        <div id="orderMsg" style="display:none;margin-top:12px;padding:12px;border-radius:8px;background:#f7fff8;color:var(--success)"></div>
      </div>
    </div>
  </div>

  <script>
    // helpers
    const modal = document.getElementById('modal');
    const openBuy = document.getElementById('openBuy');
    const buyTop = document.getElementById('buyTop');
    const addToCart = document.getElementById('addToCart');
    const buyNow = document.getElementById('buyNow');

    function openModal(){ modal.classList.add('show'); modal.setAttribute('aria-hidden','false'); }
    function closeModal(){ modal.classList.remove('show'); modal.setAttribute('aria-hidden','true'); }

    openBuy.onclick = openModal;
    buyTop.onclick = openModal;
    addToCart.onclick = ()=>{ alert('Produto adicionado ao carrinho — pronto para comprar no checkout (simulação).'); window.scrollTo({top:0,behavior:'smooth'}) }

    buyNow.onclick = ()=>{ openModal(); document.querySelector('#orderForm input[name="name"]').focus(); }

    function scrollToSection(id){ document.getElementById(id).scrollIntoView({behavior:'smooth'}); }

    function submitOrder(isCard){
      const form = document.getElementById('orderForm');
      if(!form.reportValidity()) return;
      const name = form.name.value.trim();
      const phone = form.phone.value.trim();
      const address = form.address.value.trim();

      if(!name || !phone || !address){ alert('Preencha todos os campos'); return; }

      // build message
      const product = 'Massageador Cervical Inteligente — RelaxPrime';
      const price = 'R$ 149,90';
      const msg = `Olá, eu gostaria de comprar o ${product} (R$ 149,90)\nNome: ${name}\nTelefone: ${phone}\nEndereço: ${address}`;

      if(isCard){
        // simulate card payment
        showOrderMsg('Processando pagamento com cartão... (simulação)');
        setTimeout(()=>{
          showOrderMsg('Pagamento aprovado! Pedido confirmado. Em breve entraremos em contato pelo WhatsApp.');
          // in production: redirect to payment gateway
        },1500)
      } else {
        // open WhatsApp with prefilled message (phone number blank for store)
        const encoded = encodeURIComponent(msg);
        const phoneNumber = ''; // store number, e.g. 5511999999999 without +
        const url = phoneNumber ? `https://wa.me/${phoneNumber}?text=${encoded}` : `https://wa.me/?text=${encoded}`;
        window.open(url,'_blank');
      }
    }

    function showOrderMsg(text){
      const el = document.getElementById('orderMsg');
      el.style.display = 'block'; el.textContent = text;
    }

    // small UX: close modal on ESC
    window.addEventListener('keydown', (e)=>{ if(e.key==='Escape') closeModal(); })
  </script>
</body>
</html>
