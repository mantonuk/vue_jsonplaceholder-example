<template>
    <header>
    {{ somePropsValue }}
    <ul>
        <li><span><router-link to="/">Home</router-link></span></li>
        <li><span><router-link to="/posts">Posts</router-link></span></li>
    </ul>
    <hr />
    </header>
</template>

<script>
export default {
  name: 'PageHeader',
  props: {
    somePropsValue : String
  }
}
</script>
