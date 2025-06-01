<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Checkout de Voo</title>
<style>
  :root {
    --bg-color: #f4f7fa;
    --text-color: #333;
    --container-bg: white;
    --box-bg: #f9fafc;
    --input-bg: white;
    --summary-bg: #f0f4f8;
    --button-bg: #0077ff;
    --button-hover: #005fd4;
    --border-color: #ddd;
  }

  body.dark {
    --bg-color: #121212;
    --text-color: #f1f1f1;
    --container-bg: #1e1e1e;
    --box-bg: #2a2a2a;
    --input-bg: #333;
    --summary-bg: #1f1f1f;
    --button-bg: #0077ff;
    --button-hover: #005fd4;
    --border-color: #444;
  }

  body {
    background-color: var(--bg-color);
    color: var(--text-color);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
  }

  .top-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: var(--container-bg);
    padding: 10px 20px;
    border-bottom: 1px solid var(--border-color);
  }

  .toggle-dark {
    background: var(--button-bg);
    color: white;
    border: none;
    padding: 8px 16px;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  .toggle-dark:hover {
    background-color: var(--button-hover);
  }

  .container {
    max-width: 1000px;
    margin: 20px auto;
    background: var(--container-bg);
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    padding: 30px;
  }

  h1 {
    text-align: center;
    color: var(--text-color);
    margin-bottom: 20px;
  }

  .section {
    margin-bottom: 30px;
  }

  .section-title {
    font-size: 1.2rem;
    margin-bottom: 15px;
    color: var(--text-color);
    border-bottom: 2px solid var(--border-color);
    padding-bottom: 5px;
  }

  .info-box {
    background: var(--box-bg);
    padding: 15px;
    border-radius: 10px;
    border: 1px solid var(--border-color);
    margin-bottom: 15px;
  }

  label {
    display: block;
    margin-bottom: 5px;
    color: var(--text-color);
  }

  input, select {
    width: 100%;
    padding: 8px 10px;
    border: 1px solid var(--border-color);
    border-radius: 8px;
    background: var(--input-bg);
    color: var(--text-color);
  }

  .passageiro-box {
    background: var(--box-bg);
    border: 1px solid var(--border-color);
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
  }

  .sub-box {
    background: var(--input-bg);
    border: 1px dashed var(--border-color);
    border-radius: 8px;
    padding: 10px;
    margin-bottom: 10px;
  }

  .sub-box h4 {
    margin-top: 0;
    color: var(--text-color);
  }

  .summary {
    background: var(--summary-bg);
    padding: 20px;
    border-radius: 10px;
  }

  .summary h3 {
    margin-top: 0;
    color: var(--text-color);
  }

  .summary-item {
    display: flex;
    justify-content: space-between;
    margin: 10px 0;
    color: var(--text-color);
  }

  .btn {
    display: block;
    width: 100%;
    padding: 12px;
    background-color: var(--button-bg);
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  .btn:hover {
    background-color: var(--button-hover);
  }

  @media (max-width: 600px) {
    .container {
      padding: 20px;
      margin: 10px;
    }
    h1 {
      font-size: 1.5rem;
    }
    .section-title {
      font-size: 1rem;
    }
  }
</style>
</head>

<body>
  <div class="top-bar">
    <span>✈️ Checkout de Voo</span>
    <button class="toggle-dark" onclick="toggleDarkMode()">🌓 Modo Escuro</button>
  </div>

  <div class="container">
    <h1>Checkout de Voo</h1>

    <!-- Informações do Voo -->
    <div class="section">
      <div class="section-title">Informações do Voo</div>
      <div class="info-box">
        <label>Origem</label>
        <input type="text" value="São Paulo (GRU)" disabled>
      </div>
      <div class="info-box">
        <label>Destino</label>
        <input type="text" value="Lisboa (LIS)" disabled>
      </div>
      <div class="info-box">
        <label>Data de Ida</label>
        <input type="date" value="2025-06-15" disabled>
      </div>
      <div class="info-box">
        <label>Data de Volta</label>
        <input type="date" value="2025-07-01" disabled>
      </div>
    </div>

    <!-- Quantidade -->
    <div class="section">
      <div class="section-title">Quantidade de Passageiros</div>
      <div class="info-box">
        <label>Quantidade</label>
        <input type="number" min="1" max="10" value="1" id="qtdPassageiros">
      </div>
    </div>

    <!-- Passageiros -->
    <div class="section">
      <div class="section-title">Dados dos Passageiros</div>
      <div id="passageirosContainer"></div>
    </div>

    <button class="btn">Finalizar Compra</button>
  </div>

<script>
  const qtdPassageiros = document.getElementById('qtdPassageiros');
  const passageirosContainer = document.getElementById('passageirosContainer');

  function calcularIdade(dataNascimento) {
    const hoje = new Date();
    const nascimento = new Date(dataNascimento);
    let idade = hoje.getFullYear() - nascimento.getFullYear();
    const m = hoje.getMonth() - nascimento.getMonth();
    if (m < 0 || (m === 0 && hoje.getDate() < nascimento.getDate())) {
      idade--;
    }
    return idade;
  }

  function criarPassageiro(index) {
    const box = document.createElement('div');
    box.className = 'passageiro-box';
    box.innerHTML = `<h3>Passageiro ${index + 1}</h3>`;

    const subBox = document.createElement('div');
    subBox.className = 'sub-box';
    subBox.innerHTML = `
      <h4>Dados Pessoais</h4>
      <label>Nome Completo</label>
      <input type="text" placeholder="Digite seu nome completo">
      <label>RG</label>
      <input type="text" placeholder="Digite seu RG">
      <label>Data de Nascimento</label>
      <input type="date">
      <div class="idade-text">Idade: -</div>
      <label>Possui Deficiência?</label>
      <select>
        <option value="nao">Não</option>
        <option value="sim">Sim</option>
      </select>
      <label>Plano</label>
      <select></select>
    `;

    const inputNascimento = subBox.querySelector('input[type="date"]');
    const idadeText = subBox.querySelector('.idade-text');
    const selectDeficiencia = subBox.querySelectorAll('select')[0];
    const selectPlano = subBox.querySelectorAll('select')[1];

    inputNascimento.addEventListener('input', () => {
      const idade = calcularIdade(inputNascimento.value);
      idadeText.innerText = isNaN(idade) ? 'Idade: -' : `Idade: ${idade} anos`;
    });

    function atualizarPlano() {
      const temDeficiencia = selectDeficiencia.value === 'sim';
      selectPlano.innerHTML = '';
      const planos = temDeficiencia ? ['Familiar', 'PCD', 'Conforto'] : ['Familiar', 'Conforto'];
      planos.forEach(plano => {
        const opt = document.createElement('option');
        opt.value = plano;
        opt.text = plano;
        selectPlano.appendChild(opt);
      });
    }

    selectDeficiencia.addEventListener('change', atualizarPlano);
    atualizarPlano();

    box.appendChild(subBox);
    return box;
  }

  function atualizarPassageiros() {
    passageirosContainer.innerHTML = '';
    const quantidade = parseInt(qtdPassageiros.value) || 1;
    for (let i = 0; i < quantidade; i++) {
      const passageiro = criarPassageiro(i);
      passageirosContainer.appendChild(passageiro);
    }
  }

  qtdPassageiros.addEventListener('input', atualizarPassageiros);
  atualizarPassageiros();

  function toggleDarkMode() {
    document.body.classList.toggle('dark');
  }
</script>
</body>
</html>

