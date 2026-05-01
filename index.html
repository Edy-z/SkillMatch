<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>El Puntazo – Órdenes de Trabajo</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<style>
  :root {
    --blue: #1a3a8f;
    --blue-light: #2348b0;
    --yellow: #f5c800;
    --white: #ffffff;
    --gray-bg: #f2f4f8;
    --gray-line: #d0d5e0;
    --red: #c0392b;
    --green: #27ae60;
    --text: #1a1f36;
    --text-soft: #5a6080;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--gray-bg);
    color: var(--text);
    min-height: 100vh;
  }

  /* cabecera principal */
  header {
    background: var(--blue);
    color: white;
    padding: 18px 32px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 12px rgba(0,0,0,0.2);
  }
  header .logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 26px;
    letter-spacing: 2px;
    color: white;
  }
  header .logo span { color: var(--yellow); }
  header .tabs { display: flex; gap: 8px; }
  header .tab {
    background: rgba(255,255,255,0.12);
    border: none;
    color: white;
    padding: 8px 18px;
    border-radius: 6px;
    cursor: pointer;
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    transition: background 0.2s;
  }
  header .tab:hover, header .tab.active { background: var(--yellow); color: var(--blue); }

  /* barra de estado de trello */
  #trello-banner {
    background: var(--yellow);
    color: var(--blue);
    padding: 10px 32px;
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 13px;
    font-weight: 600;
  }
  #trello-banner button {
    background: var(--blue);
    color: white;
    border: none;
    padding: 5px 14px;
    border-radius: 4px;
    cursor: pointer;
    font-size: 12px;
    font-weight: 600;
  }
  #trello-banner.connected { background: #e8f8ee; color: #1a6e38; }

  /* layout general */
  main { display: block; min-height: calc(100vh - 60px); }

  /* panel del formulario */
  #panel-form {
    width: 100%;
    max-width: 960px;
    margin: 0 auto;
    padding: 28px 40px;
    background: white;
    min-height: calc(100vh - 60px);
  }

  /* panel de pedidos guardados */
  #panel-orders {
    width: 100%;
    max-width: 960px;
    margin: 0 auto;
    padding: 28px 40px;
    background: var(--gray-bg);
    min-height: calc(100vh - 60px);
  }

  /* titulos de seccion dentro del formulario */
  .section-title {
    background: var(--blue);
    color: white;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 15px;
    letter-spacing: 1.5px;
    padding: 7px 14px;
    margin: 20px 0 12px;
    border-radius: 4px;
  }
  .section-title:first-child { margin-top: 0; }

  /* campos del formulario */
  .field-row { display: flex; gap: 12px; margin-bottom: 10px; }
  .field { display: flex; flex-direction: column; flex: 1; }
  .field label {
    font-size: 11px;
    font-weight: 600;
    color: var(--text-soft);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 4px;
  }
  .field input[type="text"],
  .field input[type="date"],
  .field input[type="tel"],
  .field textarea,
  .field select {
    border: 1.5px solid var(--gray-line);
    border-radius: 6px;
    padding: 8px 10px;
    font-size: 14px;
    font-family: 'DM Sans', sans-serif;
    color: var(--text);
    background: white;
    transition: border-color 0.2s;
    outline: none;
  }
  .field input:focus, .field textarea:focus, .field select:focus {
    border-color: var(--blue);
  }
  .field textarea { resize: vertical; min-height: 60px; }

  /* fila de fechas */
  .dates-row {
    display: flex;
    gap: 12px;
    margin-bottom: 10px;
  }
  .date-field {
    flex: 1;
    display: flex;
    flex-direction: column;
  }
  .date-field label {
    font-size: 11px;
    font-weight: 600;
    color: var(--text-soft);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 4px;
  }
  .date-field input {
    border: 1.5px solid var(--gray-line);
    border-radius: 6px;
    padding: 8px 10px;
    font-size: 14px;
    font-family: 'DM Sans', sans-serif;
    outline: none;
  }
  .date-field.vence input { border-color: var(--yellow); background: #fffbe6; }
  .date-field input:focus { border-color: var(--blue); }

  /* grupo de checkboxes tipo boton */
  .check-group {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 10px;
  }
  .check-item {
    display: flex;
    align-items: center;
    gap: 5px;
    background: var(--gray-bg);
    border: 1.5px solid var(--gray-line);
    border-radius: 5px;
    padding: 5px 10px;
    cursor: pointer;
    transition: all 0.15s;
    font-size: 13px;
    user-select: none;
  }
  .check-item input { display: none; }
  .check-item.checked {
    background: var(--blue);
    border-color: var(--blue);
    color: white;
  }
  .check-item .box {
    width: 14px; height: 14px;
    border: 2px solid var(--gray-line);
    border-radius: 3px;
    background: white;
    flex-shrink: 0;
  }
  .check-item.checked .box { background: var(--yellow); border-color: var(--yellow); }

  /* botones de tipo de entrega */
  .entrega-row {
    display: flex;
    gap: 10px;
    margin-bottom: 10px;
  }
  .entrega-btn {
    flex: 1;
    padding: 9px;
    border: 2px solid var(--gray-line);
    border-radius: 6px;
    background: white;
    font-family: 'DM Sans', sans-serif;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.15s;
    color: var(--text-soft);
  }
  .entrega-btn.active { border-color: var(--blue); background: var(--blue); color: white; }

  /* tabla de tallas */
  .sizes-table { width: 100%; border-collapse: collapse; margin-bottom: 10px; font-size: 12px; }
  .sizes-table th {
    background: var(--blue);
    color: white;
    padding: 5px 4px;
    text-align: center;
    font-weight: 600;
  }
  .sizes-table td { border: 1px solid var(--gray-line); padding: 3px; }
  .sizes-table input {
    width: 100%;
    border: none;
    outline: none;
    text-align: center;
    font-size: 12px;
    padding: 3px 2px;
    font-family: 'DM Sans', sans-serif;
    background: transparent;
  }
  .sizes-table .model-cell input { font-weight: 600; background: #f8f9fc; }

  /* grid del parche, de momento sin uso pero lo dejo */
  .parche-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 10px;
    margin-bottom: 10px;
  }

  /* posiciones, igual que arriba */
  .pos-group {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 10px;
  }

  /* boton de guardar */
  .btn-submit {
    width: 100%;
    background: var(--blue);
    color: white;
    border: none;
    padding: 14px;
    border-radius: 8px;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    letter-spacing: 2px;
    cursor: pointer;
    margin-top: 20px;
    transition: background 0.2s, transform 0.1s;
  }
  .btn-submit:hover { background: var(--blue-light); }
  .btn-submit:active { transform: scale(0.99); }

  .btn-clear {
    width: 100%;
    background: transparent;
    color: var(--text-soft);
    border: 1.5px solid var(--gray-line);
    padding: 10px;
    border-radius: 8px;
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    cursor: pointer;
    margin-top: 8px;
  }
  .btn-clear:hover { border-color: var(--red); color: var(--red); }

  /* lista de pedidos */
  .orders-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  .orders-header h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 24px;
    letter-spacing: 1px;
    color: var(--blue);
  }
  .orders-count {
    background: var(--blue);
    color: white;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 600;
  }

  /* cada tarjeta de pedido */
  .order-card {
    background: white;
    border-radius: 10px;
    border: 1.5px solid var(--gray-line);
    margin-bottom: 14px;
    overflow: hidden;
    transition: box-shadow 0.2s;
    animation: fadeIn 0.3s ease;
  }
  .order-card:hover { box-shadow: 0 4px 16px rgba(26,58,143,0.1); }
  @keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

  .card-header {
    background: var(--blue);
    color: white;
    padding: 10px 16px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .card-header .client-name { font-weight: 600; font-size: 15px; }
  .card-header .card-date { font-size: 12px; opacity: 0.8; }

  .card-body { padding: 14px 16px; }
  .card-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 10px; }
  .tag {
    background: var(--gray-bg);
    border: 1px solid var(--gray-line);
    border-radius: 4px;
    padding: 3px 8px;
    font-size: 11px;
    font-weight: 600;
    color: var(--text-soft);
    text-transform: uppercase;
  }
  .tag.blue { background: #e8eeff; border-color: #b0c0f0; color: var(--blue); }
  .tag.yellow { background: #fffbe6; border-color: #f5c800; color: #7a6000; }
  .tag.vence { background: #fff0f0; border-color: #f5a0a0; color: var(--red); }

  .card-obs { font-size: 13px; color: var(--text-soft); font-style: italic; margin-bottom: 10px; }

  .card-actions { display: flex; gap: 8px; }
  .btn-trello {
    flex: 1;
    background: #0052cc;
    color: white;
    border: none;
    padding: 8px;
    border-radius: 6px;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 6px;
    transition: background 0.2s;
  }
  .btn-trello:hover { background: #003d99; }
  .btn-trello.sent { background: var(--green); cursor: default; }
  .btn-delete {
    background: transparent;
    border: 1.5px solid var(--gray-line);
    color: var(--text-soft);
    padding: 8px 12px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 13px;
    transition: all 0.15s;
  }
  .btn-delete:hover { border-color: var(--red); color: var(--red); }
  .btn-pdf {
    background: #e74c3c;
    color: white;
    border: none;
    padding: 8px 12px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 13px;
    font-weight: 600;
    transition: background 0.2s;
  }
  .btn-pdf:hover { background: #c0392b; }
  .btn-whatsapp {
    background: #25d366;
    color: white;
    border: none;
    padding: 8px 12px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 13px;
    font-weight: 600;
    transition: background 0.2s;
  }
  .btn-whatsapp:hover { background: #1da851; }
  .btn-fotos {
    background: #ff6b35;
    color: white;
    border: none;
    padding: 8px 12px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 13px;
    font-weight: 600;
    transition: background 0.2s;
  }
  .btn-fotos:hover { background: #e55a28; }
  .foto-thumb {
    width: 90px; height: 90px;
    object-fit: cover;
    border-radius: 8px;
    border: 2px solid var(--gray-line);
    position: relative;
  }
  .foto-wrap {
    position: relative;
    display: inline-block;
  }
  .foto-wrap .remove-foto {
    position: absolute;
    top: -6px; right: -6px;
    background: var(--red);
    color: white;
    border: none;
    border-radius: 50%;
    width: 20px; height: 20px;
    font-size: 11px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
  }
  .modal-fotos img {
    max-width: 100%;
    border-radius: 8px;
    margin-bottom: 10px;
  }

  /* modal de configuracion trello */
  .modal-overlay {
    position: fixed; inset: 0;
    background: rgba(0,0,0,0.5);
    z-index: 200;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
  }
  .modal {
    background: white;
    border-radius: 12px;
    padding: 28px;
    width: 100%;
    max-width: 480px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.3);
  }
  .modal h3 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 22px;
    color: var(--blue);
    margin-bottom: 6px;
    letter-spacing: 1px;
  }
  .modal p { font-size: 13px; color: var(--text-soft); margin-bottom: 16px; line-height: 1.5; }
  .modal .field { margin-bottom: 14px; }
  .modal-actions { display: flex; gap: 10px; margin-top: 20px; }
  .btn-primary {
    flex: 1;
    background: var(--blue);
    color: white;
    border: none;
    padding: 11px;
    border-radius: 7px;
    font-family: 'DM Sans', sans-serif;
    font-weight: 600;
    cursor: pointer;
    font-size: 14px;
  }
  .btn-secondary {
    flex: 1;
    background: transparent;
    border: 1.5px solid var(--gray-line);
    color: var(--text-soft);
    padding: 11px;
    border-radius: 7px;
    font-family: 'DM Sans', sans-serif;
    font-weight: 600;
    cursor: pointer;
    font-size: 14px;
  }

  .toast {
    position: fixed;
    bottom: 24px;
    right: 24px;
    background: var(--green);
    color: white;
    padding: 12px 20px;
    border-radius: 8px;
    font-weight: 600;
    font-size: 14px;
    z-index: 300;
    animation: slideUp 0.3s ease;
    box-shadow: 0 4px 16px rgba(0,0,0,0.15);
  }
  .toast.error { background: var(--red); }
  @keyframes slideUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
  @media (max-width: 768px) {
    .toast {
      bottom: auto;
      top: 80px;
      left: 50%;
      right: auto;
      transform: translateX(-50%);
      font-size: 16px;
      padding: 16px 28px;
      border-radius: 12px;
      text-align: center;
      min-width: 260px;
      box-shadow: 0 8px 32px rgba(0,0,0,0.25);
    }
  }

  .empty-state {
    text-align: center;
    padding: 60px 20px;
    color: var(--text-soft);
  }
  .empty-state .icon { font-size: 48px; margin-bottom: 12px; }
  .empty-state h3 { font-size: 18px; font-weight: 600; margin-bottom: 6px; }
  .empty-state p { font-size: 14px; }

  .hidden { display: none !important; }

  /* separador */
  .divider { border: none; border-top: 1px solid var(--gray-line); margin: 16px 0; }
</style>
</head>
<body>

<header>
  <div class="logo">El <span>Puntazo</span> — Órdenes</div>
  <div class="tabs">
    <button class="tab active" onclick="showPanel('form')">➕ Nueva Orden</button>
    <button class="tab" onclick="showPanel('orders')">📋 Pedidos</button>
    <button class="tab" onclick="openTrelloModal()">⚙️ Trello</button>
  </div>
</header>

<div id="trello-banner">
  <span id="banner-text">⚠️ Trello no configurado — pulsa Configurar para conectarlo</span>
  <button onclick="openTrelloModal()">Configurar Trello</button>
</div>

<main>
  <!-- FORM PANEL -->
  <div id="panel-form">

    <div class="section-title">CLIENTE</div>
    <div class="field-row">
      <div class="field">
        <label>Nombre</label>
        <input type="text" id="f-nombre" placeholder="Nombre del cliente">
      </div>
      <div class="field" style="flex:0 0 160px">
        <label>Teléfono</label>
        <input type="tel" id="f-telefono" placeholder="6xx xxx xxx">
      </div>
    </div>

    <div class="dates-row">
      <div class="date-field">
        <label>📅 Fecha</label>
        <input type="date" id="f-fecha">
      </div>
      <div class="date-field vence">
        <label>⏰ Vence</label>
        <input type="date" id="f-vence">
      </div>
    </div>

    <div style="margin-bottom:10px">
      <label style="font-size:11px;font-weight:600;color:var(--text-soft);text-transform:uppercase;letter-spacing:0.5px;display:block;margin-bottom:6px;">Entrega</label>
      <div class="entrega-row">
        <button class="entrega-btn active" id="btn-recoge" onclick="setEntrega('recoge')">📦 Recoge</button>
        <button class="entrega-btn" id="btn-envio" onclick="setEntrega('envio')">🚚 Envío</button>
      </div>
    </div>

    <div class="field">
      <label>Observaciones</label>
      <textarea id="f-obs" placeholder="Notas adicionales..."></textarea>
    </div>

    <div class="section-title">DATOS DEL TRABAJO</div>
    <div class="field">
      <label>Descripción del trabajo</label>
      <textarea id="f-trabajo" placeholder="Describe el trabajo a realizar..."></textarea>
    </div>

    <div class="section-title">PRODUCTO</div>
    <div class="check-group" id="productos">
      <label class="check-item"><input type="checkbox" value="Camiseta"><div class="box"></div>Camiseta</label>
      <label class="check-item"><input type="checkbox" value="Camisa"><div class="box"></div>Camisa</label>
      <label class="check-item"><input type="checkbox" value="Hoodie"><div class="box"></div>Hoodie</label>
      <label class="check-item"><input type="checkbox" value="Sudadera"><div class="box"></div>Sudadera</label>
      <label class="check-item"><input type="checkbox" value="Polo"><div class="box"></div>Polo</label>
      <label class="check-item"><input type="checkbox" value="Pantalón"><div class="box"></div>Pantalón</label>
      <label class="check-item"><input type="checkbox" value="Abrigo"><div class="box"></div>Abrigo</label>
      <label class="check-item"><input type="checkbox" value="Polar"><div class="box"></div>Polar</label>
      <label class="check-item"><input type="checkbox" value="Chaleco"><div class="box"></div>Chaleco</label>
      <label class="check-item"><input type="checkbox" value="Bata"><div class="box"></div>Bata</label>
      <label class="check-item"><input type="checkbox" value="Otros"><div class="box"></div>Otros</label>
    </div>

    <div class="section-title">SERVICIO</div>
    <div class="check-group" id="servicios">
      <label class="check-item"><input type="checkbox" value="Bordado"><div class="box"></div>Bordado</label>
      <label class="check-item"><input type="checkbox" value="DTF"><div class="box"></div>DTF</label>
      <label class="check-item"><input type="checkbox" value="Vinilo"><div class="box"></div>Vinilo</label>
      <label class="check-item"><input type="checkbox" value="Sublimación"><div class="box"></div>Sublimación</label>
      <label class="check-item"><input type="checkbox" value="Serigrafía"><div class="box"></div>Serigrafía</label>
      <label class="check-item"><input type="checkbox" value="Picaje"><div class="box"></div>Picaje</label>
      <label class="check-item"><input type="checkbox" value="DTG"><div class="box"></div>DTG</label>
    </div>

    <div class="section-title">TALLAS Y CANTIDADES</div>
    <div style="overflow-x:auto">
      <table class="sizes-table">
        <thead>
          <tr>
            <th>Modelo/Marca</th><th>Color</th>
            <th>XXS</th><th>XS</th><th>S</th><th>M</th><th>L</th><th>XL</th><th>XXL</th><th>3XL</th><th>4XL</th><th>5XL</th><th>TOTAL</th>
          </tr>
        </thead>
        <tbody id="sizes-body">
          <tr>
            <td class="model-cell"><input type="text" placeholder="Modelo 1"></td>
            <td><input type="text" placeholder="Color"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="text" readonly style="font-weight:600;background:#e8eeff;color:var(--blue)"></td>
          </tr>
          <tr>
            <td class="model-cell"><input type="text" placeholder="Modelo 2"></td>
            <td><input type="text" placeholder="Color"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="number" min="0" oninput="calcTotal(this)"></td>
            <td><input type="text" readonly style="font-weight:600;background:#e8eeff;color:var(--blue)"></td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="section-title">POSICIÓN DE ESTAMPADO</div>
    <div style="font-size:12px;color:var(--text-soft);margin-bottom:8px;">Selecciona dónde va el diseño:</div>
    <div class="check-group" id="posiciones">
      <label class="check-item"><input type="checkbox" value="Frontal BC"><div class="box"></div>Frontal BC</label>
      <label class="check-item"><input type="checkbox" value="Frontal EC"><div class="box"></div>Frontal EC</label>
      <label class="check-item"><input type="checkbox" value="Frontal EB"><div class="box"></div>Frontal EB</label>
      <label class="check-item"><input type="checkbox" value="Frontal PC"><div class="box"></div>Frontal PC</label>
      <label class="check-item"><input type="checkbox" value="Espalda BC"><div class="box"></div>Espalda BC</label>
      <label class="check-item"><input type="checkbox" value="Espalda EC"><div class="box"></div>Espalda EC</label>
      <label class="check-item"><input type="checkbox" value="Espalda EB"><div class="box"></div>Espalda EB</label>
      <label class="check-item"><input type="checkbox" value="Manga Derecha"><div class="box"></div>Manga Derecha</label>
      <label class="check-item"><input type="checkbox" value="Manga Izquierda"><div class="box"></div>Manga Izquierda</label>
      <label class="check-item"><input type="checkbox" value="Bolsillo"><div class="box"></div>Bolsillo</label>
    </div>

    <div class="field-row">
      <div class="field">
        <label>Color diseño</label>
        <input type="text" id="f-color-diseno" placeholder="Ej: Blanco, Rojo">
      </div>
    </div>

    <div class="section-title">PARCHE / BORDADO</div>
    <div id="parche-section">
      <div class="check-group" style="margin-bottom:10px">
        <label class="check-item"><input type="checkbox" value="Velcro"><div class="box"></div>Velcro</label>
        <label class="check-item"><input type="checkbox" value="Adhesivo"><div class="box"></div>Adhesivo</label>
        <label class="check-item"><input type="checkbox" value="Coser"><div class="box"></div>Coser</label>
      </div>
      <div class="field-row">
        <div class="field">
          <label>Ancho</label>
          <input type="text" id="f-ancho" placeholder="cm">
        </div>
        <div class="field">
          <label>Alto</label>
          <input type="text" id="f-alto" placeholder="cm">
        </div>
        <div class="field">
          <label>Color hilo</label>
          <input type="text" id="f-color-hilo" placeholder="Color">
        </div>
        <div class="field">
          <label>Diseño mini</label>
          <input type="text" id="f-diseno-mini" placeholder="Desc.">
        </div>
      </div>
    </div>

    <div class="section-title">GORRA</div>
    <div class="field-row">
      <div class="field">
        <label>Unidades</label>
        <input type="number" id="f-gorra-ud" placeholder="0" min="0">
      </div>
      <div class="field">
        <label>Modelo</label>
        <input type="text" id="f-gorra-modelo" placeholder="Modelo">
      </div>
      <div class="field">
        <label>Color tela</label>
        <input type="text" id="f-gorra-color-tela" placeholder="Color">
      </div>
      <div class="field">
        <label>Color hilo</label>
        <input type="text" id="f-gorra-color-hilo" placeholder="Color">
      </div>
    </div>
    <div style="font-size:12px;color:var(--text-soft);margin-bottom:6px;font-weight:600;">Posición en gorra:</div>
    <div class="check-group" id="posiciones-gorra">
      <label class="check-item"><input type="checkbox" value="Frente"><div class="box"></div>Frente</label>
      <label class="check-item"><input type="checkbox" value="L.Izquierdo"><div class="box"></div>L.Izquierdo</label>
      <label class="check-item"><input type="checkbox" value="Trasera"><div class="box"></div>Trasera</label>
      <label class="check-item"><input type="checkbox" value="L.Derecho"><div class="box"></div>L.Derecho</label>
    </div>

    <div class="section-title">OTROS TRABAJOS</div>
    <div class="field">
      <label>Descripción</label>
      <textarea id="f-otros" placeholder="Otros trabajos adicionales..."></textarea>
    </div>

    <div class="section-title">📸 FOTOS DEL DISEÑO</div>
    <div style="display:flex;gap:10px;margin-bottom:10px;">
      <button type="button" onclick="document.getElementById('f-camara').click()" style="flex:1;padding:18px;border:2px dashed #25a8e0;border-radius:10px;background:#f0faff;cursor:pointer;font-family:DM Sans,sans-serif;font-size:14px;font-weight:600;color:#1a6e9f;transition:all 0.2s;">
        <div style="font-size:32px;margin-bottom:6px;">📷</div>
        Hacer foto con cámara
      </button>
      <button type="button" onclick="document.getElementById('f-fotos').click()" style="flex:1;padding:18px;border:2px dashed var(--gray-line);border-radius:10px;background:#fafbff;cursor:pointer;font-family:DM Sans,sans-serif;font-size:14px;font-weight:600;color:var(--blue);transition:all 0.2s;" ondragover="event.preventDefault();this.style.borderColor='var(--blue)'" ondragleave="this.style.borderColor='var(--gray-line)'" ondrop="handleDrop(event)">
        <div style="font-size:32px;margin-bottom:6px;">🖼️</div>
        Subir desde galería o archivo
      </button>
    </div>
    <input type="file" id="f-camara" accept="image/*" capture="environment" style="display:none" onchange="handleFotos(this.files)">
    <input type="file" id="f-fotos" multiple accept="image/*,application/pdf" style="display:none" onchange="handleFotos(this.files)">
    <div id="fotos-preview" style="display:flex;flex-wrap:wrap;gap:10px;margin-bottom:16px;"></div>

    <div class="section-title">🔷 DESTINO EN TRELLO</div>
    <div class="field-row">
      <div class="field">
        <label>Tablero</label>
        <select id="f-tablero" onchange="cargarListas(this.value)" style="border:1.5px solid var(--gray-line);border-radius:6px;padding:8px 10px;font-size:14px;font-family:DM Sans,sans-serif;">
          <option value="">— Selecciona tablero —</option>
        </select>
      </div>
      <div class="field">
        <label>Lista (columna)</label>
        <select id="f-lista" style="border:1.5px solid var(--gray-line);border-radius:6px;padding:8px 10px;font-size:14px;font-family:DM Sans,sans-serif;">
          <option value="">— Primero elige tablero —</option>
        </select>
      </div>
    </div>
    <div id="trello-load-status" style="font-size:12px;color:var(--text-soft);margin-bottom:10px;"></div>

    <button class="btn-submit" onclick="guardarOrden()">💾 GUARDAR ORDEN</button>
    <button class="btn-clear" onclick="limpiarFormulario()">🗑️ Limpiar formulario</button>
  </div>

  <!-- ORDERS PANEL -->
  <div id="panel-orders" class="hidden">
    <div class="orders-header">
      <h2>Pedidos guardados</h2>
      <span class="orders-count" id="orders-count">0 órdenes</span>
    </div>
    <div id="orders-list"></div>
  </div>
</main>

<!-- TRELLO MODAL -->
<div class="modal-overlay hidden" id="trello-modal">
  <div class="modal">
    <h3>⚙️ Configurar Trello</h3>
    <p>Necesitas la API Key y el Token de tu cuenta de Trello. Ve a trello.com/app-key para obtenerlos.</p>

    <div class="field">
      <label>API Key de Trello</label>
      <input type="text" id="t-apikey" placeholder="Tu API Key">
    </div>
    <div class="field">
      <label>Token de Trello</label>
      <input type="text" id="t-token" placeholder="Tu Token">
    </div>
    <div class="field">
      <label>ID de lista (opcional, ya no hace falta con los desplegables)</label>
      <input type="text" id="t-listid" placeholder="opcional">
    </div>

    <div style="background:#f2f4f8;border-radius:8px;padding:14px;margin-top:10px;font-size:12px;line-height:1.7;color:#444">
      <strong>📖 Cómo obtener estos datos:</strong><br>
      1. Ve a <strong>trello.com/power-ups/admin</strong> → crea una Power-Up → copia la <strong>API Key</strong><br>
      2. En esa misma página pulsa <strong>"Token"</strong> → autoriza → copia el <strong>Token</strong><br>
      3. Abre tu tablero Trello, añade <strong>.json</strong> al final de la URL → busca tu lista y copia su <strong>"id"</strong>
    </div>

    <div class="modal-actions">
      <button class="btn-secondary" onclick="closeTrelloModal()">Cancelar</button>
      <button class="btn-primary" onclick="saveTrelloConfig()">💾 Guardar configuración</button>
    </div>
  </div>
</div>

<script>
  let entregaMode = 'recoge';
  let orders = JSON.parse(localStorage.getItem('puntazo_orders') || '[]');
  let trelloConfig = JSON.parse(localStorage.getItem('puntazo_trello') || '{}');

  // arrancar la app
  document.getElementById('f-fecha').value = new Date().toISOString().split('T')[0];
  updateBanner();
  renderOrders();
  if (trelloConfig.apiKey && trelloConfig.token) cargarTableros();

  function showPanel(panel) {
    document.getElementById('panel-form').classList.toggle('hidden', panel !== 'form');
    document.getElementById('panel-orders').classList.toggle('hidden', panel !== 'orders');
    document.querySelectorAll('.tab').forEach((t, i) => {
      t.classList.toggle('active', (i === 0 && panel === 'form') || (i === 1 && panel === 'orders'));
    });
    if (panel === 'orders') renderOrders();
  }

  function toggleCheck(el) {
    el.classList.toggle('checked');
  }

  // esto es para que los checkboxes funcionen bien, si no se dispara doble
  document.querySelectorAll('.check-item').forEach(item => {
    item.addEventListener('click', function(e) {
      e.preventDefault();
      this.classList.toggle('checked');
    });
  });

  function setEntrega(mode) {
    entregaMode = mode;
    document.getElementById('btn-recoge').classList.toggle('active', mode === 'recoge');
    document.getElementById('btn-envio').classList.toggle('active', mode === 'envio');
  }

  function calcTotal(input) {
    const row = input.closest('tr');
    const nums = [...row.querySelectorAll('td:nth-child(n+3):not(:last-child) input')];
    const total = nums.reduce((s, i) => s + (parseInt(i.value) || 0), 0);
    row.querySelector('td:last-child input').value = total || '';
  }

  function getChecked(groupId) {
    return [...document.querySelectorAll(`#${groupId} .check-item.checked input`)].map(i => i.value);
  }

  function getSizes() {
    const rows = document.querySelectorAll('#sizes-body tr');
    const sizes = [];
    rows.forEach(row => {
      const inputs = row.querySelectorAll('input');
      const modelo = inputs[0].value.trim();
      if (!modelo) return;
      const color = inputs[1].value.trim();
      const tallas = ['XXS','XS','S','M','L','XL','XXL','3XL','4XL','5XL'];
      const cantidades = {};
      tallas.forEach((t, i) => {
        const v = parseInt(inputs[i+2].value) || 0;
        if (v) cantidades[t] = v;
      });
      const total = inputs[12].value;
      sizes.push({ modelo, color, cantidades, total });
    });
    return sizes;
  }

  function guardarOrden() {
    // minimo necesitamos el nombre del cliente
    const nombre = document.getElementById('f-nombre').value.trim();
    if (!nombre) { showToast('⚠️ Introduce el nombre del cliente', true); return; }

    const order = {
      id: Date.now(),
      fecha: document.getElementById('f-fecha').value,
      vence: document.getElementById('f-vence').value,
      entrega: entregaMode,
      cliente: { nombre, telefono: document.getElementById('f-telefono').value },
      obs: document.getElementById('f-obs').value,
      trabajo: document.getElementById('f-trabajo').value,
      productos: getChecked('productos'),
      servicios: getChecked('servicios'),
      posiciones: getChecked('posiciones'),
      colorDiseno: document.getElementById('f-color-diseno').value,
      parche: {
        tipo: getChecked('parche-section'),
        ancho: document.getElementById('f-ancho').value,
        alto: document.getElementById('f-alto').value,
        colorHilo: document.getElementById('f-color-hilo').value,
        disenoMini: document.getElementById('f-diseno-mini').value,
      },
      gorra: {
        unidades: document.getElementById('f-gorra-ud').value,
        modelo: document.getElementById('f-gorra-modelo').value,
        colorTela: document.getElementById('f-gorra-color-tela').value,
        colorHilo: document.getElementById('f-gorra-color-hilo').value,
        posiciones: getChecked('posiciones-gorra'),
      },
      sizes: getSizes(),
      otros: document.getElementById('f-otros').value,
      listId: document.getElementById('f-lista').value,
      tableroNombre: document.getElementById('f-tablero').options[document.getElementById('f-tablero').selectedIndex]?.text || '',
      listaNombre: document.getElementById('f-lista').options[document.getElementById('f-lista').selectedIndex]?.text || '',
      fotos: fotosActuales.slice(),
      trelloSent: false,
    };

    orders.unshift(order);
    localStorage.setItem('puntazo_orders', JSON.stringify(orders));
    // pequeña espera para que se vea la notificacion antes de cambiar de panel
    showToast('✅ Orden guardada correctamente');
    setTimeout(() => {
      limpiarFormulario(true);
      showPanel('orders');
    }, window.innerWidth < 768 ? 800 : 300);
  }

  function limpiarFormulario(silent = false) {
    if (!silent && !confirm('¿Limpiar todos los campos?')) return;
    document.querySelectorAll('#panel-form input[type="text"], #panel-form input[type="tel"], #panel-form input[type="number"], #panel-form textarea').forEach(i => i.value = '');
    document.querySelectorAll('.check-item').forEach(i => i.classList.remove('checked'));
    document.getElementById('f-fecha').value = new Date().toISOString().split('T')[0];
    document.getElementById('f-vence').value = '';
    setEntrega('recoge');
    fotosActuales = [];
    renderFotosPreview();
    document.getElementById('f-tablero').value = '';
    document.getElementById('f-lista').innerHTML = '<option value="">— Primero elige tablero —</option>';
  }

  function renderOrders() {
    const list = document.getElementById('orders-list');
    document.getElementById('orders-count').textContent = `${orders.length} orden${orders.length !== 1 ? 'es' : ''}`;

    if (!orders.length) {
      list.innerHTML = `<div class="empty-state"><div class="icon">📋</div><h3>Sin órdenes todavía</h3><p>Crea tu primera orden de trabajo</p></div>`;
      return;
    }

    list.innerHTML = orders.map(o => `
      <div class="order-card" id="card-${o.id}">
        <div class="card-header">
          <div>
            <div class="client-name">👤 ${o.cliente.nombre}</div>
            <div class="card-date">📅 ${o.fecha}${o.vence ? ` · ⏰ Vence: ${o.vence}` : ''} · ${o.entrega === 'recoge' ? '📦 Recoge' : '🚚 Envío'}</div>
          </div>
        </div>
        <div class="card-body">
          <div class="card-tags">
            ${o.productos.map(p => `<span class="tag blue">${p}</span>`).join('')}
            ${o.servicios.map(s => `<span class="tag yellow">${s}</span>`).join('')}
            ${o.sizes.length ? `<span class="tag">${o.sizes.reduce((s,r)=>s+(parseInt(r.total)||0),0)} uds</span>` : ''}
            ${o.gorra.unidades ? `<span class="tag">🧢 ${o.gorra.unidades} gorras</span>` : ''}
            ${o.tableroNombre ? `<span class="tag blue">🔷 ${o.tableroNombre}${o.listaNombre ? ' → ' + o.listaNombre : ''}</span>` : ''}
          </div>
          ${o.trabajo ? `<div class="card-obs">${o.trabajo}</div>` : ''}
          ${o.obs ? `<div class="card-obs">📝 ${o.obs}</div>` : ''}
          <div class="card-actions">
            <button class="btn-trello ${o.trelloSent ? 'sent' : ''}" onclick="sendToTrello(${o.id})">
              ${o.trelloSent ? '✅ Enviado a Trello' : '🔷 Enviar a Trello'}
            </button>
            <button class="btn-pdf" onclick="generarPDF(${o.id})">🖨️ PDF</button>
            ${o.cliente.telefono ? `<button class="btn-whatsapp" onclick="openWhatsApp(${o.id})">💬 WhatsApp</button>` : ''}
            ${o.fotos && o.fotos.length ? `<button class="btn-fotos" onclick="verFotos(${o.id})">📸 ${o.fotos.length} foto${o.fotos.length>1?'s':''}</button>` : ''}
            <button class="btn-delete" onclick="deleteOrder(${o.id})">🗑️</button>
          </div>
        </div>
      </div>
    `).join('');
  }

  function deleteOrder(id) {
    if (!confirm('¿Eliminar esta orden?')) return;
    orders = orders.filter(o => o.id !== id);
    localStorage.setItem('puntazo_orders', JSON.stringify(orders));
    renderOrders();
  }

  async function sendToTrello(id) {
    const cfg = trelloConfig;
    if (!cfg.apiKey || !cfg.token) {
      showToast('⚠️ Configura Trello primero', true);
      openTrelloModal();
      return;
    }

    const order = orders.find(o => o.id === id);
    if (!order) return;

    const listId = order.listId;
    if (!listId) {
      showToast('⚠️ Esta orden no tiene tablero/lista seleccionada', true);
      return;
    }

    const desc = buildTrelloDesc(order);
    const name = `📦 ${order.cliente.nombre} — ${order.fecha}${order.vence ? ' (Vence: ' + order.vence + ')' : ''}`;
    const dueDate = order.vence ? new Date(order.vence).toISOString() : null;

    // cambiar el boton a estado cargando
    const btn = document.querySelector(`#card-${id} .btn-trello`);
    if (btn) { btn.textContent = '⏳ Enviando...'; btn.disabled = true; }

    try {
      const params = new URLSearchParams({
        key: cfg.apiKey,
        token: cfg.token,
        name: name,
        desc: desc,
        idList: listId,
      });
      if (dueDate) params.append('due', dueDate);

      const res = await fetch(`https://api.trello.com/1/cards?${params.toString()}`, {
        method: 'POST',
      });

      if (!res.ok) throw new Error('Error Trello: ' + res.status);

      order.trelloSent = true;
      localStorage.setItem('puntazo_orders', JSON.stringify(orders));
      renderOrders();
      showToast('✅ Tarjeta creada en Trello');
    } catch (e) {
      if (btn) { btn.textContent = '🔷 Enviar a Trello'; btn.disabled = false; }
      showToast('❌ Error al conectar con Trello. Revisa la configuración.', true);
    }
  }

  function buildTrelloDesc(o) {
    let d = '';
    d += `## 👤 Cliente\n**Nombre:** ${o.cliente.nombre}\n`;
    if (o.cliente.telefono) d += `**Teléfono:** ${o.cliente.telefono}\n`;
    d += `**Fecha:** ${o.fecha}`;
    if (o.vence) d += ` | **Vence:** ${o.vence}`;
    d += `\n**Entrega:** ${o.entrega === 'recoge' ? 'Recoge en tienda' : 'Envío a domicilio'}\n`;
    if (o.obs) d += `**Obs:** ${o.obs}\n`;
    if (o.trabajo) d += `\n## 📋 Trabajo\n${o.trabajo}\n`;
    if (o.productos.length) d += `\n## 👕 Producto\n${o.productos.join(', ')}\n`;
    if (o.servicios.length) d += `\n## 🛠️ Servicio\n${o.servicios.join(', ')}\n`;
    if (o.posiciones.length) d += `\n## 📍 Posición estampado\n${o.posiciones.join(', ')}\n`;
    if (o.colorDiseno) d += `**Color diseño:** ${o.colorDiseno}\n`;
    if (o.sizes.length) {
      d += `\n## 📏 Tallas\n`;
      o.sizes.forEach(s => {
        d += `**${s.modelo}** (${s.color}): `;
        d += Object.entries(s.cantidades).map(([k,v])=>`${k}:${v}`).join(', ');
        d += ` | Total: ${s.total}\n`;
      });
    }
    if (o.gorra.unidades) {
      d += `\n## 🧢 Gorra\n`;
      d += `${o.gorra.unidades} uds — ${o.gorra.modelo} — Tela: ${o.gorra.colorTela} — Hilo: ${o.gorra.colorHilo}\n`;
      if (o.gorra.posiciones.length) d += `Posición: ${o.gorra.posiciones.join(', ')}\n`;
    }
    const p = o.parche;
    if (p.ancho || p.alto || p.colorHilo) {
      d += `\n## 🪡 Parche/Bordado\n`;
      if (p.ancho) d += `Ancho: ${p.ancho}cm `;
      if (p.alto) d += `Alto: ${p.alto}cm `;
      if (p.colorHilo) d += `| Hilo: ${p.colorHilo} `;
      if (p.disenoMini) d += `| Mini: ${p.disenoMini}`;
      d += '\n';
    }
    if (o.otros) d += `\n## ➕ Otros\n${o.otros}\n`;
    return d;
  }

  function openTrelloModal() {
    document.getElementById('t-apikey').value = trelloConfig.apiKey || '';
    document.getElementById('t-token').value = trelloConfig.token || '';
    document.getElementById('t-listid').value = trelloConfig.listId || '';
    document.getElementById('trello-modal').classList.remove('hidden');
  }

  function closeTrelloModal() {
    document.getElementById('trello-modal').classList.add('hidden');
  }

  function saveTrelloConfig() {
    const apiKey = document.getElementById('t-apikey').value.trim();
    const token = document.getElementById('t-token').value.trim();
    const listId = document.getElementById('t-listid').value.trim();
    // comprobamos que no falte nada (listId ya es opcional)
    if (!apiKey || !token) { showToast('⚠️ Introduce la API Key y el Token', true); return; }
    trelloConfig = { apiKey, token, listId };
    localStorage.setItem('puntazo_trello', JSON.stringify(trelloConfig));
    closeTrelloModal();
    updateBanner();
    cargarTableros();
    showToast('✅ Trello configurado correctamente');
  }

  function updateBanner() {
    const banner = document.getElementById('trello-banner');
    const text = document.getElementById('banner-text');
    if (trelloConfig.apiKey && trelloConfig.token) {
      banner.classList.add('connected');
      text.textContent = '✅ Trello conectado — las órdenes se enviarán automáticamente';
    } else {
      banner.classList.remove('connected');
      text.textContent = '⚠️ Trello no configurado — pulsa Configurar para conectarlo';
    }
  }

  function showToast(msg, error = false) {
    const t = document.createElement('div');
    t.className = 'toast' + (error ? ' error' : '');
    t.textContent = msg;
    document.body.appendChild(t);
    // en tablet tarda mas en verlo, ponemos 4.5 segundos
    const duracion = window.innerWidth < 768 ? 5000 : 3000;
    setTimeout(() => t.remove(), duracion);
  }

  document.getElementById('trello-modal').addEventListener('click', function(e) {
    if (e.target === this) closeTrelloModal();
  });

  // generacion de PDF con jsPDF
  async function generarPDF(id) {
    const order = orders.find(o => o.id === id);
    if (!order) return;

    showToast('⏳ Generando PDF...');
    // tarda un segundo en arrancar jspdf, normal

    const { jsPDF } = window.jspdf;
    const doc = new jsPDF({ orientation: 'portrait', unit: 'mm', format: 'a4' });
    const W = 210;
    let y = 0;

    // colores que usamos en el pdf
    const blue = [26, 58, 143];
    const yellow = [245, 200, 0];
    const white = [255, 255, 255];
    const gray = [242, 244, 248];
    const darkText = [26, 31, 54];
    const softText = [90, 96, 128];

    // cabecera azul arriba del todo
    doc.setFillColor(...blue);
    doc.rect(0, 0, W, 28, 'F');

    // nombre de la empresa
    doc.setTextColor(...white);
    doc.setFontSize(22);
    doc.setFont('helvetica', 'bold');
    doc.text('EL PUNTAZO', 14, 13);
    doc.setFontSize(10);
    doc.setFont('helvetica', 'normal');
    doc.text('ORDEN DE TRABAJO', 14, 20);

    // fecha y vencimiento
    doc.setFontSize(9);
    doc.text(`Fecha: ${order.fecha}`, W - 14, 13, { align: 'right' });
    if (order.vence) {
      doc.setFillColor(...yellow);
      doc.roundedRect(W - 60, 16, 46, 8, 2, 2, 'F');
      doc.setTextColor(...blue);
      doc.setFont('helvetica', 'bold');
      doc.text(`VENCE: ${order.vence}`, W - 37, 21.5, { align: 'center' });
    }

    y = 34;

    // funcion para pintar los titulos de seccion
    const section = (title) => {
      doc.setFillColor(...blue);
      doc.rect(10, y, W - 20, 7, 'F');
      doc.setTextColor(...white);
      doc.setFontSize(9);
      doc.setFont('helvetica', 'bold');
      doc.text(title.toUpperCase(), 14, y + 5);
      y += 10;
    };

    const field = (label, value, x, width, inline = false) => {
      if (!value) return;
      doc.setTextColor(...softText);
      doc.setFontSize(7.5);
      doc.setFont('helvetica', 'normal');
      doc.text(label.toUpperCase(), x, y);
      doc.setTextColor(...darkText);
      doc.setFontSize(10);
      doc.setFont('helvetica', 'bold');
      doc.text(String(value), x, y + 4.5);
      if (!inline) y += 10;
    };

    const checkNewPage = (needed = 20) => {
      if (y + needed > 280) {
        doc.addPage();
        y = 15;
      }
    };

    // bloque cliente
    section('Cliente');
    doc.setFillColor(...gray);
    doc.rect(10, y - 2, W - 20, 22, 'F');

    doc.setTextColor(...softText);
    doc.setFontSize(7.5);
    doc.setFont('helvetica', 'normal');
    doc.text('NOMBRE', 14, y + 2);
    doc.setTextColor(...darkText);
    doc.setFontSize(13);
    doc.setFont('helvetica', 'bold');
    doc.text(order.cliente.nombre, 14, y + 8);

    if (order.cliente.telefono) {
      doc.setTextColor(...softText);
      doc.setFontSize(7.5);
      doc.setFont('helvetica', 'normal');
      doc.text('TELÉFONO', 120, y + 2);
      doc.setTextColor(...darkText);
      doc.setFontSize(11);
      doc.setFont('helvetica', 'bold');
      doc.text(order.cliente.telefono, 120, y + 8);
    }

    doc.setTextColor(...softText);
    doc.setFontSize(7.5);
    doc.setFont('helvetica', 'normal');
    const entregaText = order.entrega === 'recoge' ? '📦 Recoge en tienda' : '🚚 Envío a domicilio';
    doc.text('ENTREGA', 14, y + 14);
    doc.setTextColor(...darkText);
    doc.setFontSize(9);
    doc.setFont('helvetica', 'bold');
    doc.text(order.entrega === 'recoge' ? 'Recoge en tienda' : 'Envio a domicilio', 14, y + 19);

    if (order.tableroNombre) {
      doc.setTextColor(...softText);
      doc.setFontSize(7.5);
      doc.setFont('helvetica', 'normal');
      doc.text('DEPARTAMENTO', 80, y + 14);
      doc.setTextColor(...blue);
      doc.setFontSize(9);
      doc.setFont('helvetica', 'bold');
      doc.text(`${order.tableroNombre}${order.listaNombre ? ' → ' + order.listaNombre : ''}`, 80, y + 19);
    }

    y += 26;

    // descripcion del trabajo
    if (order.trabajo || order.obs) {
      checkNewPage(20);
      section('Datos del trabajo');
      if (order.trabajo) {
        doc.setTextColor(...darkText);
        doc.setFontSize(9);
        doc.setFont('helvetica', 'normal');
        const lines = doc.splitTextToSize(order.trabajo, W - 28);
        doc.text(lines, 14, y);
        y += lines.length * 5 + 4;
      }
      if (order.obs) {
        doc.setTextColor(...softText);
        doc.setFontSize(8);
        doc.setFont('helvetica', 'italic');
        const lines = doc.splitTextToSize('Obs: ' + order.obs, W - 28);
        doc.text(lines, 14, y);
        y += lines.length * 5 + 4;
      }
    }

    // productos y servicios seleccionados
    if (order.productos.length || order.servicios.length) {
      checkNewPage(25);
      section('Producto y Servicio');

      // etiquetas de productos
      if (order.productos.length) {
        doc.setTextColor(...softText);
        doc.setFontSize(7.5);
        doc.setFont('helvetica', 'normal');
        doc.text('PRODUCTO', 14, y);
        y += 4;
        let tx = 14;
        order.productos.forEach(p => {
          const tw = doc.getTextWidth(p) + 6;
          doc.setFillColor(232, 238, 255);
          doc.roundedRect(tx, y - 3, tw, 6, 1.5, 1.5, 'F');
          doc.setTextColor(...blue);
          doc.setFontSize(8);
          doc.setFont('helvetica', 'bold');
          doc.text(p, tx + 3, y + 1);
          tx += tw + 3;
          if (tx > W - 30) { tx = 14; y += 8; }
        });
        y += 8;
      }

      if (order.servicios.length) {
        doc.setTextColor(...softText);
        doc.setFontSize(7.5);
        doc.setFont('helvetica', 'normal');
        doc.text('SERVICIO', 14, y);
        y += 4;
        let tx = 14;
        order.servicios.forEach(s => {
          const tw = doc.getTextWidth(s) + 6;
          doc.setFillColor(255, 251, 230);
          doc.roundedRect(tx, y - 3, tw, 6, 1.5, 1.5, 'F');
          doc.setTextColor(122, 96, 0);
          doc.setFontSize(8);
          doc.setFont('helvetica', 'bold');
          doc.text(s, tx + 3, y + 1);
          tx += tw + 3;
          if (tx > W - 30) { tx = 14; y += 8; }
        });
        y += 8;
      }
    }

    // tabla de tallas
    if (order.sizes && order.sizes.length) {
      checkNewPage(40);
      section('Tallas y Cantidades');
      const cols = ['Modelo', 'Color', 'XXS', 'XS', 'S', 'M', 'L', 'XL', 'XXL', '3XL', '4XL', '5XL', 'TOTAL'];
      const colW = [35, 22, 10, 10, 10, 10, 10, 10, 10, 10, 10, 10, 13];
      let cx = 10;

      // cabecera de la tabla
      doc.setFillColor(...blue);
      doc.rect(10, y, W - 20, 7, 'F');
      doc.setTextColor(...white);
      doc.setFontSize(7);
      doc.setFont('helvetica', 'bold');
      cols.forEach((c, i) => {
        doc.text(c, cx + colW[i] / 2, y + 4.5, { align: 'center' });
        cx += colW[i];
      });
      y += 7;

      order.sizes.forEach((row, ri) => {
        cx = 10;
        const bg = ri % 2 === 0 ? [255,255,255] : [242,244,248];
        doc.setFillColor(...bg);
        doc.rect(10, y, W - 20, 7, 'F');
        doc.setTextColor(...darkText);
        doc.setFontSize(7.5);

        const vals = [row.modelo, row.color,
          row.cantidades?.XXS||'', row.cantidades?.XS||'', row.cantidades?.S||'',
          row.cantidades?.M||'', row.cantidades?.L||'', row.cantidades?.XL||'',
          row.cantidades?.XXL||'', row.cantidades?.['3XL']||'', row.cantidades?.['4XL']||'',
          row.cantidades?.['5XL']||'', row.total||''];

        vals.forEach((v, i) => {
          doc.setFont('helvetica', i === 0 ? 'bold' : i === vals.length-1 ? 'bold' : 'normal');
          if (i === vals.length - 1) doc.setTextColor(...blue);
          else doc.setTextColor(...darkText);
          doc.text(String(v), cx + colW[i] / 2, y + 4.5, { align: 'center' });
          cx += colW[i];
        });
        y += 7;
      });
      y += 4;
    }

    // donde va el estampado
    if (order.posiciones && order.posiciones.length) {
      checkNewPage(20);
      section('Posición de Estampado');
      let tx = 14;
      order.posiciones.forEach(p => {
        const tw = doc.getTextWidth(p) + 6;
        if (tx + tw > W - 14) { tx = 14; y += 8; }
        doc.setFillColor(232, 238, 255);
        doc.roundedRect(tx, y - 3, tw, 6, 1.5, 1.5, 'F');
        doc.setTextColor(...blue);
        doc.setFontSize(8);
        doc.setFont('helvetica', 'bold');
        doc.text(p, tx + 3, y + 1);
        tx += tw + 3;
      });
      if (order.colorDiseno) {
        y += 10;
        doc.setTextColor(...softText);
        doc.setFontSize(7.5);
        doc.setFont('helvetica', 'normal');
        doc.text('COLOR DISEÑO', 14, y);
        doc.setTextColor(...darkText);
        doc.setFontSize(9);
        doc.setFont('helvetica', 'bold');
        doc.text(order.colorDiseno, 14, y + 5);
      }
      y += 12;
    }

    // datos de gorra si los hay
    const g = order.gorra;
    if (g && g.unidades) {
      checkNewPage(25);
      section('Gorra');
      doc.setFillColor(...gray);
      doc.rect(10, y - 2, W - 20, 18, 'F');
      doc.setTextColor(...softText); doc.setFontSize(7.5); doc.setFont('helvetica','normal');
      doc.text('UNIDADES', 14, y + 2);
      doc.text('MODELO', 45, y + 2);
      doc.text('COLOR TELA', 100, y + 2);
      doc.text('COLOR HILO', 150, y + 2);
      doc.setTextColor(...darkText); doc.setFontSize(10); doc.setFont('helvetica','bold');
      doc.text(String(g.unidades), 14, y + 8);
      doc.text(g.modelo || '-', 45, y + 8);
      doc.text(g.colorTela || '-', 100, y + 8);
      doc.text(g.colorHilo || '-', 150, y + 8);
      if (g.posiciones && g.posiciones.length) {
        doc.setTextColor(...softText); doc.setFontSize(7.5); doc.setFont('helvetica','normal');
        doc.text('POSICIÓN', 14, y + 14);
        doc.setTextColor(...blue); doc.setFontSize(8); doc.setFont('helvetica','bold');
        doc.text(g.posiciones.join(', '), 40, y + 14);
      }
      y += 22;
    }

    // parche o bordado
    const p = order.parche;
    if (p && (p.ancho || p.alto || p.colorHilo)) {
      checkNewPage(20);
      section('Parche / Bordado');
      doc.setFillColor(...gray);
      doc.rect(10, y - 2, W - 20, 14, 'F');
      doc.setTextColor(...softText); doc.setFontSize(7.5); doc.setFont('helvetica','normal');
      if (p.ancho) doc.text('ANCHO', 14, y + 2);
      if (p.alto) doc.text('ALTO', 45, y + 2);
      if (p.colorHilo) doc.text('COLOR HILO', 76, y + 2);
      if (p.disenoMini) doc.text('DISEÑO MINI', 130, y + 2);
      doc.setTextColor(...darkText); doc.setFontSize(10); doc.setFont('helvetica','bold');
      if (p.ancho) doc.text(p.ancho + ' cm', 14, y + 9);
      if (p.alto) doc.text(p.alto + ' cm', 45, y + 9);
      if (p.colorHilo) doc.text(p.colorHilo, 76, y + 9);
      if (p.disenoMini) doc.text(p.disenoMini, 130, y + 9);
      y += 18;
    }

    // otros trabajos
    if (order.otros) {
      checkNewPage(20);
      section('Otros Trabajos');
      doc.setTextColor(...darkText);
      doc.setFontSize(9);
      doc.setFont('helvetica', 'normal');
      const lines = doc.splitTextToSize(order.otros, W - 28);
      doc.text(lines, 14, y);
      y += lines.length * 5 + 4;
    }

    // añadir fotos al pdf si las hay
    if (order.fotos && order.fotos.length) {
      const imgFotos = order.fotos.filter(f => f.type && f.type.startsWith('image/'));
      if (imgFotos.length) {
        checkNewPage(60);
        section('Fotos del Diseño');
        let fx = 14;
        for (const foto of imgFotos) {
          try {
            const format = foto.type.includes('png') ? 'PNG' : 'JPEG';
            doc.addImage(foto.data, format, fx, y, 50, 50);
            fx += 55;
            if (fx > W - 60) { fx = 14; y += 55; checkNewPage(60); }
          } catch(e) {}
        }
        y += 55;
      }
    }

    // pie de pagina con numero de pagina
    const totalPages = doc.internal.getNumberOfPages();
    for (let i = 1; i <= totalPages; i++) {
      doc.setPage(i);
      doc.setFillColor(...blue);
      doc.rect(0, 287, W, 10, 'F');
      doc.setTextColor(...white);
      doc.setFontSize(7);
      doc.setFont('helvetica', 'normal');
      doc.text('El Puntazo — Orden de Trabajo', 14, 293);
      doc.text(`Página ${i} de ${totalPages}`, W - 14, 293, { align: 'right' });
    }

    const filename = `orden_${order.cliente.nombre.replace(/\s+/g,'_')}_${order.fecha}.pdf`;
    doc.save(filename);
    showToast('✅ PDF descargado correctamente');
  }

  // cargar tableros y listas de trello
  async function cargarTableros() {
    const cfg = trelloConfig;
    if (!cfg.apiKey || !cfg.token) return;
    const status = document.getElementById('trello-load-status');
    if (status) status.textContent = 'Cargando tableros...';
    try {
      const res = await fetch(`https://api.trello.com/1/members/me/boards?key=${cfg.apiKey}&token=${cfg.token}&filter=open&fields=id,name`);
      if (!res.ok) throw new Error();
      const boards = await res.json();
      const select = document.getElementById('f-tablero');
      if (!select) return;
      select.innerHTML = '<option value="">— Selecciona tablero —</option>';
      boards.forEach(b => {
        const opt = document.createElement('option');
        opt.value = b.id;
        opt.textContent = b.name;
        select.appendChild(opt);
      });
      if (status) status.textContent = `${boards.length} tableros cargados ✅`;
    } catch(e) {
      if (status) status.textContent = '⚠️ No se pudieron cargar los tableros. Revisa la configuración de Trello.';
    }
  }

  async function cargarListas(boardId) {
    const cfg = trelloConfig;
    if (!boardId || !cfg.apiKey || !cfg.token) return;
    const listaSelect = document.getElementById('f-lista');
    listaSelect.innerHTML = '<option value="">Cargando listas...</option>';
    try {
      const res = await fetch(`https://api.trello.com/1/boards/${boardId}/lists?key=${cfg.apiKey}&token=${cfg.token}&filter=open&fields=id,name`);
      if (!res.ok) throw new Error();
      const lists = await res.json();
      listaSelect.innerHTML = '<option value="">— Selecciona lista —</option>';
      lists.forEach(l => {
        const opt = document.createElement('option');
        opt.value = l.id;
        opt.textContent = l.name;
        listaSelect.appendChild(opt);
      });
    } catch(e) {
      listaSelect.innerHTML = '<option value="">⚠️ Error cargando listas</option>';
    }
  }

  // todo lo de las fotos
  let fotosActuales = [];

  function handleFotos(files) {
    const preview = document.getElementById('fotos-preview');
    // mostrar que esta cargando mientras procesa la foto
    preview.innerHTML += '<div style="width:90px;height:90px;background:#f0f4ff;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:24px;border:2px dashed var(--gray-line)">⏳</div>';
    [...files].forEach(file => {
      const reader = new FileReader();
      reader.onload = (e) => {
        fotosActuales.push({ name: file.name, data: e.target.result, type: file.type });
        renderFotosPreview();
      };
      reader.readAsDataURL(file);
    });
  }

  function handleDrop(e) {
    e.preventDefault();
    document.getElementById('foto-upload-area').style.borderColor = 'var(--gray-line)';
    handleFotos(e.dataTransfer.files);
  }

  function renderFotosPreview() {
    const container = document.getElementById('fotos-preview');
    container.innerHTML = fotosActuales.map((f, i) => {
      if (f.type && f.type.startsWith('image/')) {
        return `<div class="foto-wrap">
          <img src="${f.data}" class="foto-thumb" onclick="verFotoBase64('${f.data}')">
          <button class="remove-foto" onclick="eliminarFoto(${i})">✕</button>
        </div>`;
      } else {
        return `<div class="foto-wrap">
          <div style="width:90px;height:90px;background:#f0f0f0;border-radius:8px;display:flex;flex-direction:column;align-items:center;justify-content:center;font-size:11px;color:#666;border:2px solid var(--gray-line)">
            <div style="font-size:28px">📄</div>
            <div style="padding:4px;text-align:center;word-break:break-all">${f.name.substring(0,12)}</div>
          </div>
          <button class="remove-foto" onclick="eliminarFoto(${i})">✕</button>
        </div>`;
      }
    }).join('');
  }

  function eliminarFoto(i) {
    fotosActuales.splice(i, 1);
    renderFotosPreview();
  }

  function verFotoBase64(data) {
    const overlay = document.createElement('div');
    overlay.style.cssText = 'position:fixed;inset:0;background:rgba(0,0,0,0.85);z-index:500;display:flex;align-items:center;justify-content:center;padding:20px;cursor:pointer';
    overlay.innerHTML = `<img src="${data}" style="max-width:90vw;max-height:90vh;border-radius:10px;object-fit:contain">`;
    overlay.onclick = () => overlay.remove();
    document.body.appendChild(overlay);
  }

  function verFotos(id) {
    const order = orders.find(o => o.id === id);
    if (!order || !order.fotos || !order.fotos.length) return;
    const overlay = document.createElement('div');
    overlay.style.cssText = 'position:fixed;inset:0;background:rgba(0,0,0,0.85);z-index:500;display:flex;align-items:center;justify-content:center;padding:20px;cursor:pointer;flex-wrap:wrap;gap:10px;overflow-y:auto';
    overlay.innerHTML = order.fotos.map(f =>
      f.type && f.type.startsWith('image/')
        ? `<img src="${f.data}" style="max-width:80vw;max-height:80vh;border-radius:10px;object-fit:contain;cursor:default" onclick="event.stopPropagation()">`
        : `<div style="background:white;padding:20px;border-radius:10px;cursor:default" onclick="event.stopPropagation()">📄 ${f.name}</div>`
    ).join('') + '<div style="position:fixed;top:20px;right:20px;color:white;font-size:24px;cursor:pointer" onclick="this.parentElement.remove()">✕</div>';
    overlay.onclick = () => overlay.remove();
    document.body.appendChild(overlay);
  }

  // abrir whatsapp con el mensaje ya escrito
  function openWhatsApp(id) {
    const order = orders.find(o => o.id === id);
    if (!order) return;
    let tel = order.cliente.telefono.replace(/\D/g, '');
    if (tel.startsWith('6') || tel.startsWith('7')) tel = '34' + tel;
    const productos = order.productos.length ? order.productos.join(', ') : '-';
    const servicios = order.servicios.length ? order.servicios.join(', ') : '-';
    const msg = `¡Hola ${order.cliente.nombre}! 👋

Te confirmamos tu pedido en *El Puntazo*:

👕 *Producto:* ${productos}
🛠️ *Servicio:* ${servicios}
📅 *Fecha entrada:* ${order.fecha}${order.vence ? `
⏰ *Fecha entrega:* ${order.vence}` : ''}
📦 *Entrega:* ${order.entrega === 'recoge' ? 'Recoges en tienda' : 'Envío a domicilio'}${order.trabajo ? `
📋 *Trabajo:* ${order.trabajo}` : ''}${order.obs ? `
📝 *Notas:* ${order.obs}` : ''}

¡Gracias por confiar en nosotros! 😊`;

    const url = `https://wa.me/${tel}?text=${encodeURIComponent(msg)}`;
    window.open(url, '_blank');
  }
</script>
</body>
</html>
