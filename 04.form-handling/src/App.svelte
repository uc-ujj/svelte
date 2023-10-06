<script>
  const formValues = {
    name: '',
    age: 0,
    details: '',
    country: '',
    jobLocation: [],
    remote: false,
    skillSet: [],
    gender: ''
  }

  
  function handleSubmit(e) {
    e.preventDefault()
    console.log(formValues)
  }
</script>

<main>
  <form on:submit={handleSubmit}>
    <div>
      <label for="name">Name</label>
      <input type="text" name="" id="name" bind:value={formValues.name}>
      <label for="age">Age</label>
      <input type="number" name="" id="age" bind:value={formValues.age}>
    </div>
    <div>
      <label for="summary">Enter you details</label>
      <textarea name="" id="summary" cols="20" rows="10" bind:value={formValues.details} />
    </div>
    <div>
      <label for="country"></label >
      <select name="" id="country" bind:value={formValues.country}>
        <option value="" disabled>Select a Country</option>
        <option value="india">India</option>
        <option value="nepal">Nepal</option>
        <option value="sri-lanka">Sri Lanka</option>
        <option value="hong-kong">Hong Kong</option>
      </select>
    </div>
    <div>
      <label for="job-location">Job Location</label>
      <select name="job-location" id="job-location" multiple bind:value={formValues.jobLocation}>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
        <option value="dubai">Dubai</option>
      </select>
    </div>

    <div>
      <input type="checkbox" name="remote" id="remote" bind:checked={formValues.remote}>
      <label for="remote">Do you need Remote Job?</label>
    </div>

    <div>
      <label for="language">Languages</label>
      <!-- <input type="checkbox" id="language"> -->
      <input type="checkbox" name="javascript" id="javascript" value="javascript" bind:group={formValues.skillSet}>
      <label for="javascript">JavaScript</label>
      <input type="checkbox" name="python" id="python" value="python" bind:group={formValues.skillSet}>
      <label for="python">Python</label>
      <input type="checkbox" name="react" id="react" value="react" bind:group={formValues.skillSet}>
      <label for="react">React</label>
    </div>

    <div>
      <input type="radio" name="male" id="male" value="male" bind:group={formValues.gender}>
      <label for="male">Male</label>
      <input type="radio" name="female" id="female" value="female"  bind:group={formValues.gender}>
      <label for="female">Female</label>
    </div>

    <button>Submit</button>
  </form>
  <div>
    <pre>
      {JSON.stringify(formValues, null, 1)}
    </pre>
  </div>

 

</main>

<style>
  input + label {
    display: inline-flex;
  }

  main {
		/* text-align: center; */
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
