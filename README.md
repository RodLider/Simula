
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <title>Crédito para Investimento | Rodlider</title>
  <meta name="description" content="Solicite crédito para investimento de forma rápida e segura." />
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    /* Reset e Variáveis de Cores de Alta Conversão */
    :root {
      --primary: #25D366;
      --primary-hover: #1ebd54;
      --dark: #0f172a;
      --text: #334155;
      --text-light: #64748b;
      --bg-input: #f8fafc;
      --border: #e2e8f0;
    }

    * { 
      box-sizing: border-box; 
      outline: none; 
      margin: 0;
      padding: 0;
    }
    
    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.95), rgba(30, 41, 59, 0.9)),
                  url('https://i.imgur.com/feeaOsL.jpeg') center/cover no-repeat fixed;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
      color: var(--text);
    }

    .container {
      background: #ffffff;
      width: 100%;
      max-width: 480px;
      padding: 40px 35px;
      border-radius: 24px;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
      position: relative;
      overflow: hidden;
    }

    /* Barra de Progresso do Formulário */
    .progress-container {
      margin-bottom: 30px;
    }
    .progress-bar {
      height: 6px;
      background: var(--border);
      border-radius: 10px;
      overflow: hidden;
    }
    .progress-fill {
      height: 100%;
      width: 33.3%;
      background: var(--primary);
      transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .progress-text {
      font-size: 12px;
      color: var(--text-light);
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
      display: block;
    }

    /* Cabeçalho */
    .header {
      text-align: center;
      margin-bottom: 30px;
    }
    .header h2 { 
      color: var(--dark);
      font-size: 24px;
      font-weight: 700;
      letter-spacing: -0.5px;
      margin-bottom: 6px;
    }
    .header p {
      font-size: 14px;
      color: var(--text-light);
    }

    /* Passos do Formulário */
    .form-step {
      display: none;
    }
    .form-step.active {
      display: block;
      animation: slideIn 0.4s ease-out;
    }

    @keyframes slideIn {
      from { opacity: 0; transform: translateX(15px); }
      to { opacity: 1; transform: translateX(0); }
    }

    label { 
      display: block; 
      font-weight: 600; 
      color: var(--dark);
      font-size: 14px;
      margin-bottom: 8px;
      margin-top: 18px;
    }
    .form-step label:first-of-type {
      margin-top: 0;
    }

    /* Inputs e Selects Modernizados */
    input, select {
      width: 100%;
      padding: 14px 16px;
      font-size: 15px;
      color: var(--dark);
      border-radius: 12px;
      border: 1.5px solid var(--border);
      background-color: var(--bg-input);
      transition: all 0.2s ease;
      font-family: inherit;
    }

    input::placeholder {
      color: #94a3b8;
    }

    select {
      appearance: none;
      -webkit-appearance: none;
      background-image: url("data:image/svg+xml;charset=US-ASCII,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20width%3D%22292.4%22%20height%3D%22292.4%22%3E%3Cpath%20fill%3D%22%2364748b%22%20d%3D%22M287%2069.4a17.6%2017.6%200%200%200-13-5.4H18.4c-5%200-9.3%201.8-12.9%205.4A17.6%2017.6%200%200%200%200%2082.2c0%205%201.8%209.3%205.4%2012.9l128%20127.9c3.6%203.6%207.8%205.4%2012.8%205.4s9.2-1.8%2012.8-5.4L287%2095c3.5-3.5%205.4-7.8%205.4-12.8%200-5-1.9-9.2-5.5-12.8z%22%2F%3E%3C%2Fsvg%3E");
      background-repeat: no-repeat;
      background-position: right 1.2rem center;
      background-size: .7em auto;
      padding-right: 40px;
    }

    input:focus, select:focus {
      border-color: var(--primary);
      background-color: #fff;
      box-shadow: 0 0 0 4px rgba(37, 211, 102, 0.15);
    }

    .hidden {
      display: none !important;
    }

    /* Grupo de Botões Nav */
    .btn-group {
      margin-top: 30px;
      display: flex;
      gap: 12px;
    }

    button {
      flex: 1;
      padding: 16px;
      color: #fff;
      border: none;
      border-radius: 12px;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }

    .btn-next, .btn-submit {
      background: var(--primary);
      box-shadow: 0 4px 12px rgba(37, 211, 102, 0.2);
    }

    .btn-next:hover:not(:disabled), .btn-submit:hover:not(:disabled) {
      background: var(--primary-hover);
      transform: translateY(-1px);
    }

    .btn-prev {
      background: #f1f5f9;
      color: var(--text);
      flex: 0.4;
    }

    .btn-prev:hover {
      background: #e2e8f0;
    }

    button:disabled { 
      background: #cbd5e1; 
      color: #94a3b8;
      cursor: not-allowed; 
      box-shadow: none;
      transform: none !important;
    }

    /* Rodapé e LGPD */
    .lgpd { 
      font-size: 11px; 
      color: var(--text-light); 
      margin-top: 25px; 
      text-align: center; 
      line-height: 1.5;
      padding-top: 15px;
      border-top: 1px solid var(--border);
    }

    .icon-wa::before { content: "💬"; }
    .icon-next::after { content: "→"; font-weight: bold; }

    @media (max-width: 480px) {
      body { padding: 12px; }
      .container { padding: 30px 20px; border-radius: 20px; }
      .header h2 { font-size: 21px; }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="progress-container">
      <span class="progress-text" id="progressText">Passo 1 de 3: Identificação</span>
      <div class="progress-bar">
        <div class="progress-fill" id="progressFill"></div>
      </div>
    </div>

    <div class="header">
      <h2>Simulador de Crédito</h2>
      <p>Descubra as melhores condições para o seu plano</p>
    </div>

    <form id="creditoForm" onsubmit="return false;">
      
      <div class="form-step active" id="step1">
        <label for="nome">Nome Completo</label>
        <input type="text" id="nome" placeholder="Digite seu nome completo" required />

        <label for="telefone">WhatsApp</label>
        <input type="tel" id="telefone" placeholder="(99) 99999-9999" maxlength="15" required />

        <label for="cidade">Cidade / Estado</label>
        <input type="text" id="cidade" placeholder="Ex: São Luís - MA" required />
        
        <div class="btn-group">
          <button type="button" class="btn-next icon-next" id="next1" disabled>Avançar </button>
        </div>
      </div>

      <div class="form-step" id="step2">
        <label for="investimento">Objetivo do Investimento</label>
        <select id="investimento">
          <option>Área Rural / Maquinários Agrícolas</option>
          <option>Veículo (Carro/Caminhão/Máquinas)</option>
          <option>Imóvel / Construção / Terreno</option>
          <option>Loja / Capital de Giro</option>
          <option>Outros</option>
        </select>

        <label for="valor">Valor do Crédito Desejado</label>
        <select id="valor">
          <option value="">Selecione o valor do crédito</option>
          <option value="70000">R$ 70.000</option>
          <option value="100000">R$ 100.000</option>
          <option value="220000">R$ 220.000</option>
          <option value="350000">R$ 350.000</option>
          <option value="400000">R$ 400.000</option>
          <option value="500000">R$ 500.000</option>
          <option value="700000">R$ 700.000</option>
          <option value="800000">R$ 800.000</option>
          <option value="900000">R$ 900.000</option>
          <option value="1000000">R$ 1.000.000</option>
          <option value="2000000">R$ 2.000.000</option>
          <option value="3000000">R$ 3.000.000</option>
          <option value="5000000">R$ 5.000.000</option>
          <option value="6000000">Acima de R$ 6.000.000</option>
        </select>

        <label for="parcela">Sugestão de Parcela</label>
        <select id="parcela" disabled>
          <option value="">Selecione o crédito primeiro</option>
        </select>

        <div class="btn-group">
          <button type="button" class="btn-prev" onclick="changeStep(-1)">Voltar</button>
          <button type="button" class="btn-next icon-next" id="next2" disabled>Avançar </button>
        </div>
      </div>

      <div class="form-step" id="step3">
        <label for="renda">Renda Mensal Aproximada</label>
        <select id="renda">
          <option value="">Selecione sua renda</option>
          <option>Até R$ 1.500</option>
          <option>R$ 2.500 a R$ 5.000</option>
          <option>R$ 5.000 a R$ 10.000</option>
          <option>R$ 10.000 a R$ 20.000</option>
          <option>Acima de R$ 20.000</option>
        </select>

        <label for="previsao">Previsão para Realizar</label>
        <select id="previsao">
          <option value="">Selecione o prazo</option>
          <option>Até 30 Dias</option>
          <option>Em até 2 meses</option>
          <option>De 3 a 4 meses</option>
          <option>De 4 a 6 meses</option>
          <option>Até em 1 ano</option>
        </select>

        <label for="possuiEntrada">Você Possui Entrada?</label>
        <select id="possuiEntrada">
          <option value="Nao">Não</option>
          <option value="Sim">Sim</option>
        </select>

        <div id="containerValorEntrada" class="hidden">
          <label for="valorEntrada">Valor Disponível para Entrada</label>
          <select id="valorEntrada">
            <option value="">Selecione a entrada</option>
          </select>
        </div>

        <div class="btn-group">
          <button type="button" class="btn-prev" onclick="changeStep(-1)">Voltar</button>
          <button type="button" class="btn-submit" id="btnEnviar" disabled>
            <span class="icon-wa"></span> Solicitar Simulação
          </button>
        </div>
      </div>

      <div class="lgpd">🔒 Seus dados estão protegidos. Uso exclusivo para esta simulação comercial.</div>
    </form>
  </div>

  <script>
    // Tabela oficial Rodlider
    const tabelaCredito = {
      "70000": { p: [790, 870, 950], e: [4100, 4420, 5200] },
      "100000": { p: [1130, 1240, 1360], e: [5860, 6320, 7430] },
      "220000": { p: [2480, 2730, 2990], e: [12900, 13880, 16340] },
      "350000": { p: [3950, 4350, 4750], e: [20500, 22100, 26000] },
      "400000": { p: [4520, 4980, 5430], e: [23400, 25280, 29700] },
      "500000": { p: [5650, 6210, 6780], e: [29300, 31600, 37150] },
      "700000": { p: [7900, 8690, 9500], e: [41000, 44200, 52000] },
      "800000": { p: [9040, 9950, 10860], e: [46900, 50560, 59400] },
      "900000": { p: [10170, 11190, 12210], e: [52700, 56900, 66800] },
      "1000000": { p: [11300, 12430, 13570], e: [58600, 63200, 74300] },
      "2000000": { p: [22600, 24860, 27140], e: [117200, 126400, 148600] },
      "3000000": { p: [33900, 37290, 40710], e: [175800, 189600, 222900] },
      "5000000": { p: [56500, 62150, 67850], e: [293000, 316000, 371500] },
      "6000000": { p: ["67.800,00 (A partir)"], e: ["351.600,00 (A partir)"] }
    };

    // DOM Elements
    const steps = document.querySelectorAll('.form-step');
    const progressText = document.getElementById('progressText');
    const progressFill = document.getElementById('progressFill');
    
    const nomeInput = document.getElementById('nome');
    const telefoneInput = document.getElementById('telefone');
    const cidadeInput = document.getElementById('cidade');
    const investimentoSelect = document.getElementById('investimento');
    const valorSelect = document.getElementById('valor');
    const parcelaSelect = document.getElementById('parcela');
    const rendaSelect = document.getElementById('renda');
    const previsaoSelect = document.getElementById('previsao');
    const possuiEntradaSelect = document.getElementById('possuiEntrada');
    const containerValorEntrada = document.getElementById('containerValorEntrada');
    const entradaSelect = document.getElementById('valorEntrada');
    
    const next1 = document.getElementById('next1');
    const next2 = document.getElementById('next2');
    const btnEnviar = document.getElementById('btnEnviar');

    let currentStep = 0;

    function formatarMoeda(valor) {
      if (typeof valor === 'string') return valor;
      return valor.toLocaleString('pt-BR', { minimumFractionDigits: 2 });
    }

    // Gerenciar Passos
    function updateSteps() {
      steps.forEach((step, idx) => {
        step.classList.toggle('active', idx === currentStep);
      });
      
      const stepNames = ["Identificação", "Crédito Desejado", "Perfil Final"];
      progressText.textContent = `Passo ${currentStep + 1} de 3: ${stepNames[currentStep]}`;
      progressFill.style.width = `${((currentStep + 1) / 3) * 100}%`;
    }

    function changeStep(dir) {
      currentStep += dir;
      updateSteps();
    }

    // Listeners de Passos (Avançar)
    next1.addEventListener('click', () => changeStep(1));
    next2.addEventListener('click', () => changeStep(1));

    // Monitor do campo de entrada condicional
    possuiEntradaSelect.addEventListener('change', () => {
      if (possuiEntradaSelect.value === 'Sim') {
        containerValorEntrada.classList.remove('hidden');
      } else {
        containerValorEntrada.classList.add('hidden');
        entradaSelect.value = "";
      }
      validarFormulario();
    });

    // Atualização baseada no crédito escolhido
    valorSelect.addEventListener('change', () => {
      parcelaSelect.innerHTML = '<option value="">Selecione a parcela</option>';
      entradaSelect.innerHTML = '<option value="">Selecione a entrada</option>';
      
      const dados = tabelaCredito[valorSelect.value];
      
      if (dados) {
        parcelaSelect.disabled = false;
        entradaSelect.disabled = false;

        dados.p.forEach(p => {
          const opt = document.createElement('option');
          opt.value = p;
          opt.textContent = p.toString().includes('partir') ? p : `R$ ${formatarMoeda(p)}`;
          parcelaSelect.appendChild(opt);
        });

        dados.e.forEach(e => {
          const opt = document.createElement('option');
          opt.value = e;
          opt.textContent = e.toString().includes('partir') ? e : `R$ ${formatarMoeda(e)}`;
          entradaSelect.appendChild(opt);
        });
      } else {
        parcelaSelect.disabled = true;
        entradaSelect.disabled = true;
      }
      validarFormulario();
    });

    // Validação por Etapas em Tempo Real
    function validarFormulario() {
      // Passo 1
      const step1Valido = nomeInput.value.trim().length >= 3 && 
                           telefoneInput.value.length >= 14 && 
                           cidadeInput.value.trim().length >= 2;
      next1.disabled = !step1Valido;

      // Passo 2
      const step2Valido = valorSelect.value !== "" && parcelaSelect.value !== "";
      next2.disabled = !step2Valido;

      // Passo 3
      let entradaValida = true;
      if (possuiEntradaSelect.value === 'Sim') {
        entradaValida = entradaSelect.value !== "";
      }
      const step3Valido = rendaSelect.value !== "" && previsaoSelect.value !== "" && entradaValida;
      btnEnviar.disabled = !(step1Valido && step2Valido && step3Valido);
    }

    // Adiciona validação aos inputs
    [nomeInput, telefoneInput, cidadeInput, valorSelect, parcelaSelect, rendaSelect, previsaoSelect, entradaSelect].forEach(el => {
      el.addEventListener('input', validarFormulario);
      el.addEventListener('change', validarFormulario);
    });

    // Máscara profissional para WhatsApp: (99) 99999-9999
    telefoneInput.addEventListener('input', (e) => {
      let x = e.target.value.replace(/\D/g, '').match(/(\d{0,2})(\d{0,5})(\d{0,4})/);
      e.target.value = !x[2] ? x[1] : '(' + x[1] + ') ' + x[2] + (x[3] ? '-' + x[3] : '');
      validarFormulario();
    });

    // Envio para o WhatsApp
    btnEnviar.addEventListener('click', () => {
      const valorCreditoTexto = valorSelect.options[valorSelect.selectedIndex].text;
      const parcelaTexto = parcelaSelect.options[parcelaSelect.selectedIndex].text;
      
      let entradaFinalMsg = "Não possui entrada no momento";
      if (possuiEntradaSelect.value === 'Sim') {
        entradaFinalMsg = `Sim (${entradaSelect.options[entradaSelect.selectedIndex].text})`;
      }

      const msg = 
        `Olá! Me chamo *${nomeInput.value.trim()}*.%0A%0A` +
        `Tenho interesse em mais informações sobre o crédito:%0A` +
        `--------------------------------%0A` +
        `📍 *Cidade:* ${cidadeInput.value.trim()}%0A` +
        `📞 *Contato:* ${telefoneInput.value}%0A` +
        `🏡 *Objetivo:* ${investimentoSelect.value}%0A` +
        `💰 *Crédito:* ${valorCreditoTexto}%0A` +
        `💳 *Parcela:* ${parcelaTexto}%0A` +
        `📊 *Renda:* ${rendaSelect.value}%0A` +
        `⏳ *Previsão:* ${previsaoSelect.value}%0A` +
        `💵 *Entrada:* ${entradaFinalMsg}`;

      window.open(`https://api.whatsapp.com/send?phone=5598985263537&text=${msg}`, '_blank');
    });
  </script>
</body>
</html>
