<template>
  <BlogPost
    id="1"
    blogPostTitle="What is a muggle?"
    blogPostContent="A muggle is a person who lacks any sort of magical ability ..."
  />

  <hr />
  <BlogPost :id="blogPostId" :blogPostTitle="blogPostTitle" :blogPostContent="blogPostContent" />

  <!-- <hr />
  <BlogPost
    v-for="post in posts"
    :key="post.id"
    :id="post.id"
    :blogPostTitle="post.blogPostTitle"
    :blogPostContent="post.blogPostContent"
  ></BlogPost> -->

  <hr />
  <BlogPost v-for="post in posts" :key="post.id" v-bind="post"></BlogPost>
</template>

<script setup>
import { ref } from 'vue'
import BlogPost from './components/BlogPost.vue'

let blogPostId = ref(2)
let blogPostTitle = ref(
  'Harry Potter and the Cursed Child Bradway production suspended until April'
)
let blogPostContent = ref(
  'Adding to teh earlier post, the Broadway production of Herry Potter and the Cursed Child has been ...'
)

let posts = ref([
  {
    id: 1,
    blogPostTitle: 'Harry Potter and the Cursed Child Bradway production suspended until April',
    blogPostContent:
      'Adding to teh earlier post, the Broadway production of Herry Potter and the Cursed Child has been ...'
  },
  {
    id: 2,
    blogPostTitle: 'Harry Potter and the Cursed Child Bradway production suspended until April',
    blogPostContent:
      'Adding to teh earlier post, the Broadway production of Herry Potter and the Cursed Child has been ...'
  },
  {
    id: 3,
    blogPostTitle: 'Harry Potter and the Cursed Child Bradway production suspended until April',
    blogPostContent:
      'Adding to teh earlier post, the Broadway production of Herry Potter and the Cursed Child has been ...'
  },
  {
    id: 4,
    blogPostTitle: 'Harry Potter and the Cursed Child Bradway production suspended until April',
    blogPostContent:
      'Adding to teh earlier post, the Broadway production of Herry Potter and the Cursed Child has been ...'
  }
])
</script>

<style scoped></style>
