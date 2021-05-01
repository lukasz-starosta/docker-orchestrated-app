<template>
<div>
    <table>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Price</th>
        </tr>
        <tr v-for="product in products" v-bind:key="product.name">
            <td>{{product.name}}</td>
            <td>{{product.description}}</td>
            <td>{{product.price}}</td>
        </tr>
    </table>
</div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'Products',
    data: function() {
        return {
            products : [],
        }
    },
    mounted: function() {
       var self = this;
    axios
      .get('http://127.0.0.1:5001/products')
      .then(res => {
          self.products = res.data;
          });
      
    }
}
</script>