<template>
  <div class="flex flex-col gap-y-[0px] w-[520px] h-[60px] justify-center relative">
    <label :class="[
      'ml-[7px] absolute select-none  bg-white px-2 transition-all duration-300 easy-in-out font-Roboto ',
      (isFocusedOrFilled ? 'transform-[translateY(-100%)] z-[3] text-[15px]' : 'transform-none opacity-60 z-[-1] text-[14px]')
    ]">
      {{ FieldName }}
    </label>
    <input
      class="outline-none border border-[rgba(0,0,0,0.2)] rounded-[8px] w-full h-[45px] p-2 font-Poppins text-[14px]"
      :type="type"
      v-model="inputValue"
      @focus="focused = true"
      @blur="focused = false"
    >
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

defineProps<{
  FieldName: string,
  type: string
}>()

const inputValue = ref('')
const focused = ref(false)

const isFocusedOrFilled = computed(() => {
  return focused.value || inputValue.value.length > 0
})
</script>
