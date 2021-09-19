<template>
  <div class="fit">
    <canvas class="fit" style="border: 2px solid black" :height="`${$props.tile_height * $props.rows}`" :width="`${$props.tile_width * $props.columns}`"></canvas>
  </div>
</template>

<script lang="ts">
import {
  defineComponent,
  PropType,
  computed,
  ref,
  toRef,
  Ref,
} from 'vue';
import { Meta } from './models';

export default defineComponent({
  name: 'TileGenCanvas',
  props: {
    tile_width: {
      type: Number,
      required: true
    },
    tile_height: {
      type: Number,
      required: true
    },
    rows: {
      type: Number,
      required: true
    },
    columns: {
      type: Number,
      required: true
    },
    meta: {
      type: Object as PropType<Meta>,
      required: false
    },
  },
  setup(props) {
    return { };
  },
});
</script>
