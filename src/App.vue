<template>
  <div class="container">
      <h1>PI. Aplicación con tu entorno de desarrollo, Framework</h1>
      <FilterByStatus/>
      <FilterByName/>
      <ListCharacters />
  </div>
</template>

<script>
import ListCharacters from './components/ListCharacters';
import FilterByStatus from './components/FilterByStatus';
import FilterByName from './components/FilterByName';
export default {
  name: 'App',
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName
}



}
</script>

<style lang="scss">
:root{
  --background-body:#ffffff;
  --background-card:#00a993;
  --text-wihite:#fff;
  --text-gray:#c0c0c0;
  --text-orange:#ff0000;
}
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body{
  background-color: var(--background-body);
  color: var(--text-wihite);
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
h1{
  margin-bottom: 3rem;
  text-align: center;
}
.container{
  width: 900px;
  max-width: 100%;
  margin: 5rem auto;
}
img{
  width: 100%;
}
</style>
