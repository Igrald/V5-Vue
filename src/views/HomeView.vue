<script setup>
import Comp from "@/components/Comp.vue";

const clickHandler = (value) => {
  console.log("clicked", value);
};

const keyupHandler = (e) => {
  console.log("key up", e.target.value);
};
</script>

<template>
  <main>
    <table border>
      <tr>
        <td><Comp msg="Hello" @clicou="clickHandler" /></td>
        <td><Comp msg="sou" /></td>
      </tr>
      <tr>
        <td><Comp msg="o" @clicou="clickHandler" /></td>
        <td><Comp msg="prop" /></td>
      </tr>
    </table>

    <input type="text" @keyup.enter="keyupHandler" />
    <button @click.once="clickHandler">click</button>
  </main>
</template>
