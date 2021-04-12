<script>
  import { goto } from '@sapper/app';

  let title;
  let salaly;
  let details;
  const handleSubmit = async () => {
    if (title && salaly && details) {
      const res = await fetch('jobs.json', {
        method: 'POST',
        headers: { 'content-type': 'application/json' },
        body: JSON.stringify({ title, salaly, details }),
      });
      const updatedJobs = await res.json();
      // console.log(updatedJobs);
      goto('jobs');
    }
  };
</script>

<h2>Add a New Job</h2>
<form on:submit|preventDefault={handleSubmit}>
  <input type="text" placefolder="job title" bind:value={title} required />
  <input type="number" placefolder="salaly" bind:value={salaly} required />
  <textarea placeholder="job detail" bind:value={details} required />
  <button class="btn">Add new job</button>
</form>

<style>
  h2 {
    text-align: center;
  }
  form {
    max-width: 360px;
    margin: 40px auto;
    text-align: center;
  }
  input,
  textarea {
    display: block;
    width: 100%;
    padding: 10px;
    font-family: arial;
    margin: 10px auto;
    border: 1px solid #eee;
    border-radius: 8px;
  }
</style>
