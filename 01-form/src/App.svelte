<script lang="ts">
  let form = {
    userName: '',
    email: '',
    password: '',
  };

  const handleSubmit = (e: Event) => {
    e.preventDefault();
    const { userName } = form;

    if (userName === 'manudous') {
      alert(`User ${userName} is already taken`);
      return;
    }
  };
</script>

<main>
  <h1>Hello User!!</h1>
  <div class="form">
    <form on:submit={handleSubmit}>
      <label for="userName">userName: </label>
      <input bind:value={form.userName} name="userName" />

      <label for="email">Email: </label>
      <input bind:value={form.email} name="email" />

      <label for="message">Passord: </label>
      <input type="password" bind:value={form.password} name="password" />

      <button type="submit">Submit</button>
    </form>
  </div>
</main>

<style>
  form {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  label {
    margin-bottom: 0.5rem;
    font-weight: 700;
  }
  input {
    margin-bottom: 0.5rem;
    border: 1px solid #ccc;
    padding: 0.5rem;
    border-radius: 0.5rem;
  }
</style>
