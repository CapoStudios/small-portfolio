<template>
    <li @click="NewTab(url)"  class="card">
        <div class="account-name">
          {{name}}
          <i :class="icon" :style="marginLeft"></i>
        </div>
    </li>
</template>

<script>
export default {
    name: 'Card',
    props: ['name', 'icon', 'margin', 'media', 'url'],
    methods: {
        NewTab(url) {
            window.open(url, "_blank");
        }
    },
    computed: {
        marginLeft(){
            return {
                '--margin-left': this.margin,
                '--margin-left-media': this.media,
            };
        },
    },
}
</script>

<style scoped>
.card {
  height: 60px;
  width: 354px;
  border: 2px solid #eee;
  border-radius: 15px;
  margin: 10px auto auto auto;
  font-size: 1.4rem;
  text-align: center;
  cursor: pointer;
}

.account-name {
  height: 50px;
  padding-left: 30px;
  text-align: start;
  margin-top: 5px;
  display: flex;
  align-items: center;
}

i {
    font-size: 2.5rem; 
    text-align: center;
    margin-left: var(--margin-left);
}

@media only screen and (max-width: 600px)  {
    .card {
        height: 50px;
        width: 309px;
        margin: 8px auto auto auto;
        font-size: 1.2rem;
    }
    .account-name {
        height: 40px;
        padding-left: 20px;
        margin-top: 5px;
    }
    i {
        font-size: 2.3rem;
        margin-left: var(--margin-left-media);
    }
}
</style>