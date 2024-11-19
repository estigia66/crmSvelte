<script>
  let servicio = '';
  let cliente = '';
  let asesor = '';
  let fecha = '';
  let horaInicio = '';
  let horaFin = '';

  function Guardar() {
    console.log('Datos guardados', { servicio, cliente, asesor, fecha, horaInicio, horaFin });
  }

  function Cancelar() {
    console.log('Operación cancelada');
  }
</script>

<form on:submit|preventDefault={Guardar}>
  <div class="form-group">
    <label for="servicio">Servicio:</label>
    <input id="servicio" bind:value={servicio} required>
  </div>
  <div class="form-group">
    <label for="cliente">Cliente:</label>
    <input id="cliente" bind:value={cliente} required>
  </div>
  <div class="form-group">
    <label for="asesor">Asesor:</label>
    <input id="asesor" bind:value={asesor} required>
  </div>
  <div class="form-group">
    <label for="fecha">Fecha:</label>
    <input id="fecha" type="date" bind:value={fecha} required>
  </div>
  <div class="hora-container">
    <div class="form-group hora-group">
      <label for="horaInicio">Hora de inicio:</label>
      <input id="horaInicio" type="time" bind:value={horaInicio} required>
    </div>
    <div class="form-group hora-group">
      <label for="horaFin">Hora finalización:</label>
      <input id="horaFin" type="time" bind:value={horaFin} required>
    </div>
  </div>

  <button type="submit">Guardar</button>
  <button type="button" on:click={Cancelar}>Cancelar</button>
</form>

<style>
  form {
    background-color: white;
    color: #333;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    width: 100%;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
  }

  .hora-container {
    display: flex;
    gap: 15px;
  }

  .hora-group {
    flex: 1;
  }

  label {
    margin-bottom: 5px;
  }

  input {
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
    width: 100%;
    box-sizing: border-box;
  }

  input[type="time"] {
    text-align: center;
    font-size: 14px;
  }

  button {
    width: 100%;
    margin-top: 10px;
    padding: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  button[type="button"] {
    background-color: grey;
  }
</style>
