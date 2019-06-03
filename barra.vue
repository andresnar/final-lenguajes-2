<template>
  <div>
    <v-toolbar
      color="cyan"
      dark
      tabs
    >
      <v-toolbar-side-icon></v-toolbar-side-icon>

      <v-toolbar-title>Localiza a tu Familiar</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>search</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>more_vert</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs v-model="tab" color="cyan" grow>
          <v-tabs-slider color="yellow">
          </v-tabs-slider>
          <v-tab v-for="item in items" :key="item">
            {{ item }} 
          </v-tab>
        </v-tabs>
      </template>
    </v-toolbar>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="item in text" :key="item">
        <v-card flat>
          <v-card-text><b>{{ item }}</b></v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          'Alzheimer y demencia', 'Equipo de Localizacion GPS'
        ],
        text: [
          'El Alzheimer es la forma más común de demencia, un término general que se aplica a la pérdida de memoria y otras habilidades cognitivas que interfieren con la vida cotidiana. Obtenga más información sobre los signos, causas y factores de riesgo y datos de la enfermedad de Alzheimer y sobre los tratamientos disponibles.'
          ,'Es un localizador que consta de un reloj GPS que permite que la persona que lo lleva continúe paseando sin miedo a perderle, ya que podrá saber donde está en cualquier momento gracias al receptor portable del que dispone. Es tan fácil como pulsar un botón en el receptor. En cuanto este se pulse, se verá en la pantalla un mapa con la posición del portador que lleve el reloj GPS.'
        ]
      }
    }
  }
</script>