<template>
<div>
  <div class="image" v-for="photo in photos" v-bind:key="photo._id">
    <br>
      <li>
        <a href="#">
        <h2 class="photoTitle">{{photo.title}}</h2>
        <p>{{photo.description}}</p>
        <p class="photoDate">
        <span v-if="photo.user.name">{{photo.user.name}}, </span>
          {{formatDate(photo.created)}}
        </p>
        </a>
      </li>
  </div>
</div>
</template>

<script>
import moment from 'moment';

export default {
  name: 'ImageGallery',
  props: {
    photos: Array
  },
  methods: {
    formatDate(date) {
      if (moment(date).diff(Date.now(), 'days') < 15)
        return moment(date).fromNow();
      else
        return moment(date).format('d MMMM YYYY');
    }
  }
}
</script>

<style scoped>
.photoTitle {
  margin: 0px;
  font-size: 1.2em;
}

.photoDate {
  margin: 0px;
  font-size: 0.9em;
  font-weight: normal;
}

p {
  margin: 0px;
}

</style>
