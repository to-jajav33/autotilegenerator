<template>
  <q-page class="row items-center justify-evenly">
    <q-form class="row">
      <q-input outlined v-model="settings.tile_width" label="Tile Width" ></q-input>
      <q-input outlined v-model="settings.tile_height" label="Tile Height" ></q-input>
      <q-input outlined v-model="settings.rows" label="Rows" ></q-input>
      <q-input outlined v-model="settings.columns" label="Columns" ></q-input>
    </q-form>
    <tile-gen-canvas
      :tile_height="settings.tile_height"
      :tile_width="settings.tile_width"
      :rows="settings.rows"
      :columns="settings.columns"
    ></tile-gen-canvas>
  </q-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import TileGenCanvas from '../components/TileGenCanvas.vue';

export default defineComponent({
  name: 'PageIndex',
  components: { TileGenCanvas },
  setup() {
    const settings = {
      tile_width: 64,
      tile_height: 64,
      rows: 4,
      columns: 12
    };

    return {
      settings
    }
  }
});
</script>
