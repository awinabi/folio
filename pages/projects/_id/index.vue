<template>
  <div class='wrap'>
    <div class='thumbnail-show' :style="{ backgroundImage: 'url(' + project.thumbnail + ')' }"></div>
    <h1>{{ project.title }}</h1>
    <p>{{ project.description }}</p>
  </div>
</template>>

<style scoped>
.thumbnail-show {
  width: 300px;
  height: 400px;
  background-position: center;
  background-size: cover;
}
.wrap {
  padding: 20px;
}
</style>


<script>
/* eslint-disable */
export default {
  asyncData(ctx) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          project: [
            {
              id: '1',
              title: 'AutoTrader',
              description: 'Auction of vehicles',
              thumbnail: 'https://i.imgur.com/0pCBaMG.jpg'
            },
            {
              id: '2',
              title: 'Halogen',
              description: 'Performance Managment',
              thumbnail: 'https://i.imgur.com/dLrqvx0.jpg'
            }
          ].find(el => el.id === ctx.params.id )
        })
      }, 150)
    })
  }
}
</script>
