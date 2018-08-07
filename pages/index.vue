<template>
  <section id="posts" class="container">
    <PostPreview
    v-for="post in posts"
    :key="post.id"
    :title="post.title"
    :excerpt="post.previewText"
    :thumbnailImage="post.thumbnailUrl"
    :id="post.id"
    >
    </PostPreview>
  </section>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'
export default {
  components:{
    PostPreview
  },
  asyncData(context){
    return context.app.$storyapi.get('cdn/stories',{version: 'draft',
    starts_with:'blog/'}).then(res =>{
      return {
        posts: res.data.stories.map(bp => {
          return {
            id: bp.slug,
            title: bp.content.title,
            previewText: bp.content.summary,
            thumbnailUrl: bp.content.thumbnail
          };
        }),
      };
    });
  }
  /**data (){
    return{
      posts: [
        {
          title: 'A New Beginning',
          previewText: 'This is awesome dont miss it.',
          thumbnailUrl: 'https://firebasestorage.googleapis.com/v0/b/blog-f460a.appspot.com/o/ravi-pinisetti-761080-unsplash.jpg?alt=media&token=264ba4f2-07a3-49fc-9043-af0c43523a49',
          id: 'a-new-beginning'
        },
        {
          title: 'A New Beginning',
          previewText: 'This is awesome dont miss it.',
          thumbnailUrl: 'https://firebasestorage.googleapis.com/v0/b/blog-f460a.appspot.com/o/ravi-pinisetti-761080-unsplash.jpg?alt=media&token=264ba4f2-07a3-49fc-9043-af0c43523a49',
          id: 'a-second-beginning'
        }
      ]
    }
  }**/
}
</script>

<style scoped>
#posts{
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items:center;
}
</style>
