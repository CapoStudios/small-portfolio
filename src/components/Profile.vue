<template>
    <li class="profile-img" :style="bgImg"></li>
    <li class="name">{{name}}</li>
</template>

<script>
export default {
    name: 'Profile', 
    props: ['name', 'image'],
    computed: {
        bgImg(){
            return {
                'background-image': "url('" + this.image + "')",
            };
        },
    },
}
</script>

<style scoped>
.profile-img {
  height: 110px;
  width: 110px;
  background-size: cover;
  border-radius: 50%;
  margin: auto;
}

.name {
  font-size: 1.4rem;
  margin-top: 5px;
  margin: auto;
}

@media only screen and (max-width: 600px) {
    .profile-img {
        height: 93px;
        width: 93px;
    }
    .name {
        font-size: 1.2rem;
        margin-top: 3px;
    }
}
</style>