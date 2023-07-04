---
title: Liveries
type: docs
---

<style>
    table: {
        font-family: Arial, Helvetica, sans-serif;
        border-collapse: collapse;
        width: 100%;
    }

    td {
        border: 1px solid #ddd;
        padding: 8px;
        }

    tr:nth-child(even){background-color: #f2f2f2;}

    tr:hover {background-color: #ddd;}

    th {
        padding-top: 12px;
        padding-bottom: 12px;
        text-align: left;
        color: #bcc3cb;
        background-color: #05072f;
        }

        #counter{
            text-align: center;
            background-color: #05072f;
            color: #bcc3cb;
            width: 20%;
            padding: 5px;
            float: center;
        }
</style>

<script>
    function sortTable(table) {
  var rows, switching, i, x, y, shouldSwitch;
  switching = true;
  /*Make a loop that will continue until
  no switching has been done:*/
  while (switching) {
    //start by saying: no switching is done:
    switching = false;
    rows = table.rows;
    /*Loop through all table rows (except the
    first, which contains table headers):*/
    for (i = 1; i < (rows.length - 1); i++) {
      //start by saying there should be no switching:
      shouldSwitch = false;
      /*Get the two elements you want to compare,
      one from current row and one from the next:*/
      x = rows[i].getElementsByTagName("TD")[0];
      y = rows[i + 1].getElementsByTagName("TD")[0];
      //check if the two rows should switch place:
      if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
        //if so, mark as a switch and break the loop:
        shouldSwitch = true;
        break;
      }
    }
    if (shouldSwitch) {
      /*If a switch has been marked, make the switch
      and mark that a switch has been done:*/
      rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
      switching = true;
    }
  }
}

    async function load(){
        await fetch("https://raw.githubusercontent.com/kolos26/GEOFS-LiverySelector/main/livery.json").then(res => res.json()).then(data => liveryobj = data);
        Array.prototype.slice.call(document.getElementsByTagName("table")).forEach(
            function(e){
                grabLiveries(e.id, e);
                sortTable(e);
            }
        );
        document.getElementById("counter").innerHTML = Array.prototype.slice.call(document.getElementsByTagName("td")).length;
    }

    function grabLiveries(id, element){
        liveryobj.aircrafts[id].liveries.forEach(function(e){
            row = document.createElement("tr");
            liveryname = document.createElement("td");
            liveryname.innerHTML = e.name
            row.appendChild(liveryname)
            element.appendChild(row);
        })
    }

    load();
</script>

<div id="counter"></div>

## Piper J-3 Cub
<table id="1">
<th>Available liveries</th>
</table>

## Cessna 172 Skyhawk
<table id="2">
<th>Available liveries</th>
</table>

## Boeing b737-700 / Boeing b737-700BCF
<table id="4">
<th>Available liveries</th>
</table>

## de Havilland Canada DHC-6 Twin Otter
<table id="6">
<th>Available liveries</th>
</table>

## Airbus a380-800
<table id="10">
<th>Available liveries</th>
</table>

## de Havilland Canada DHC-2 Beaver
<table id="13">
<th>Available liveries</th>
</table>

## Colomban MC-15 Cri-Cri
<table id="14">
<th>Available liveries</th>
</table>

## Lockheed P38-F5B Lightning
<table id="15">
<th>Available liveries</th>
</table>

## Sukhoi Su-35 Flanker-E
<table id="18">
<th>Available liveries</th>
</table>

## Aerospatiale France - British Aircraft Corporation Concorde
<table id="20">
<th>Available liveries</th>
</table>

## Boeing b767-300ER / Boeing b767-300F
<table id="237">
<th>Available liveries</th>
</table>

## Boeing b757-200 / Boeing b757-200F
<table id="238">
<th>Available liveries</th>
</table>

## Airbus a350-900XWB
<table id="239">
<th>Available liveries</th>
</table>

## Airbus a319-100
<table id="2879">
<th>Available liveries</th>
</table>

## ATR72-600
<table id="2418">
<th>Available liveries</th>
</table>

## Airbus a350-1000XWB / Airbus a350F
<table id="2973">
<th>Available liveries</th>
</table>

## Boeing b787-9 Dreamliner
<table id="3575">
<th>Available liveries</th>
</table>

## Airbus a220-300 / Bombardier CS300
<table id="2899">
<th>Available liveries</th>
</table>

## Airbus a320neo
<table id="2871">
<th>Available liveries</th>
</table>

## Boeing b737 MAX 8 / Boeing b737-8 / Boeing b737 MAX 8-200 / Boeing b737-8-200
<table id="2769">
<th>Available liveries</th>
</table>

## Boeing b787-10 Dreamliner
<table id="3180">
<th>Available liveries</th>
</table>

## Boeing P8I Poseidon
<table id="3292">
<th>Available liveries</th>
</table>

## Bombardier CRJ-700
<table id="3307">
<th>Available liveries</th>
</table>

## Booeing b737-800 / Boeing b737-800BCF
<table id="3054">
<th>Available liveries</th>
</table>

## Embraer ERJ-145LR
<table id="4017">
<th>Available liveries</th>
</table>

## Boeing b737-200
<table id="4140">
<th>Available liveries</th>
</table>

## Bombardier dash8-q400 / de Havilland Canada DHC-8-400
<table id="247">
<th>Available liveries</th>
</table>

## Britten-Norman BN-2 Islander
<table id="4398">
<th>Available liveries</th>
</table>