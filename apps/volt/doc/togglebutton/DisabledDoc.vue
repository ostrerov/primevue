<template>
    <DocSectionText v-bind="$attrs">
        <p>When <i>disabled</i> is present, the element cannot be edited and focused.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <ToggleButton v-model="checked" disabled onIcon="pi pi-check" offIcon="pi pi-times" class="w-full sm:w-40" aria-label="Confirmation" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import ToggleButton from '@/volt/ToggleButton.vue';
import { ref } from 'vue';

const checked = ref(false);

const code = ref(`
<template>
    <div class="card flex justify-center">
        <ToggleButton v-model="checked" disabled onIcon="pi pi-check" offIcon="pi pi-times" class="w-full sm:w-40" aria-label="Confirmation" />
    </div>
</template>

<script setup lang="ts">
import ToggleButton from '@/volt/ToggleButton.vue';
import { ref } from 'vue';

const checked = ref(false);
<\/script>
`);
</script>
