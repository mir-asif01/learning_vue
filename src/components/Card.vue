<script setup>
defineProps({
  divClasses: {
    type: String,
  },
  title: {
    type: String,
    default: "card title",
  },
  subTitle: {
    type: String,
    default: "card subtitle",
  },
  btnText: {
    type: String,
    default: "Button",
  },
  titleClasses: {
    type: String,
    default: "",
  },
  subTitleClasses: {
    type: String,
    default: "",
  },
  btnClasses: {
    type: String,
    default: "",
  },
})
</script>

<template>
  <div :class="divClasses">
    <!-- <h2 class="text-2xl font-bold">{{ text }}</h2> -->
    <h2 :class="titleClasses">{{ title }}</h2>
    <p :class="subTitleClasses">
      Browse our Vue jobs and start your career today
    </p>
    <a :class="btnClasses"> Browse Jobs </a>
  </div>
</template>
