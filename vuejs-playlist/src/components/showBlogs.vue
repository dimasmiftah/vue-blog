<template>
<div id="show-blogs">
<h1>All Blogs Articles</h1>
<div class="single-blog" v-for="blog in blogs" :key="blog.index">
    <h3>{{blog.title}}</h3>
    <article>{{blog.body}}</article>

</div>
</div>
</template>

<script>
export default {
data () {
return {
    blogs: []
}
},
created() {
    this.$http.get('https://jsonplaceholder.typicode.com/posts').then(function (data) {  
        this.blogs = data.body.slice(0,10);
        console.log(this.blogs);
        
    })
},
}
</script>

<style>
#show-blogs{
    max-width: 800px;
    margin: 0 auto;
}
.single-blog{
    padding: 20px;
    margin: 20px 0;
    box-sizing: border-box;
    background: #eee;
}
</style>
