<template>
  <div class="wrapper-content wrapper-content--fixed">
    <promo />
    <Intro title="My last posts:"/>
    <PostsList :posts="posts"/>
    <contacts />
  </div>
</template>

<script>
import promo from '@/components/Promo.vue'
import contacts from '@/components/Contacts.vue'

export default {
  components: {promo, contacts},
  data() {
    return{
      posts: [
        {
          id: 1,
          title: '1 post',
          descr: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.',
          img: 'https://drasler.ru/wp-content/uploads/2019/05/Фото-на-рабочий-стол-кошки-и-котята-коллекция-23.jpg'
        },
        {
          id: 2,
          title: '2 post',
          descr: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.',
          img: 'https://fullhdoboi.ru/wp-content/uploads/_ph/29/121630753.jpg'
        },
        {
          id: 3,
          title: '3 post',
          descr: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.',
          img: 'http://www.fonstola.ru/download.php?file=201610/1920x1080/fonstola.ru-247447.jpg'
        }

      ]
    }
  }

}


</script>


