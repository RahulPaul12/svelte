<script>
   
</script>

<div class="section grid grid-cols-4">
  <div class="section-item section-item--1 item1">
    
  </div>
  <div class="section-item section-item--2 item2">
    
  </div>
  <div class="section-item section-item--3 item3">
    
  </div>
  <div class="section-item section-item--4 item4">
    
  </div>
  <div class="section-item section-item--5 item5">
    
  </div>
  <div class="section-item section-item--6 item6">
    
  </div>
  <div class="section-item section-item--7 item7">
    
  </div>
</div>


<style>
  .section {
    display: grid;
    width: 100%;
    height: 100vh;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(6,1fr);
    
}
   .section-item--1 {
    grid-area: item1;
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 4;
    background-color:#42A5F5;
  }

   .section-item--2 {
    grid-area: item2;
    grid-column-start: 3;
    grid-column-end: 7;
    grid-row-start: 1;
    grid-row-end: 6;
    background-color: #ffe4e6;
}
   .section-item--3 {
    grid-area: item3;
    grid-column-start: 7;
    grid-column-end: 13;
    grid-row-start: 1;
    grid-row-end: 3;
    background-color: #22d3ee;
}
   .section-item--4 {
    grid-area: item4;
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 4;
    grid-row-end: 6;
    background-color: #2dd4bf;
}
   .section-item--5 {
    grid-area: item5;
    grid-column-start: 7;
    grid-column-end: 11;
    grid-row-start: 3;
    grid-row-end: 13;
    background-color: #fef9c3;
}
   .section-item--6 {
    grid-area: item6;
    grid-column-start: 11;
    grid-column-end: 13;
    grid-row-start: 3;
    grid-row-end: 13;
    background-color: #34d399;
}
   .section-item--7 {
    grid-area: item7;
    grid-column-start: 1;
    grid-column-end: 7;
    grid-row-start: 6;
    grid-row-end: 7;
    background-color: #e879f9;
}

@media only screen and (max-width: 768px) {
  .section{
    grid-template-columns: 1fr;
    grid-template-rows: repeat(7,1fr);
    grid-template-areas:
            'item1'
            'item2'
            'item3'
            'item4'
            'item5'
            'item6'
            'item7';
    }
  [class*="section-item--"] {
  width: 100%;}
}


</style>
