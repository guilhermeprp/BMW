<template>
  <form class="quotation__form">
    <p class="quotation__form__title">Solicitar Cotação</p>

    <div>
      <input type="text" placeholder=" " required />
      <p>Nome</p>
    </div>
    <div>
      <input type="email" placeholder=" " required />
      <p>E-mail</p>
    </div>
    <div>
      <input type="tel" placeholder=" " />
      <p>Telefone</p>
    </div>

    <div>
      <select required>
        <option value="" selected disabled>Modelo</option>
        <option value="1">Modelo2</option>
        <option value="2">Modelo3</option>
        <option value="3">Modelo4</option>
      </select>
    </div>

    <div>
      <textarea placeholder="Mensagem" />
    </div>

    <label>
      <input type="checkbox" required />
      <span class="quotation__form__agree">
        Aceito a <strong> Política de Privacidade.</strong>
      </span>
    </label>

    <button class="quotation__form__submit__button">Enviar</button>
  </form>
</template>

<script>
import "./QuotationForm.css";
export default {
  name: "QuotationForm",
};
</script>
