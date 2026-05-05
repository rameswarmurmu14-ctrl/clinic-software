<script>
function printBill(i){
  let d = data[i];

  let w = window.open('', '', 'width=500,height=700');

  w.document.write(`
  <html>
  <head>
    <title>Bill</title>
    <style>
      body{font-family:Arial;padding:20px}
      .center{text-align:center}
      .box{border:1px solid #000;padding:10px;margin-top:10px}
      h2,h3{margin:5px}
    </style>
  </head>
  <body>

    <div class="center">
      <h2>Neuro Electro Physiology</h2>
      <p>Portable-EEG, NCS, EMG, EP</p>
      <hr>
    </div>

    <div class="box">
      <p><b>Doctor:</b> ${doctorSelect.value}</p>
      <p><b>Date:</b> ${billDate.value}</p>
    </div>

    <div class="box">
      <p><b>Patient Name:</b> ${d.name}</p>
      <p><b>Case No:</b> ${d.caseNo}</p>
      <p><b>Test:</b> ${d.test}</p>
    </div>

    <div class="box">
      <h3>Total Amount: ₹${d.price}</h3>
    </div>

    <br><br>
    <p>Signature __________________</p>

  </body>
  </html>
  `);

  w.print();
}
</script>
