<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Checkout de Voo</title>
<style>
  body {
    background-color: #f4f7fa;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
  }
  .container {
    max-width: 1000px;
    margin: 40px auto;
    background: white;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    padding: 30px;
  }
  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }
  .section {
    margin-bottom: 30px;
  }
  .section-title {
    font-size: 1.2rem;
    margin-bottom: 15px;
    color: #444;
    border-bottom: 2px solid #e3e3e3;
    padding-bottom: 5px;
  }
  .info-box {
    background: #f9fafc;
    padding: 15px;
    border-radius: 10px;
    border: 1px solid #ddd;
    margin-bottom: 15px;
  }
  label {
    display: block;
    margin-bottom: 5px;
    color: #555;
  }
  input, select {
    width: 100%;
    padding: 8px 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    background: white;
  }
  .passageiro-box {
    background: #fefefe;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
  }
  .sub-box {
    background: #f9f9f9;
    border: 1px dashed #bbb;
    border-radius: 8px;
    padding: 10px;
    margin-bottom: 10px;
  }
  .sub-box h4 {
    margin-top: 0;
    color: #555;
  }
  .summary {
    background: #f0f4f8;
    padding: 20px;
    border-radius: 10px;
  }
  .summary h3 {
    margin-top: 0;
    color: #333;
  }
  .summary-item {
    display: flex;
    justify-content: space-between;
    margin: 10px 0;
    color: #444;
  }
  .btn {
    display: block;
    width: 100%;
    padding: 12px;
    background-color: #0077ff;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  .btn:hover {
    background-color: #005fd4;
  }
</style>
</head>
<body>

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
      <input type="number" min="1" max="10" value="2">
    </div>
  </div>

  <!-- Passageiro 1 -->
  <div class="section">
    <div class="section-title">Passageiro 1</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Passageiro 2 -->
  <div class="section">
    <div class="section-title">Passageiro 2</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Resumo -->
  <div class="section">
    <div class="section-title">Resumo da Compra</div>
    <div class="summary">
      <h3>Voo São Paulo → Lisboa</h3>
      <div class="summary-item">
        <span>Passagem</span>
        <span>R$ 2.500,00</span>
      </div>
      <div class="summary-item">
        <span>Taxas</span>
        <span>R$ 150,00</span>
      </div>
      <div class="summary-item">
        <strong>Total por pessoa</strong>
        <strong>R$ 2.650,00</strong>
      </div>
    </div>
  </div>

  <button class="btn">Finalizar Compra</button>
</div>

</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Checkout de Voo</title>
<style>
  body {
    background-color: #f4f7fa;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
  }
  .container {
    max-width: 1000px;
    margin: 40px auto;
    background: white;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    padding: 30px;
  }
  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }
  .section {
    margin-bottom: 30px;
  }
  .section-title {
    font-size: 1.2rem;
    margin-bottom: 15px;
    color: #444;
    border-bottom: 2px solid #e3e3e3;
    padding-bottom: 5px;
  }
  .info-box {
    background: #f9fafc;
    padding: 15px;
    border-radius: 10px;
    border: 1px solid #ddd;
    margin-bottom: 15px;
  }
  label {
    display: block;
    margin-bottom: 5px;
    color: #555;
  }
  input, select {
    width: 100%;
    padding: 8px 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    background: white;
  }
  .passageiro-box {
    background: #fefefe;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
  }
  .sub-box {
    background: #f9f9f9;
    border: 1px dashed #bbb;
    border-radius: 8px;
    padding: 10px;
    margin-bottom: 10px;
  }
  .sub-box h4 {
    margin-top: 0;
    color: #555;
  }
  .summary {
    background: #f0f4f8;
    padding: 20px;
    border-radius: 10px;
  }
  .summary h3 {
    margin-top: 0;
    color: #333;
  }
  .summary-item {
    display: flex;
    justify-content: space-between;
    margin: 10px 0;
    color: #444;
  }
  .btn {
    display: block;
    width: 100%;
    padding: 12px;
    background-color: #0077ff;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  .btn:hover {
    background-color: #005fd4;
  }
</style>
</head>
<body>

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
      <input type="number" min="1" max="10" value="2">
    </div>
  </div>

  <!-- Passageiro 1 -->
  <div class="section">
    <div class="section-title">Passageiro 1</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Passageiro 2 -->
  <div class="section">
    <div class="section-title">Passageiro 2</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Resumo -->
  <div class="section">
    <div class="section-title">Resumo da Compra</div>
    <div class="summary">
      <h3>Voo São Paulo → Lisboa</h3>
      <div class="summary-item">
        <span>Passagem</span>
        <span>R$ 2.500,00</span>
      </div>
      <div class="summary-item">
        <span>Taxas</span>
        <span>R$ 150,00</span>
      </div>
      <div class="summary-item">
        <strong>Total por pessoa</strong>
        <strong>R$ 2.650,00</strong>
      </div>
    </div>
  </div>

  <button class="btn">Finalizar Compra</button>
</div>

