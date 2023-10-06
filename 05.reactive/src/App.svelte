<script>
  let firstName = 'Ujjawal'
  let lastName = 'Gupta'
  $: fullName = `${firstName} ${lastName}`;
  setTimeout(() => {
    firstName = 'Naman'
  }, 1000);

  let items= [
    {id: 1, name: 'phone', price: 80000},
    {id: 2, name: 'fridge', price: 40000},
    {id: 3, name: 'ac', price: 50000},
  
  ]

  let volume = 0;
  $: if (volume < 0) {
    alert(`You can't go lower`)
    volume = 0
  } else if (volume > 20) {
    alert(`Can't go higher`)
    volume = 20;
  } 


  $:total = items.reduce((acc, curr) => acc += curr.price, 0);
</script>

<main>
  <button on:click={() => volume -= 2}>-</button>
  <h2>Volume: {volume}</h2>
  <button on:click={() => volume += 2}>+</button>

  <h2>{firstName} {lastName}</h2>
  <h2>{fullName}</h2>
  <h2>Total price: {total}</h2>

  <button on:click={() => {
    firstName = 'Yojan';
    lastName = 'Saini'
  }}>Click to change name</button>

  <button on:click={() => {
    // items.push({id: 4, name: 'microwave', price: 60000}) // this will not work
    items = [...items, {id: 4, name: 'microwave', price: 60000}]
    console.log(items)
  }}>Click to add an item</button>
</main>

<style>

</style>
