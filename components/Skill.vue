<template>
  <q-linear-progress stripe size="10px" :value="progress" />
  <p>Traitement et analyse de données multiomiques</p>
</template>

<script>
export default {
    props: { progress: Number },
};
</script>

<style>
</style>