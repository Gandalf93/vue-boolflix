<template>
  <div class="card">
    <ul>
      <li>
        <h4>Titolo: {{info.title}}</h4>
      </li>
      <li>
        <h4>Titolo Originale: {{info.original_title}}</h4>
      </li>
      <li>
        <h4>Lingua: {{info.language}}</h4>
      </li>
      <li>
        <h4>Voto: {{info.vote_average}}</h4>
      </li>

        
    </ul>
  </div>
</template>

<script>
export default {
name : 'Card',
props:['info'],
}
</script>

<style>

</style>