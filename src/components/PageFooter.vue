<template>
    <footer>
    <hr />
    {{ somePropsValue }}
    <ul>
        <li><span><router-link to="/">Home</router-link></span></li>
        <li><span><router-link to="/posts">Posts</router-link></span></li>
    </ul>
    </footer>
</template>

<script>
export default {
  name: 'PageFooter',
  props: {
    somePropsValue : String
  }
}
</script>
