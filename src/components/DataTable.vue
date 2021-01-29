<template>
  <div>
    <!-- <table style="width: 100%">
      <tr>
        <th>Firstname</th>
        <th>Lastname</th>
        <th>Age</th>
      </tr>
      <tr>
        <td>Jill</td>
        <td>Smith</td>
        <td>50</td>
      </tr>
      <tr>
        <td>Eve</td>
        <td>Jackson</td>
        <td>94</td>
      </tr>
    </table> -->
  </div>
</template>


<script>
//import request from "request";
import axios from "axios";

export default {
  name: "DataTable",

  created() {
    // myData = new Object();
    
  // err be http requst (cors)
  // Response to preflight request doesn't pass access control check: 
  // No 'Access-Control-Allow-Origin' header is present on the requested resource.

    axios
      .get(
        "https://esp32-1channel-gateway-test.data.thethingsnetwork.org/api/v2/query?last=3d",
        {
          
          headers: {
            Accept: "application/json",
            Authorization:
              "key ttn-account-v2.LzHLMQlro-qrHb85jxYYDMLdCTdLkBQHKeWMkOc4Bjw",
          },
        }
      )
      .then((response) => console.log(response))
      .catch((error) => console.log(error));



    //https://web.dev/cross-origin-resource-sharing/


    /*

    // EXTRACT VALUE FOR HTML HEADER.
    // ('Book ID', 'Book Name', 'Category' and 'Price')
    var col = [];
    for (var i = 0; i < myData.length; i++) {
      for (var key in myData[i]) {
        if (col.indexOf(key) === -1) {
          col.push(key);
        }
      }
    }

    // CREATE DYNAMIC TABLE.
    var table = document.createElement("table");

    // CREATE HTML TABLE HEADER ROW USING THE EXTRACTED HEADERS ABOVE.

    var tr = table.insertRow(-1); // TABLE ROW.

    for (var i = 0; i < col.length; i++) {
      var th = document.createElement("th"); // TABLE HEADER.
      th.innerHTML = col[i];
      tr.appendChild(th);
    }

    // ADD JSON DATA TO THE TABLE AS ROWS.
    for (var i = 0; i < myData.length; i++) {
      tr = table.insertRow(-1);

      for (var j = 0; j < col.length; j++) {
        var tabCell = tr.insertCell(-1);
        tabCell.innerHTML = myData[i][col[j]];
      }
    }

    // FINALLY ADD THE NEWLY CREATED TABLE WITH JSON DATA TO A CONTAINER.
    var divContainer = document.getElementById("showData");
    divContainer.innerHTML = "";
    divContainer.appendChild(table);


    */
  },
};
</script>

<style scoped>
</style>