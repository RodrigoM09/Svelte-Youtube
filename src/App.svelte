<script>
	// Binding Text -------------------------------------------------------------------------------->
	// const name = 'Rodrigo'

	// Binding HTML -------------------------------------------------------------------------------->
	// const channel = '<b>Svelte Brasil</b>'
	// const hack = `<a href="#" onclick="alert('Te Hackearon!')">Hackeado!</a>`

	// Binding ID -------------------------------------------------------------------------------->
	// const headingId = 'heading'

	// Binding Attributes -------------------------------------------------------------------------------->
	// const disabled = true
	// const isPromoted = true
	// const promoted = true

	// Binding Classes --------------------------------------------------------------------------------->
	// const status = 'danger'

	// Conditional Rendering -------------------------------------------------------------------------------->
	// const num = 0;

	// List Rendering -------------------------------------------------------------------------------->
	// const names = ['Bruce', 'Clark', 'Diana']
	// const fullNames = [
	// 	{ first: 'Bruce', last: 'Wayne' },
	// 	{ first: 'Clark', last: 'Kent' },
	// 	{ first: 'Diana', last: 'Prince' }
	// ]

	// Inline Event Handling -------------------------------------------------------------------------------->
	// let count = 0;

	// Event Handling -------------------------------------------------------------------------------->
	// let count = 0;
	// function handleClick(event){
	// 	console.log(event);
	// 	count += 1;
	// }

	// Form Handling -------------------------------------------------------------------------------->
		// const formValues = {
		// 	name: '',
		// 	profileSummaries: '',
		// 	country: '',
		// 	jobLocation: [],
		// 	remoteWork: false,
		// 	skills: [],
		// 	yearsofExperience: ''
		// };

		// function submitForm(e){
		// 	e.preventDefault();
		// 	console.log(formValues);
			
		// }
	
	// Reactive Declarations -------------------------------------------------------------------------------->
	// let firstName = 'Bruce';
	// let lastName = 'Wayne';
	// $: fullName = `${firstName} ${lastName}`;
	// $: { const greet = `Full name is ${firstName} ${lastName}`
	// 	console.log(greet)
	// };
	// let items = [
	// 	{
	// 	id: 1,
	// 	title: 'TV',
	// 	price: 100
	// 	},
	// 	{
	// 	id: 2,
	// 	title: 'Phone',
	// 	price: 200
	// 	},
	// 	{
	// 	id: 3,
	// 	title: 'Laptop',
	// 	price: 300
	// 	}
	// ]
	// $: total = items.reduce((total, curr) =>(total = total + curr.price), 0)
	// let volume = 0;
	// $: {
	// 	if(volume < 0){
	// 		alert('Volume cannot be less than 0')
	// 		volume = 0;
	// 	}else if(volume > 20){
	// 		alert('Volume cannot be greater than 20')
	// 		volume = 20;
	// 	}
	// }

	// Svelte Component Props -------------------------------------------------------------------------------->
	// import Greet from './components/Greet.svelte';	
	// const name = 'Rodrigo';
	// const channel = 'Svelte Brasil';
	// const obj = {
	// 	name: 'Barry',
	// 	heroName: 'Flash'
	// }

	// Context API -------------------------------------------------------------------------------->
	// import {setContext} from 'svelte';
	// import ComponentC from "./components/ComponentC.svelte";

	// const userName = 'Rodrigo';
	// setContext('username-context', userName);

	// Component Events -------------------------------------------------------------------------------->
	// import Popup from "./components/Popup.svelte";
	// let showPopup = false;
	
	// function closePopup(event){
	// 	console.log(event.detail);
	// 	showPopup = false;
	// }
	
	// Event Forwarding -------------------------------------------------------------------------------->
	// import Outter from "./components/Outter.svelte";
	// import Button from "./components/Button.svelte";
	// 	function handleGreet(event){
	// 		alert(event.detail);
	// 	}

	// Slots -------------------------------------------------------------------------------->
	// import Card from "./components/Card.svelte";

	// Component Styles -------------------------------------------------------------------------------->
	// import NameList from "./components/NameList.svelte";
	// import ChildStyles from "./components/ChildStyles.svelte";
	
	// Lifecycle Hooks -------------------------------------------------------------------------------->
	// import PostList from "./components/PostList.svelte";

	// This Binding -------------------------------------------------------------------------------->
	// import AutoFocus from "./components/AutoFocus.svelte";

	// Dynamic Components -------------------------------------------------------------------------------->
	// import TabA from "./components/TabA.svelte";
	// import TabB from "./components/TabB.svelte";
	// import TabC from "./components/TabC.svelte";

	// let activeTab = TabA;

	// Module Context -------------------------------------------------------------------------------->
	// import Counter, { getTotalCount } from "./Counter.svelte";

	// Writable Stores -------------------------------------------------------------------------------->
	// import Display from "./components/Display.svelte";
  	// import Increment from "./components/Increment.svelte";
	// import Decrement from "./components/Decrement.svelte";
	// import Reset from "./components/Reset.svelte";

	// Readable and Derived Stores -------------------------------------------------------------------------------->
	// import Timer from "./components/Timer.svelte";

	//Custom Stores -------------------------------------------------------------------------------->
	import Display from "./components/Display.svelte";

