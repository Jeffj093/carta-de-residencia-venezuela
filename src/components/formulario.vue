<template>
  <div class="formulario">
    <div class="campo" v-for="(field, index) in fields" :key="index">
      <label>{{ field.label }}</label>
      <input v-model="field.value" type="text" :placeholder="field.placeholder" :ref="`input_${index}`" @keydown.enter="focusNextInput(index)">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fields: [
        { label: 'Nombres:', value: '', placeholder: 'Ingrese sus nombres' },
        { label: 'Apellidos:', value: '', placeholder: 'Ingrese sus apellidos' },
        { label: 'Cedula:', value: '', placeholder: 'Ingrese su cedula' },
        { label: 'Direccion:', value: '', placeholder: 'Ingrese su direccion' },
        { label: 'Telefono:', value: '', placeholder: 'Ingrese su telefono' }
      ]
    };
  },
  methods: {
    focusNextInput(index) {
      if (index < this.fields.length - 1) {
        this.$refs[`input_${index + 1}`][0].focus();
      }
    }
  }
};
</script>

<style scoped>
.formulario {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.campo {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  padding: 20px;
  border-radius: 10px;
  background-color: #222;
}

.campo label {
  font-weight: bold;
  margin-bottom: 5px;
  background: linear-gradient(135deg, #c0ac72, #49eb87);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.campo input {
  padding: 15px;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  font-size: 16px;
  background-color: #444;
  color: #fff;
}

</style>
