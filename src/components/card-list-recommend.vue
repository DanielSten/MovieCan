<template>
  <div class="flex">
    <card-film v-for="movie in movies" :movie="movie"></card-film>
  </div>
</template>

<script>
import CardFilm from "./card-film.vue";

export default {
  components: {
    CardFilm,
  },
  name: "card-list",
  data() {
    return {
      movies: [
        {
          id: 1,
          title: "Аватар",
          originalTitle: "Avatar",
          description: "But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness. No one rejects, dislikes, or avoids pleasure itself, because it is pleasure, but But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness. No one rejects, dislikes, or avoids pleasure itself, because it is pleasure, but",
          year: 2009,
          coverImage: {
            id: 1,
            src: "./icons/avatar.jpg",
            title: "Обложка",
            description: null,
          },
        },
        {
          id: 2,
          title: "Железный человек",
          originalTitle: "Iron man",
          description: "But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness. No one rejects, dislikes, or avoids pleasure itself, because it is pleasure, but...",
          year: 2009,
          coverImage: {
            id: 1,
            src: "./icons/film.png",
            title: "Обложка",
            description: null,
          },
        },
        {
          id: 3,
          title: "Аватар",
          originalTitle: "Avatar",
          description: "Фильм про синих чуваков",
          year: 2009,
          coverImage: {
            id: 1,
            src: "./icons/avatar.jpg",
            title: "Обложка",
            description: null,
          },
        },
        {
          id: 4,
          title: "Аватар",
          originalTitle: "Avatar",
          description: "Фильм про синих чуваков",
          year: 2009,
          coverImage: {
            id: 1,
            src: "./icons/avatar.jpg",
            title: "Обложка",
            description: null,
          },
        },
      ],
    };
  },
}
</script>

<style scoped>
.flex{
  display: flex;
  justify-content:space-between;
  flex-wrap:wrap;
  gap: 25px 0;
}
</style>