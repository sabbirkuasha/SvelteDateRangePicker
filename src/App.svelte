<script>
  import DatePicker from "./DatePicker.svelte";
  let DateSelected = ''


</script>

<main class="flex flex-col space-y-5 justify-center items-center h-screen bg-black">
  
  <!-- child to parent - Sab -->
  <DatePicker onChange={newValue => 
      {
        DateSelected = newValue; 
        console.log(DateSelected)
      }}/>


  <input type="text" id="dateRange" value="" class="w-1/2 bg-orange-700 text-white font-bold" />
  
  <!-- child to parent - Sab -->
  <div>
      Selected Date is <b>{DateSelected}</b> 
  </div>

</main>

<style>

</style>
