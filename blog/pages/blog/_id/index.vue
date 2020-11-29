<template>
    <div class="wrapper-content wrapper-content--fixed">
    <post :post="post" />
    <comments :comments="comments"/>
    <newComment />
  </div>
</template>

<script>
import post from '@/components/Blog/Post.vue'
import newComment from '@/components/Comments/NewComment.vue'
import comments from '@/components/Comments/Comments.vue'

export default {
    components: {post, comments, newComment},
    data() {
        return{
            post: {
                id: 1,
                title: '1 post',
                descr: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.',
                content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Lorem, ipsum dolor sit amet consectetur adipisicing elit.',
                img: 'https://drasler.ru/wp-content/uploads/2019/05/Фото-на-рабочий-стол-кошки-и-котята-коллекция-23.jpg'
            },
            comments: [
                {name: 'Artur', text: 'loremipsum. ipsum dolor sit amet consectetur adipisicing'},
                {name: 'Denis', text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'}
            ]
        }
    }
}
</script>

<style lang="scss">
.post{
    max-width: 900px;
    margin: 0 auto;
}

.post-header {
    text-align: center;
    margin-bottom: 30px;
    img{
        max-width: 400px;
        margin-bottom: 16px;
    }
    p{
        color: #999;
    }
}

.post-body{
    text-align: left;
}
</style>