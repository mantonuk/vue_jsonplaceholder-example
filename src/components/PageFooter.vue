<template>
    <footer>
    234234234
    {{ somePropsValue }}
    <ul>
        <li><span><a href="">menu 1</a></span></li>
        <li><span><a href="">menu 2</a></span></li>
        <li><span><a href="">menu 3</a></span></li>
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
