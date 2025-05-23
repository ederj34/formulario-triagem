<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Formulário Jurídico - Rafael Nunes Advogados Associados</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&display=swap');

    body {
      font-family: 'Playfair Display', serif;
      background: #f4f4f4;
      margin: 0;
      padding: 20px;
    }

    .container {
      max-width: 800px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    h1 {
      text-align: center;
      color: #2c3e50;
    }

    label {
      display: block;
      margin-top: 20px;
      font-weight: bold;
    }

    input, select, textarea {
      width: 100%;
      padding: 10px;
      margin-top: 8px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      margin-top: 30px;
      width: 100%;
      padding: 15px;
      font-size: 16px;
      background: #2c3e50;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    button:hover {
      background: #34495e;
    }

    .checkbox-group {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .checkbox-group label {
      font-weight: normal;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Formulário Jurídico</h1>
    <form action="https://formspree.io/f/{SEU_CÓDIGO}" method="POST">
      
      <label>Nome Completo</label>
      <input type="text" name="nome" required>

      <label>CPF</label>
      <input type="text" name="cpf" required>

      <label>Comarca do Processo</label>
      <input type="text" name="comarca">

      <label>Tipo de Prisão</label>
      <select name="tipo-prisao">
        <option value="">Selecione</option>
        <option value="flagrante">Flagrante</option>
        <option value="preventiva">Preventiva</option>
        <option value="temporária">Temporária</option>
        <option value="domiciliar">Domiciliar</option>
      </select>

      <label>Documentos que você possui</label>
      <div class="checkbox-group">
        <label><input type="checkbox" name="documentos[]" value="denuncia"> Denúncia</label>
        <label><input type="checkbox" name="documentos[]" value="boletim"> Boletim de Ocorrência</label>
        <label><input type="checkbox" name="documentos[]" value="mandado"> Mandado de Prisão</label>
        <label><input type="checkbox" name="documentos[]" value="sentenca"> Sentença</label>
        <label><input type="checkbox" name="documentos[]" value="outros"> Outros</label>
      </div>

      <label>Observações</label>
      <textarea name="observacoes" rows="4"></textarea>

      <button type="submit">Enviar Informações</button>
    </form>
  </div>
</body>
</html>
