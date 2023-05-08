<script>
export default {
  setup(props) {
    const displayValue = new Array(props.params.value).fill("#").join("");
    return {
      displayValue,
    };
  },
};
</script>

<template>
    <span>{{ displayValue }} HELLO</span>
</template>
