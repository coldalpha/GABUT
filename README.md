# Tools

Project Ini Ditujukan untuk membantu dalam pekerjaan

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Gabut</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0-beta1/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-0evHe/X+R7YkIZDRvuzKMRqM+OrBnVFBL6DOitfPri4tjfHxaWutUpFmBp4vmVor"
      crossorigin="anonymous"
    />
  </head>
  <body>
    <div class="container m-5 d-flex justify-content-center">
      <div class="card shadow-lg p-3 mb-5 bg-white rounded">
        <div class="card-body m-3">
          <h1 class="card-title mb-3">Hilang Spasi</h1>
          <input class="input-group" id="no_bpjs" onchange="hapusSpasi()" />
          <p id="hasil" class="mt-2"></p>
        </div>
      </div>
    </div>

    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0-beta1/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-pprn3073KE6tl6bjs2QrFaJGz5/SUsLqktiwsUTF55Jfv3qYSDhgCecCxMW52nD2"
      crossorigin="anonymous"
    ></script>

  </body>
  <script>
    function zeroPad(num, numZeros) {
      var n = Math.abs(num);
      var zeros = Math.max(0, numZeros - Math.floor(n).toString().length);
      var zeroString = Math.pow(10, zeros).toString().substr(1);
      if (num < 0) {
        zeroString = "-" + zeroString;
      }
      return zeroString + n;
    }
    function hapusSpasi() {
      var no_bpjs = document.getElementById("no_bpjs").value;
      hasil = no_bpjs.split(" ").join("");
      jumlah = hasil.length;
      if (jumlah < 16) {
        var kosong = 13 - jumlah;
        var zeroString = "";
        for (let index = 0; index < kosong; index++) {
          zeroString = "0" + zeroString;
        }
        angka1 = no_bpjs.split(" ").join("");
        angka = zeroString + angka1;
      }
      document.getElementById("hasil").innerHTML = angka;
    }
  </script>
</html>
