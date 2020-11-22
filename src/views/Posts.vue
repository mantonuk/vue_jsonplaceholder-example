<template>
    <div>
        <h1>Posts Page</h1>
        <PostsComponent title="Posts" />
    </div>
</template>

<script>

import {default as PostsComponent} from '@/components/Posts.vue'

export default {
    name: 'Posts',
    components: {
      PostsComponent,
    }
}
</script>

