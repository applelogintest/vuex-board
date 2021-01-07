<template>
    <post-list :posts="posts"/>
</template>

<script>
import PostList from '@/components/PostList';
import api from '@/api';
import { mapState, mapActions } from 'vuex';

export default{
    name: 'PostListPage',
    components:{
        PostList
    },
    // data() {
    //     return {
    //         posts: []
    //     }
    // },
    created() {
        // api.get('/posts')
        // .then(res => {
        //     this.posts = res.data;
        // })
        this.fetchPostList();
    },
    computed: {
        ...mapState([
            'posts'
        ])        
    },
    methods: {
      ...mapActions([
        'fetchPostList',
        ]),
    }

}
</script>