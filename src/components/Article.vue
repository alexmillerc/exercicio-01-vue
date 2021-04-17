<template>
  <section>    
    <article v-for="(item, index) in items" :key="index">
        <Picture :link="item.linkImg" :title="item.titleImg"/>
        <section>
          <h4>{{ item.title }}</h4>
          <p>{{ item.content }}</p>
        </section>
    </article>
  </section>
</template>

<script>
import Picture from './Picture';

export default {
  name: 'Article',
  components: {
    Picture,
  },
  data(){
    return{
      items: [
        {
          id: 1,
          title: 'Imagem 1',
          content:'Lorem ipsum litora habitasse condimentum donec aenean sollicitudin elit porta curae habitasse mi.',
          titleImg: 'imagem 1',
          linkImg: 'img1'
        },
        {
          id: 2,
          title: 'Imagem 2',
          content:'Primis aucto scelerisque hendrerit cubilia urna massa ultrices ornare id dapibus, quam sit faucibus.',
          titleImg: 'imagem 2',
          linkImg: 'img2'
        },
        {
          id: 3,
          title: 'Imagem 3',
          content:'Ut sem orci habitasse donec luctus libero nulla sodales laoreet eros lacus proin tellus justo convallis',
          titleImg: 'imagem 3',
          linkImg: 'img3'
        },
      ]
    }
  }
}
</script>

<style scoped>
article{
  display: flex;
  margin-bottom: 1%;
  background-color: #c9d6df;
}

article section{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 5%;
}
</style>