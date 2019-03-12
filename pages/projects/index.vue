<template>
  <div class='projects'>
    <Project
      v-for="project in projects"
      :key="project.id"
      :title="project.title"
      :description="project.description"
      :thumbnail='project.thumbnail'
    />

  </div>
</template>


<script>
/* eslint-disable */

import Project from '~/components/Project'

export default {
  components: {
    Project
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          projects: [
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
          ]
        })
      }, 1500)
    })
  }
}
</script>
