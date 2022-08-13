<template>
  <div>
    <!-- this will filter the users price selection showing only items with prices that are equal too or less than the number they enterd -->
    <input type="number" />
    <button @click="price_filter">Price Filter</button>
    <!-- using a for loop inside HTML to display the items in the array inside the data js section -->
    <article v-for="(item, index) in items" :key="index">
      <h3>{{ item[`title`] }}</h3>
      <p>{{ item[`price`] }}</p>
      <h4>{{ item[`description`] }}</h4>
    </article>
  </div>
</template>

<script>
export default {
  methods: {
    price_filter() {},
  },

  data() {
    return {
      items: [
        {
          title: `Fruit Cup`,
          price: 10,
          description: `A fresh assortment of fruits`,
          image_url: `value`,
        },
        {
          title: `Hash Browns`,
          price: 5,
          description: `Two hash browns made from in our in house potates`,
          image_url: `value`,
        },
        {
          title: `Fruit Salad`,
          price: 15,
          description: `A fresh assortment of fruits mixed in a bowl`,
          image_url: `value`,
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>