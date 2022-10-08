<template>
    <div class="container">
      <div class="film">
        <div class="film_photo"><img alt="" :src="movie.coverImage.src"></div>
        <div class="film_info">
          <div class="film_info_title">{{ movie.title }}</div>
          <div class="film_info_subtitle">{{ movie.originalTitle }}</div>
          <div class="film_info_age">{{ movie.year }}</div>
          <div class="film_info_description">{{ movie.description}}</div>
          <div class="film_info_button">
            <button class="film_info_button_watch">Смотреть</button>
            <button class="film_info_button_bookmark"><i class='bx bx-bookmark'></i></button>
          </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
  name: "card-film",
  props: {
    movie: {
      id: 1,
      title: "Аватар",
      originalTitle: "Avatar",
      description: "Фильм про синих чуваков",
      year: 2009,
      coverImage: {
        id: 1,
        src: "./icons/film.png",
        title: "Обложка",
        description: null,
      },
    },
  },
}
</script>

<style scoped>

.container{
  max-width: 600px;
  max-height: 300px;
  flex: 0 1 50%;

}
.film{
  display: flex;
}
.film_photo{
  margin-right: 15px;
  height: 300px;

}
.film_photo img{
  height: 100%;
  object-fit: cover;
}
.film_info_title{
  font-family: 'Raleway', serif;
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 24px;
  margin: 15px 0;
}
.film_info_subtitle{
  font-family: 'Raleway', serif;
  font-style: normal;
  font-weight: 300;
  font-size: 24px;
  line-height: 24px;
  margin-bottom: 15px;
}
.film_info_age{
  font-family: 'Raleway', serif;
  font-style: normal;
  font-weight: 300;
  font-size: 16px;
  line-height: 16px;
  margin-bottom: 15px;
}
.film_info_description{
  font-family: 'Roboto', serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  margin-bottom: 15px;
  max-height: 110px;
  text-overflow: ellipsis;
  overflow: hidden;
  display: -webkit-box;
  -webkit-line-clamp: 5;
  -webkit-box-orient: vertical;
}
.film_info_button{
  display: flex;
  position: absolute;
  bottom: 0;
}
.film_info_button_watch{
  padding: 10px 15px;
  font-family: 'Roboto', serif;
  font-weight: 400;
  font-size: 14px;
  line-height: 16px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: #f6f6f6;
  background-color: #6200EE;
  border: 1px solid #6200EE;
  border-radius: 4px;
  margin-right: 18px;
}
.film_info_button_bookmark{
  font-size: 24px;
  padding-top: 6px;
  color: #6200EE;
  margin-top: 0;
  border: 1px solid rgba(0, 0, 0, 0.12);
  border-radius: 4px;
  background-color: #fcfcfc;
}
</style>