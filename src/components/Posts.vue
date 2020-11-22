<template>
    <div>
        <h1>{{ title }}</h1>
        <ul>
            <PostItem 
                v-for="(item, index) in items" 
                v-bind:item="item"
                v-bind:index ="index"
                v-bind:key="item.id"
                />
        </ul>
    </div>
</template>

<script>
import axios from 'axios';

import PostItem from '@/components/PostItem'

export default {
    name: 'Posts',
    props: {
        title : String,
    },
    created() {
        this.loadPosts();
    },
    methods : {
        loadPosts() {
            axios.get('https://jsonplaceholder.typicode.com/posts')
            .then(({data}) => this.items = data)
        },
        loadPostById({id}) {
            console.log(id);
            axios.get('https://jsonplaceholder.typicode.com/posts/' + id)
            .then(({data}) => this.expandPost(data))
        },
        expandPost(item) {
            console.log(item);
        },
        loadUsersByIds(ids) {
            console.log(ids);
        }
    },
	data() {
		return {
			items: [
                {
                    id : 1,
                    title: 'Title1'
                },
                {
                    id : 2,
                    title: 'Title2'
                },
                {
                    id : 3,
                    title: 'Title3'
                },
                {
                    id : 4,
                    title: 'Title4'
                },
            ]
		}
	},
    components : {
        PostItem
    }
}
</script>
