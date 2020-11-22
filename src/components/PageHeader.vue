<template>
    <header>
    {{ somePropsValue }}
    <ul>
        <li><span><a href="">menu 1</a></span></li>
        <li><span><a href="">menu 2</a></span></li>
    </ul>
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
