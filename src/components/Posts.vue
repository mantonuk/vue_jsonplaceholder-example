<template>
    <div>
        <h1>{{ title }}</h1>
		<Loader v-if="loading" />
        <ul v-else-if="items.length">
            <PostItem 
                v-for="(item, index) in items" 
                v-bind:item="item"
                v-bind:index ="index"
                v-bind:key="item.id"
                />
        </ul>
        <div v-else>No data</div>
    </div>
</template>

<script>
import axios from 'axios';

import PostItem from '@/components/PostItem'
import Loader from '@/components/Loader'

export default {
    name: 'Posts',
    props: {
        title : String,
    },
    mounted() {
        this.loadPosts();
    },
    methods : {
        loadPosts() {
            this.loading = true;
            setTimeout(() => {
                axios.get('https://jsonplaceholder.typicode.com/posts')
                .then(({data}) => {
                    this.items = data;
                    this.loading  = false;
                })
            }, 3000);
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
            ],
            loading: true,
		}
	},
    components : {
        PostItem,
		Loader
    }
}
</script>
