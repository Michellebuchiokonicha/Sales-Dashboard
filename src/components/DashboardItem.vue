<script>
// import { ref } from 'vue'

export default {
  
  name: 'app',
  data 
  () {
    return {
      count_1: {
        quantity: 0,
        price: 592,
        key: 1
      },
      count_2: {
        quantity: 0,
        price: 635,
        key: 2  
      },
      count_3: {
        quantity: 0,
        price: 710,
        key: 3
      },
      count_4: {
        quantity: 0,
        price: 820,
        key: 4
      },
      count_5: {
        quantity: 0,
        price: 955,
        key: 5
      },
    }
    
  },

  methods: {
    increaseS(count) {
      if (count.quantity < 2000)
      count.quantity++
    },
    decreaseS(count) {
      if(count.quantity > 0)
      count.quantity--
    },
  }
}

</script>

<template>
  <div class="item">
    <div class="counter">
      <div class="count">
        <h4>10</h4>
        <p>Number of Products</p>
      </div>
      <div class="count">
        <h4>
          {{ 
            count_1.quantity +
            count_2.quantity +
            count_3.quantity + 
            count_4.quantity + 
            count_5.quantity 
          }}
        </h4>
        <p>Number of Orders</p>
      </div>
      <div class="count">
        <h4>
          {{ 
            count_1.quantity +
            count_2.quantity +
            count_3.quantity + 
            count_4.quantity + 
            count_5.quantity 
          }}
        </h4>
        <p>Number of Sales</p>
      </div>
      <div class="count">
        <h4><img src="../assets/Nairaaa.png" alt="naira" class="naira">
          {{
            (count_1.quantity * count_1.price) +
            (count_2.quantity * count_2.price) +
            (count_3.quantity * count_3.price) +
            (count_4.quantity * count_4.price) +
            (count_5.quantity * count_5.price)
          }}
        </h4>
        <p>Sales Value</p>
      </div>
    </div >

    <div class="table">
      <table>
        <caption>Order Table</caption>
        <tr>
          <th>s/n</th>
          <th>Product Name</th>
          <th>Quantity</th>
          <th>Order ID</th>
          <th>Order Value</th>
          <th>Customer Email</th>
        </tr>
        <tr>
          <td>{{ count_1.key }}</td>
          <td>Talike</td>
          <td>
            <p>
              <span @click="increaseS(count_1)" class="span">+</span>{{ count_1.quantity }}
              <span @click="decreaseS(count_1)" class="span">-</span>
            </p>
          </td>
          <td>{{ count_1.key }}</td>
          <td>{{ count_1.quantity * count_1.price }}</td>
          <td>Mimi@gmail.com</td>
        </tr>
        <tr>
          <td>{{ count_2.key }}</td>
          <td>Falike</td>
          <td>
            <p>
              <span @click="increaseS(count_2)" class="span">+</span>{{ count_2.quantity }}
              <span @click="decreaseS(count_2)" class="span">-</span>
            </p>

          </td>
          <td>{{ count_2.key }}</td>
          <td>{{ count_2.quantity * count_2.price }}</td>
          <td>Cimi@gmail.com</td>
        </tr>
        <tr>
          <td>{{ count_3.key }}</td>
          <td>Calike</td>
          <td>
            <p>
              <span @click="increaseS(count_3)" class="span">+</span>{{ count_3.quantity }}
              <span @click="decreaseS(count_3)" class="span">-</span>
            </p>

          </td>
          <td>{{ count_3.key }}</td>
          <td>{{ count_3.quantity * count_3.price }}</td>
          <td>Mimi@gmail.com</td>
        </tr>
        <tr>
          <td>{{ count_4.key }}</td>
          <td>Balike</td>
          <td>
            <p>
              <span @click="increaseS(count_4)" class="span">+</span>{{ count_4.quantity }}
              <span @click="decreaseS(count_4)" class="span">-</span>
            </p>

          </td>
          <td>{{ count_4.key }}</td>
          <td>{{ count_4.quantity * count_4.price }}</td>
          <td>Mimi@gmail.com</td>
        </tr>
        <tr>
          <td>{{ count_5.key }}</td>
          <td>Dalike</td>
          <td>
            <p>
              <span @click="increaseS(count_5)" class="span">+</span>{{ count_5.quantity}}
              <span @click="decreaseS(count_5)" class="span">-</span>
            </p>

          </td>
          <td>{{ count_5.key }}</td>
          <td>{{ count_5.quantity * count_5.price }}</td>
          <td>Mimi@gmail.com</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.counter {
  display: flex;
  justify-content: space-evenly;
  padding-top: 40px;

 @media (max-width: 768px) {
    display: flex;
    flex-direction: column;
  }
  .count {
    border: 1px solid transparent;
    border-radius: 5px;
    box-shadow: 5px 3px 5px 5px rgb(233, 226, 226);
    width: 17%;
    height: 140px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    img {
      width: 0.7rem;
    }
  }
}

.table {
  padding-top: 50px;

  caption {
    font-size: 30px;
    font-weight: 700;
    padding-top: 40px;
    padding-bottom: 40px;
  }
  .span {
    border: 1px solid transparent;
    background: rgb(247, 247, 247);
    border-width: 3px;
    font-size: larger;
    cursor: pointer;
    box-shadow: 2px 2px 2px rgb(216, 212, 212);
}
  table {
    width: 870px;
    margin: auto;
    @media (max-width: 768px) {
     th {
       display: none;
     }
     table, th, td, tr {
       display: block;
       width: 150px;
     }
     
  }
    // border-spacing: 40px;
  }
  th {
    text-align: left;
  }
  table, th, td {
    border: 1px solid transparent;
    border-collapse: collapse;
    
  }
  th, td {
    padding: 20px;
  }
  td, tr {
    
    @media (max-width: 768px) {
     border: 1px solid rgb(177, 175, 175);
     
  }
  }
  th {
    background: #ddd;
  }
  tr:nth-child(1) {
    background: #ddd;
  }
   
}

@media (min-width: 768px) {
 
}
</style>
