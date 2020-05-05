<template>
    <div class="wrapper">
        <div class="placeholder">
            <img :src="img" :alt="name" title="Hey! It's me!">
        </div>
        <span>{{ username }}</span>
        <div class="description">
            <h1>{{ name }}</h1>
            <h2>{{ job }}</h2>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Title',
  props: ['img', 'username', 'name', 'job']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.placeholder {
    width: 150px;
    height: 150px;
    display: block;
    position: relative;
    margin: auto;
    margin-bottom: 8px;
}

img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    object-position: center;
    border-radius: 50%;
}

.description h1 {font-size: 26px; line-height: 32px; margin: 0;}
.description h2 {font-size: 20px; line-height: 20px; margin: 0; font-weight: 300;}

span {font-weight: 700;}

h1, h2, p, span {color: #17242A;}

.description {
    margin-top: 15px;
}

</style>
