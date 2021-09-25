<template>
<div class="presentation">
  <img class="picture" alt="Photo de moi" :src="require('@/assets/images/me.jpg')">
  <div class="texts">
    <p class="text1">Salut! Je m'appelle Guillaume Bertherat, étudiant en Master Informatique.</p>
    <p class="text2">Passionné par l'informatique depuis petit, j'aimerais développer les outils informatiques de demain.</p>
  </div>
</div>
</template>
<script>
export default{
  name:"Presentation"
}
</script>