<template>
    <div class="wrapper">
        <a :href="link" target="_blank">
            <span class="top">{{ label_top }}</span>
            <span class="under">{{ label_under }}</span>
        </a>
    </div>
</template>

<script>
export default {
  name: 'Leaf',
  props: ['label_top', 'label_under', 'link']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
    display: flex;
    flex-direction: column;
    width: 100%;
    position: relative;
    margin-bottom: 30px;
    z-index: 1;
    text-decoration: none;
}

.top {
    position: relative;
    height: 100%;
    left: 0; right: 0;
    opacity: 1;
    transform: scale(1,1);
    color: #17242A;
    background-color: #FEDA6A;
    transition: all ease 250ms;
    padding: 20px 30px;
    border-radius: 50px;
}

.under {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    right: 0;
    opacity: 0;
    transform: scale(0.5,0.5);
    color: #FEFFFF;
    background-color: #EF476F;
    transition: all ease 250ms;
    padding: 20px 30px;
    border-radius: 50px;
}

a:hover .top {
    opacity: 0;
    transform: scale(1.2,1.2);
}

a:hover .under {
    opacity: 1;
    transform: scale(1,1);
}
</style>
