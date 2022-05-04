<!-- <script setup>

</script> -->

<template>
 

  <div class="table">
    <table>
        <caption>Product List</caption>
      <tr>
        <th>s/n</th>
        <th>Product Name</th>
        <th>Product Price</th>
        <th>Product SKU</th>
        <th>Product Quantity</th>
      </tr>
      <tr>
        <td>1</td>
        <td>Talike</td>
        <td>592</td>
        <td>12345</td>
        <td>500</td>
      </tr>
      <tr>
        <td>2</td>
        <td>Falike</td>
        <td>635</td>
        <td>12346</td>
        <td>650</td>
      </tr>
      <tr>
        <td>3</td>
        <td>Calike</td>
        <td>710</td>
        <td>12347</td>
        <td>800</td>
      </tr>
      <tr>
        <td>4</td>
        <td>Balike</td>
        <td>820</td>
        <td>12348</td>
        <td>850</td>
      </tr>
      <tr>
        <td>5</td>
        <td>Dalike</td>
        <td>955</td>
        <td>12349</td>
        <td>1000</td>
      </tr>
    </table>
  </div>
</template>

<style lang="scss" scoped>
.table {
  caption {
    font-size: 30px;
    font-weight: 700;
    padding-top: 40px;
    padding-bottom: 40px;
  }
  table {
    width: 1000px;
    margin: auto;
  }
  th {
    text-align: left;
  }
  table,  th, td {
    border: 1px solid transparent;
    // border-radius:50px;
    border-collapse: collapse;
  }
  table {
    border: 1px solid transparent;
    //     border-radius:50px;
    //     border-collapse: collapse;
  }
  th, td {
    padding: 15px;
  }
  tr:nth-child(1) {
    background: #ddd;
  }
}
</style>
