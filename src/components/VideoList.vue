<template>
  <div class="videos-list">
    <h1>Ambience Library</h1>
    <div class="list-wrap">
      <div v-for="video in videos" :key="video.id" :id="video.id">
        <div class="video-wrap">
            <iframe width="560" height="315" :src="video.source" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="tag-wrap">
          <div>Tags:</div>
          <span v-for="tag in video.tags">{{ tag }}</span>
        </div>
    </div>
    </div>
  </div>
</template>
<script setup lang="ts">
  const videos = [
    { 
      id: 'pjeaX4Z2N6Q', 
      source: 'https://www.youtube.com/embed/pjeaX4Z2N6Q', 
      tags: ['work', 'jazz'] 
    }, { 
      id: 'nd5cpmQiP-4', 
      source: 'https://www.youtube.com/embed/nd5cpmQiP-4', 
      tags: ['cozy', 'hobbit', 'coffee shop']
    }, { 
      id: 'fV1kXBfMl6k', 
      source: 'https://www.youtube.com/embed/fV1kXBfMl6k', 
      tags: ['underwater', 'ambient']
    }
  ]
</script>