</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Checkout de Voo</title>
<style>
  body {
    background-color: #f4f7fa;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
  }
  .container {
    max-width: 1000px;
    margin: 40px auto;
    background: white;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    padding: 30px;
  }
  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }
  .section {
    margin-bottom: 30px;
  }
  .section-title {
    font-size: 1.2rem;
    margin-bottom: 15px;
    color: #444;
    border-bottom: 2px solid #e3e3e3;
    padding-bottom: 5px;
  }
  .info-box {
    background: #f9fafc;
    padding: 15px;
    border-radius: 10px;
    border: 1px solid #ddd;
    margin-bottom: 15px;
  }
  label {
    display: block;
    margin-bottom: 5px;
    color: #555;
  }
  input, select {
    width: 100%;
    padding: 8px 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    background: white;
  }
  .passageiro-box {
    background: #fefefe;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
  }
  .sub-box {
    background: #f9f9f9;
    border: 1px dashed #bbb;
    border-radius: 8px;
    padding: 10px;
    margin-bottom: 10px;
  }
  .sub-box h4 {
    margin-top: 0;
    color: #555;
  }
  .summary {
    background: #f0f4f8;
    padding: 20px;
    border-radius: 10px;
  }
  .summary h3 {
    margin-top: 0;
    color: #333;
  }
  .summary-item {
    display: flex;
    justify-content: space-between;
    margin: 10px 0;
    color: #444;
  }
  .btn {
    display: block;
    width: 100%;
    padding: 12px;
    background-color: #0077ff;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  .btn:hover {
    background-color: #005fd4;
  }
</style>
</head>
<body>

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
      <input type="number" min="1" max="10" value="2">
    </div>
  </div>

  <!-- Passageiro 1 -->
  <div class="section">
    <div class="section-title">Passageiro 1</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Passageiro 2 -->
  <div class="section">
    <div class="section-title">Passageiro 2</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Resumo -->
  <div class="section">
    <div class="section-title">Resumo da Compra</div>
    <div class="summary">
      <h3>Voo São Paulo → Lisboa</h3>
      <div class="summary-item">
        <span>Passagem</span>
        <span>R$ 2.500,00</span>
      </div>
      <div class="summary-item">
        <span>Taxas</span>
        <span>R$ 150,00</span>
      </div>
      <div class="summary-item">
        <strong>Total por pessoa</strong>
        <strong>R$ 2.650,00</strong>
      </div>
    </div>
  </div>

  <button class="btn">Finalizar Compra</button>
</div>

</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Checkout de Voo</title>
<style>
  body {
    background-color: #f4f7fa;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
  }
  .container {
    max-width: 1000px;
    margin: 40px auto;
    background: white;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    padding: 30px;
  }
  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }
  .section {
    margin-bottom: 30px;
  }
  .section-title {
    font-size: 1.2rem;
    margin-bottom: 15px;
    color: #444;
    border-bottom: 2px solid #e3e3e3;
    padding-bottom: 5px;
  }
  .info-box {
    background: #f9fafc;
    padding: 15px;
    border-radius: 10px;
    border: 1px solid #ddd;
    margin-bottom: 15px;
  }
  label {
    display: block;
    margin-bottom: 5px;
    color: #555;
  }
  input, select {
    width: 100%;
    padding: 8px 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    background: white;
  }
  .passageiro-box {
    background: #fefefe;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 15px;
    margin-bottom: 20px;
  }
  .sub-box {
    background: #f9f9f9;
    border: 1px dashed #bbb;
    border-radius: 8px;
    padding: 10px;
    margin-bottom: 10px;
  }
  .sub-box h4 {
    margin-top: 0;
    color: #555;
  }
  .summary {
    background: #f0f4f8;
    padding: 20px;
    border-radius: 10px;
  }
  .summary h3 {
    margin-top: 0;
    color: #333;
  }
  .summary-item {
    display: flex;
    justify-content: space-between;
    margin: 10px 0;
    color: #444;
  }
  .btn {
    display: block;
    width: 100%;
    padding: 12px;
    background-color: #0077ff;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  .btn:hover {
    background-color: #005fd4;
  }
</style>
</head>
<body>

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
      <input type="number" min="1" max="10" value="2">
    </div>
  </div>

  <!-- Passageiro 1 -->
  <div class="section">
    <div class="section-title">Passageiro 1</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Passageiro 2 -->
  <div class="section">
    <div class="section-title">Passageiro 2</div>
    <div class="passageiro-box">

      <!-- Dados Pessoais -->
      <div class="sub-box">
        <h4>Dados Pessoais</h4>
        <label>Nome Completo</label>
        <input type="text" placeholder="Digite seu nome completo">

        <label>RG</label>
        <input type="text" placeholder="Digite seu RG">
      </div>

      <!-- Plano e Valor -->
      <div class="sub-box">
        <h4>Plano e Valor</h4>
        <label>Plano</label>
        <select>
          <option value="Familiar">Familiar</option>
          <option value="PCD">PCD</option>
          <option value="Idoso">Idoso</option>
        </select>

        <label>Valor Individual</label>
        <input type="text" value="R$ 2.650,00" disabled>
      </div>
    </div>
  </div>

  <!-- Resumo -->
  <div class="section">
    <div class="section-title">Resumo da Compra</div>
    <div class="summary">
      <h3>Voo São Paulo → Lisboa</h3>
      <div class="summary-item">
        <span>Passagem</span>
        <span>R$ 2.500,00</span>
      </div>
      <div class="summary-item">
        <span>Taxas</span>
        <span>R$ 150,00</span>
      </div>
      <div class="summary-item">
        <strong>Total por pessoa</strong>
        <strong>R$ 2.650,00</strong>
      </div>
    </div>
  </div>

  <button class="btn">Finalizar Compra</button>
</div>

</body>
</html>
