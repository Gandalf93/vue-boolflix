<template>
  <div class="card">
    <ul>
      <li>
        <h4>Titolo: {{info.title}}</h4>
        <h4>Titolo: {{info.original_title}}</h4>
        <h4>Titolo: {{info.language}}</h4>
        <h4>Titolo: {{info.vote_average}}</h4>
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