<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="4">
        <qrcode-vue
          :value="value"
          :size="size"
          level="H"
          :background="backgroundColor"
          :foreground="foregroundColor"
        ></qrcode-vue>
      </v-col>
      <v-col cols="12" md="6">
        <v-container>
          <v-row>
            <v-col cols="12" md="12">
              <v-text-field
                v-model="value"
                :rules="valueRules"
                :counter="25"
                label="Ingresa tu QR: www.ejemplo.com"
                required
              ></v-text-field>
            </v-col>
            <v-col cols="12" md="12">
              <v-text-field
                v-model="backgroundColor"
                :rules="valueRules"
                :counter="25"
                label="Cambia el color de fondo aqui (Hexadecimal)"
                required
              ></v-text-field>
            </v-col>
            <v-col cols="12" md="12">
              <v-text-field
                v-model="foregroundColor"
                :rules="valueRules"
                :counter="25"
                label="Cambia el color del plano aqui (Hexadecimal)"
                required
              ></v-text-field>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import QrcodeVue from 'qrcode.vue';

export default {
  name: 'Home',
  data() {
    return {
      value: '',
      backgroundColor: '#FFFFFF',
      foregroundColor: '#000000',
      size: 300,
      valueRules: [
        v => !!v || 'El texto de QrCode es requerido',
        v => v.length <= 10 || 'No puede sobrepasar los 25 caracteres',
      ],
    };
  },
  components: {
    QrcodeVue,
  },
};
</script>