</script>



<main>

	<!--Custom Stores -->
	<Display />


	<!-- Readable and Derived Stores
	<Timer />
	-------------------------------------------------------------------------------->


	<!-- Writable Stores 
	<Display />
	<Increment />
	<Decrement />
	<Reset />
	-------------------------------------------------------------------------------->

	
	<!-- Module Context 
	<button on:click={() => alert(getTotalCount())}>Alert Total Count</button>
	<Counter />
	<Counter />
	<Counter />
	-------------------------------------------------------------------------------->
	
	


	<!-- Dynamic Components using built in svelte element
	<button on:click={()=>(activeTab = TabA)}>TabA</button>
	<button on:click={()=>(activeTab = TabB)}>TabB</button>
	<button on:click={()=>(activeTab = TabC)}>TabC</button>

	<svelte:component this={activeTab}/>
	-------------------------------------------------------------------------------->

	<!-- Dynamic Components using else if for components
		 {#if activeTab === 'TabA'}
		<TabA/>
	{:else if activeTab === 'TabB'}
		<TabB/>
	{:else if activeTab === 'TabC'}
		<TabC/>
	{/if} -->


	<!-- This Binding 
	<AutoFocus />
	-------------------------------------------------------------------------------->

	<!-- lifecycle hooks onMount
	
	<PostList />
	-------------------------------------------------------------------------------->

	<!-- Component Styles 
	<NameList>
		<h3 slot='hero', let:firstName let:lastName> {firstName}, {lastName}</h3>
	</NameList> 
	<h4>App Component Text</h4>
	<h3>App Component Global Style</h3>


	<ChildStyles />
	-------------------------------------------------------------------------------->


	 <!-- Slots -->
	<!-- <Card content='Card content 1'/>
	<Card content='Card content 2'/> -->
	<!-- <Card>Card Content</Card>
	<Card><h2>Card Content</h2></Card> 
	<Card><img src="https://picsum.photos/200" alt=""></Card>
	<Card />
	
	<Card>
		<div slot="header">
			<h3>Header</h3>
		</div>
		<div slot="content">
			<img src="https://picsum.photos/200" alt="">
		</div>
		<div class="footer">
			<button>View Details</button>
		</div>
	</Card>
	-------------------------------------------------------------------------------->

	<!--Event Forwarding
	<Outter on:greet={handleGreet}/>
	<Button on:click={() => alert('Clicked')}>Click</Button>
	-------------------------------------------------------------------------------->

	<!-- Component Events 
	<button on:click={() => (showPopup = true)}>Show Popup</button>
	{#if showPopup}
		<Popup on:close={closePopup} />
	{/if}
	-------------------------------------------------------------------------------->

	<!-- Context API 
	<h2>App Component Username - {userName}</h2>
	<ComponentC />
	-------------------------------------------------------------------------------->

	<!-- Svelte Components Props 
	<Greet name='Bruce' heroName='Batman'/>
	<Greet name='Clark' heroName='Superman'/>
	<Greet name='Diana' heroName='Wonder Woman'/>
	<Greet {name} heroName={channel}/>
	<Greet {...obj}/> 
	-------------------------------------------------------------------------------->

	<!-- Reactive Declarations 
	<h2>Current volume {volume}</h2>
	<button on:click={() => (volume += 2)}>Increase Volume</button><br>
	<button on:click={() => (volume -= 2)}>Decrease Volume</button><br>
	<button on:click={()=> (items = [...items, {id: 4, title: 'keyboard', price: 50 }])}>Add Items</button><br>
	<button on:click={()=> {
		firstName = 'Clark'
		lastName = 'Kent'
	}}>Change Name</button>
	<h1>Hello {firstName} {lastName}</h1>
	<h2>{fullName}</h2>
	<h2>
		Total - {total}
	</h2> 
	-------------------------------------------------------------------------------->

	<!-- Form Handling 
	<div>
		<pre>
			{JSON.stringify(formValues, null, 2)}
		</pre>
	</div>
	<form on:submit={submitForm}>
		<div>
			<label for="name"></label>
			<input type="text" name="name" id="name" bind:value={formValues.name}>
		</div>
		<div>
			<label for="profile">Profile Summary</label>
			<textarea id="profile" bind:value={formValues.profileSummaries}></textarea>
		</div>
		<div>
			<label for="country">Country</label>
			<select name="" id="country" bind:value={formValues.country}>
				<option value="">Select a country</option>
				<option value="US">United States</option>
				<option value="MX">Mexico</option>
				<option value="CA">Canada</option>
				<option value="BR">Brazil</option>
			</select>
		</div>
				<div>
			<label for="job-location">Job Location</label>
			<select name="" id="job-location" bind:value={formValues.jobLocation} multiple>
				<option value="">Select a country</option>
				<option value="US">United States</option>
				<option value="MX">Mexico</option>
				<option value="CA">Canada</option>
				<option value="BR">Brazil</option>
			</select>
		</div>
		<div>
			<input type="checkbox" name="" id="remoteWork" bind:checked={formValues.remoteWork}>
			<label for="remoteWork">Open to Remote Work?</label>
		</div>
		<div>
			<label for="skills">Skills</label>
			<input type="checkbox" name="html" id="html" bind:group={formValues.skills}>
			<label for="html">HTML</label>
			<input type="checkbox" name="css" id="css" bind:group={formValues.skills}>
			<label for="css">CSS</label>
			<input type="checkbox" name="js" id="js" bind:group={formValues.skills}>
			<label for="js">JavaScript</label>
		</div>
		<div>
			<label for="years">Years of Experience</label>
			<input type="radio" value="0-2" id="0-2" bind:group={formValues.yearsofExperience}>
			<label for="0-2">0-2</label>
			<input type="radio" value="3-5" id="3-5" bind:group={formValues.yearsofExperience}>
			<label for="3-5">3-5</label>
			<input type="radio" value="6-10" id="6-10" bind:group={formValues.yearsofExperience}>
			<label for="6-10">6-10</label>
			<input type="radio" value="10+" id="10+" bind:group={formValues.yearsofExperience}>
			<label for="10+">10+</label>
		</div>
		<button>Submit</button>
	</form>
	-------------------------------------------------------------------------------->

	<!-- Event Handling
	<button on:click={handleClick}>Count {count}</button>
	-------------------------------------------------------------------------------->

	<!-- Inline Event Handling 
	<button on:click={() => (count = count + 1)}>Count {count}</button>
	-------------------------------------------------------------------------------->

	<!-- List Rendering
		{#each fullNames as name, index(name.last)}
		<h2>{index + 1} {name.first} {name.last}</h2>
		{/each}
		
		{#each names as name, index(name)}
		<h1>{index + 1} {name}</h1>
		{/each} 
	-------------------------------------------------------------------------------->

	<!-- Conditional Rendering 
	{#if num === 0 }
	<h2>The number is zero</h2>
	{:else if num < 0}
	<h2>The number is negative</h2>
	{:else if num > 0}
	<h2>The number is </h2>
	{:else}
	<h2>The number is not zero</h2>
	{/if}  
	-->
	
	<!-- Binding Styles
	<h2 class="underlined">underlined text</h2>
	<h2 class={status}>Status</h2> 
	-->

	<!-- Binding Text
	<h1>Hello {name}</h1> 
	-->

	<!-- Binding Classes
	<h2 class={isPromoted ? 'promoted' : ''}>Movie Title</h2>
	<h2 class:promoted={isPromoted}>Movie Title 2</h2>
	<h2 class:promoted>Movie Title 3</h2> 
	-->

	<!-- Binding HTML
	<p>Welcome to {@html channel}</p>
	<p>{@html hack}</p> 
	-->

	<!-- Binding Properties
	<h1 id={headingId}>Heading</h1> 
	-->

	<!-- Binding Attributes
	<button {disabled}>Bind</button> 
	-------------------------------------------------------------------------------->
</main>

<style> 
:global(h3){
	color: blue;
}
	h4{
		color: orange;
	}
	/* input + label {
		display: inline-flex;
	} */
	/* .underlined{
		text-decoration: underline;
	}
	.danger{
		color: red;
	}
	.success{
		color: green;
	}
	.promoted{
		font-style: italic;
	} */
	main {
		text-align: center;
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